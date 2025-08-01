# 35 Relying on Client-side Time untuk Security Logic (contoh: token expiration)

## Problem
Keamanan mengandalkan jam di browser user.

## Risk
- User bisa mengubah jam dan bypass logika.
- Token expiration jadi tidak valid.

## Example (Before)
```javascript
if(Date.now() > token.exp) logout();
```

## Solution (After)
- Validasi token di server menggunakan waktu server.
- Jangan rely pada waktu client untuk keputusan security.

## How to Avoid
1. Gunakan server-side time untuk validasi.
2. Jangan percaya Date.now() untuk logika keamanan.
3. Audit semua kode yang menggunakan jam browser.
