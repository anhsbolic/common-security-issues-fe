# 25 Weak Password Policy di Frontend Form Validation

## Problem
Validasi password terlalu lemah (misalnya hanya minimal 4 karakter).

## Risk
- Mudah ditebak/dibrute force
- Menurunkan standar keamanan aplikasi

## Example (Before)
```javascript
if(password.length < 4) showError("Password too short");
```

## Solution (After)
```javascript
const regex = /^(?=.*[A-Z])(?=.*[0-9]).{8,}$/;
if(!regex.test(password)) showError("Password harus kombinasi huruf besar dan angka, min 8 karakter");
```

## How to Avoid
1. Terapkan password policy yang kuat (misalnya OWASP).
2. Validasi di frontend dan backend.
3. Berikan indikator kekuatan password ke user.
