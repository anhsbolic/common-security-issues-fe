# 64 Unsafe Dynamic Script Insertion via createElement('script')

## Problem
Memasukkan script secara dinamis dari sumber yang tidak terverifikasi.

## Risk
- XSS dan eksekusi kode berbahaya.

## Example (Before)
```javascript
const script = document.createElement('script');
script.src = userInputUrl;
document.body.appendChild(script);
```

## Solution (After)
- Validasi URL script sebelum load.
- Gunakan CSP untuk membatasi sumber script.

## How to Avoid
1. Jangan izinkan user menentukan URL script.
2. Gunakan hanya sumber terpercaya.
3. Audit semua dynamic script injection.
