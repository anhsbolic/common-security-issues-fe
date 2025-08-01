# 49 Use of Deprecated Crypto Functions di Browser (misalnya MD5 di frontend)

## Problem
Menggunakan fungsi kriptografi usang seperti MD5 atau SHA1.

## Risk
- Mudah di-crack.
- Menurunkan keamanan aplikasi.

## Example (Before)
```javascript
const hash = md5(password);
```

## Solution (After)
- Gunakan algoritma modern seperti SHA-256 atau bcrypt (server-side).

## How to Avoid
1. Jangan gunakan crypto usang.
2. Gunakan Web Crypto API.
3. Validasi library crypto yang dipakai.
