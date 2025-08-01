# 19 Insecure JWT Handling (Expired / Refresh Logic)

## Problem
JWT disimpan tidak aman dan tidak dicek masa kedaluwarsanya.

## Risk
- Token tetap bisa dipakai setelah expired
- Session hijack

## Example (Before)
```javascript
localStorage.setItem('jwt', token);
axios.get('/secure', { headers: { Authorization: 'Bearer ' + token } });
```

## Solution (After)
- Gunakan HttpOnly cookie untuk token.
- Implementasi refresh token dengan rotasi.

## How to Avoid
1. Jangan simpan JWT di localStorage.
2. Validasi exp di frontend dan backend.
3. Hapus token saat logout.
