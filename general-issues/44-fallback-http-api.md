# 44 Fallback ke HTTP API saat HTTPS gagal (logic fallback insecure)

## Problem
Aplikasi fallback ke HTTP jika HTTPS gagal.

## Risk
- Potensi man-in-the-middle attack.

## Example (Before)
```javascript
fetch('http://' + apiHost);
```

## Solution (After)
- Hanya gunakan HTTPS dan tangani error koneksi dengan benar.

## How to Avoid
1. Jangan buat fallback ke HTTP.
2. Gunakan strict transport security.
3. Audit semua endpoint API.
