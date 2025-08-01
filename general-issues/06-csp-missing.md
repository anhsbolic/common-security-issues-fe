# 06 Content Security Policy (CSP) Missing atau Salah Konfigurasi

## Problem
Tidak adanya CSP atau konfigurasi yang salah memungkinkan eksekusi script tak terduga.

## Risk
- XSS lebih mudah dieksploitasi
- Data injection tidak terdeteksi

## Example (Before)
// Tidak ada CSP header

## Solution (After)
```html
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self'">
```

## How to Avoid
1. Terapkan CSP ketat sesuai kebutuhan aplikasi.
2. Uji CSP dengan mode report-only sebelum enforced.
3. Perbarui whitelist domain ketika menambah resource baru.
