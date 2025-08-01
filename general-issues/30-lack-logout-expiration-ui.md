# 30 Lack of Logout Mechanism atau Session Expiration UI

## Problem
Tidak ada tombol logout atau session tidak pernah kadaluarsa.

## Risk
- Akun tetap login di perangkat umum
- Resiko session hijack

## Example (Before)
// Tidak ada logout
```javascript
// session tidak pernah habis
```

## Solution (After)
- Tambahkan tombol logout.
- Implementasi session timeout dengan peringatan UI.

## How to Avoid
1. Tambahkan mekanisme logout di UI.
2. Pastikan session otomatis kadaluarsa.
3. Tampilkan notifikasi session hampir habis.
