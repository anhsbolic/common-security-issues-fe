# 56 Not Handling File Drag-and-Drop Properly (Arbitrary File Upload)

## Problem
Drag-and-drop file tidak divalidasi tipenya.

## Risk
- Upload file berbahaya (executable, script).

## Example (Before)
```javascript
dropzone.addEventListener('drop', e => {
  e.preventDefault();
  uploadFile(e.dataTransfer.files[0]);
});
```

## Solution (After)
```javascript
const allowed = ['image/png', 'image/jpeg'];
if(!allowed.includes(file.type)) return alert('Tipe file tidak didukung');
uploadFile(file);
```

## How to Avoid
1. Validasi file type dan ukuran.
2. Tambahkan validasi di backend.
3. Jangan izinkan folder upload langsung terbuka ke publik.
