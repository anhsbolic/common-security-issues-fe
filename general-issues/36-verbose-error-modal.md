# 36 Information Disclosure via Verbose Error Modal

## Problem
Modal error menampilkan detail stack trace atau config internal.

## Risk
- Bocor path file, library version, atau info internal
- Membantu attacker mengenali aplikasi

## Example (Before)
```javascript
alert(error.stack);
```

## Solution (After)
```javascript
alert("Terjadi kesalahan, coba lagi nanti.");
console.error(error);
```

## How to Avoid
1. Tampilkan pesan error generik ke user.
2. Log detail di console atau server.
3. Nonaktifkan debug di production.
