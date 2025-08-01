# 17 Insecure Third-Party Component (npm dependencies)

## Problem
Menggunakan library pihak ketiga yang rentan atau usang.

## Risk
- Terkena CVE dari dependency
- Potensi supply chain attack

## Example (Before)
// package.json
"dependencies": { "some-lib": "^1.0.0" }
```

## Solution (After)
- Update library ke versi terbaru.
- Jalankan `npm audit` dan `npm audit fix`.

## How to Avoid
1. Audit dependency secara berkala.
2. Gunakan Dependabot atau Snyk.
3. Hapus dependency yang tidak perlu.
