# 41 Click-to-Download tanpa Validasi (user bisa trigger arbitrary file download)

## Problem
Menyediakan link download yang menerima input user tanpa validasi.

## Risk
- Attacker dapat memaksa browser mendownload file berbahaya.
- Potensi drive-by download.

## Example (Before)
```javascript
const file = getParameter('file');
window.location.href = '/download/' + file;
```

## Solution (After)
- Validasi file di server dan hanya izinkan tipe tertentu.
- Gunakan Content-Disposition: attachment.

## How to Avoid
1. Jangan percaya input user untuk path file.
2. Validasi file name di backend.
3. Audit link download di frontend.
