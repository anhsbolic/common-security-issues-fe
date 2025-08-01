# 15 Token Leakage di URL atau Local Storage

## Problem
Token autentikasi ditampilkan di URL atau disimpan di localStorage.

## Risk
- Token bocor di history browser atau referer
- Pengambilalihan session

## Example (Before)
```javascript
const token = location.search.split('token=')[1];
localStorage.setItem('token', token);
```

## Solution (After)
- Gunakan cookie HttpOnly untuk menyimpan token.
- Hapus parameter token dari URL setelah digunakan.

## How to Avoid
1. Jangan kirim token via query string.
2. Gunakan cookie HttpOnly + Secure.
3. Simpan token hanya di memory state (Vuex/Pinia).
