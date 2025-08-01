# 58 LocalStorage Session Token without Expiration Logic

## Problem
Token disimpan di localStorage tanpa mekanisme kedaluwarsa.

## Risk
- Token tetap berlaku setelah logout.
- Potensi penyalahgunaan jika device hilang.

## Example (Before)
```javascript
localStorage.setItem('token', token);
```

## Solution (After)
- Simpan token di HttpOnly cookie atau memory state.
- Tambahkan mekanisme refresh & expiry.

## How to Avoid
1. Jangan gunakan localStorage untuk token jangka panjang.
2. Tambahkan mekanisme sesi otomatis kadaluarsa.
3. Hapus token saat logout.
