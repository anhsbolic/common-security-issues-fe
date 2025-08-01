# 43 Missing Feature Policy / Permissions Policy (mencegah abuse kamera, mic)

## Problem
Tidak ada Permissions Policy, sehingga semua iframe bisa akses fitur seperti kamera, mic, dan geolocation.

## Risk
- Iframe jahat bisa memanfaatkan fitur sensitif.

## Example (Before)
// Tidak ada Permissions Policy

## Solution (After)
```http
Permissions-Policy: camera=(), microphone=(), geolocation=()
```

## How to Avoid
1. Tambahkan Permissions Policy sesuai kebutuhan.
2. Audit penggunaan iframe.
3. Gunakan CSP untuk membatasi domain.
