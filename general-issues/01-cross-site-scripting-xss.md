# 01 Cross-Site Scripting (XSS) di Input & Output

## Problem
Aplikasi menampilkan input user secara langsung ke dalam DOM tanpa validasi atau encoding yang benar. Hal ini memungkinkan attacker menyisipkan kode JavaScript berbahaya.

## Risk
- Pencurian cookie atau token sesi user
- Deface atau manipulasi tampilan halaman
- Eksekusi aksi tanpa izin di sisi pengguna

## Example (Before)
```javascript
const name = document.getElementById('input').value;
document.getElementById('output').innerHTML = `Hello ${name}`;
```

## Solution (After)
```javascript
const name = document.getElementById('input').value;
document.getElementById('output').textContent = `Hello ${name}`;
```

## How to Avoid
1. Gunakan `textContent` atau binding framework yang aman (`{{ variable }}` di Vue, JSX di React).
2. Jika harus render HTML, gunakan library sanitasi seperti DOMPurify.
3. Aktifkan Content Security Policy (CSP) untuk mencegah inline script.
