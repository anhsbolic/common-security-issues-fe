# 27 Insecure File Upload (tanpa extension dan content type check)

## Problem
File upload diterima tanpa cek jenis file, memungkinkan upload file berbahaya.

## Risk
- Upload shell atau script berbahaya
- Penyalahgunaan storage

## Example (Before)
```javascript
<input type="file" name="file">
```

## Solution (After)
```javascript
const allowed = ['image/png','image/jpeg'];
if(!allowed.includes(file.type)) return alert("File tidak diizinkan");
```

## How to Avoid
1. Validasi ekstensi dan content type di frontend dan backend.
2. Batasi ukuran file.
3. Scan file upload dengan antivirus.
