# 29 Browser Storage untuk PII (IndexedDB/Session Storage tanpa enkripsi)

## Problem
Menyimpan PII di browser storage tanpa enkripsi.

## Risk
- PII mudah diambil jika ada XSS
- Data bisa bocor di perangkat bersama

## Example (Before)
```javascript
sessionStorage.setItem('user', JSON.stringify(userData));
```

## Solution (After)
- Simpan hanya data non-PII.
- Gunakan cookie HttpOnly untuk data sensitif.

## How to Avoid
1. Hindari menyimpan PII di browser storage.
2. Enkripsi data jika harus disimpan sementara.
3. Hapus storage saat logout.
