# 63 Misuse of Geolocation API without Consent Flow

## Problem
Mengakses lokasi user tanpa persetujuan atau tanpa menjelaskan alasan.

## Risk
- Kebocoran lokasi sensitif.
- Pelanggaran privasi.

## Example (Before)
```javascript
navigator.geolocation.getCurrentPosition(pos => {...});
```

## Solution (After)
- Minta izin user dengan penjelasan.
- Gunakan HTTPS untuk semua permintaan.

## How to Avoid
1. Beri tahu user alasan penggunaan lokasi.
2. Pastikan lokasi hanya diakses setelah user setuju.
3. Audit semua fitur yang menggunakan geolocation.
