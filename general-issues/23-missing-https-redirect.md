# 23 Missing HTTPS Redirect (aplikasi masih bisa diakses via HTTP)

## Problem
Aplikasi tidak mengarahkan HTTP ke HTTPS, membuka peluang serangan man-in-the-middle.

## Risk
- Data login bisa dicuri
- Integrity halaman tidak terjamin

## Example (Before)
// Tidak ada konfigurasi redirect

## Solution (After)
```nginx
server {
  listen 80;
  return 301 https://$host$request_uri;
}
```

## How to Avoid
1. Gunakan HSTS (HTTP Strict Transport Security).
2. Konfigurasi redirect di server.
3. Pastikan semua asset menggunakan HTTPS.
