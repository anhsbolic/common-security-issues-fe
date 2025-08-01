# 04 Clickjacking di Frame Embedding

## Problem
Aplikasi dapat dimuat dalam iframe oleh domain lain, memungkinkan attacker membuat UI palsu yang menipu user untuk melakukan klik tanpa sadar.

## Risk
- Pengambilalihan aksi user (misal klik tombol submit atau konfirmasi)
- Potensi serangan phishing visual

## Example (Before)
// Tidak ada proteksi terhadap embedding iframe

## Solution (After)
```http
X-Frame-Options: DENY
Content-Security-Policy: frame-ancestors 'none';
```

## How to Avoid
1. Tambahkan header `X-Frame-Options` atau `Content-Security-Policy` dengan `frame-ancestors`.
2. Gunakan library keamanan default dari framework.
3. Audit penggunaan iframe pada aplikasi.
