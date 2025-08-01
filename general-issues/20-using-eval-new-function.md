# 20 Using eval() atau new Function() di Vue

## Problem
Menjalankan string sebagai kode menggunakan `eval()` atau `new Function()`.

## Risk
- Eksekusi kode jahat jika input tidak terkontrol
- Remote Code Execution di sisi client

## Example (Before)
```javascript
eval(userInput);
```

## Solution (After)
- Hindari penggunaan eval sama sekali.
- Gunakan parser atau whitelist command.

## How to Avoid
1. Linter rule untuk melarang eval (`no-eval`).
2. Review library pihak ketiga yang menggunakan eval.
3. Gunakan CSP untuk memblokir eval.
