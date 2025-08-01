# 16 Improper Input Validation di Form Binding

## Problem
Tidak ada validasi input, memungkinkan data invalid atau injeksi karakter berbahaya.

## Risk
- Data kotor masuk ke backend
- Potensi XSS/SQL Injection jika backend tidak memvalidasi ulang

## Example (Before)
```vue
<input v-model="email">
```

## Solution (After)
```javascript
const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
if(!emailPattern.test(this.email)) return alert("Email tidak valid");
```

## How to Avoid
1. Validasi input di frontend dan backend.
2. Gunakan library validasi (Vuelidate/Yup).
3. Tampilkan pesan error yang jelas ke user.
