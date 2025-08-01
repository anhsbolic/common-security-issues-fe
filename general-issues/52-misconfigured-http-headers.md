# 52 Misconfigured HTTP Security Headers (X-Content-Type-Options, X-XSS-Protection)

## Problem
Tidak mengatur header HTTP yang penting untuk keamanan.

## Risk
- XSS lebih mudah terjadi.
- MIME sniffing menyebabkan eksekusi konten berbahaya.

## Example (Before)
// Tidak ada X-Content-Type-Options, X-XSS-Protection

## Solution (After)
```http
X-Content-Type-Options: nosniff
X-XSS-Protection: 1; mode=block
```

## How to Avoid
1. Atur header keamanan default.
2. Gunakan middleware security (helmet.js atau sejenisnya).
3. Audit header menggunakan tools seperti securityheaders.com.
