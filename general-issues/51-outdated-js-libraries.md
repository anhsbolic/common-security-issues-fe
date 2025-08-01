# 51 Using Outdated JavaScript Libraries with Known CVE

## Problem
Menggunakan library JS yang sudah memiliki CVE (Common Vulnerabilities and Exposures).

## Risk
- Serangan melalui bug library.
- Potensi supply chain attack.

## Example (Before)
```javascript
<script src="https://cdn.example.com/old-library.js"></script>
```

## Solution (After)
- Update library ke versi terbaru yang sudah patched.
- Gunakan CDN resmi atau package manager yang terverifikasi.

## How to Avoid
1. Pantau CVE dari library yang digunakan.
2. Jalankan `npm audit` dan update secara berkala.
3. Gunakan Dependabot atau Snyk untuk notifikasi.
