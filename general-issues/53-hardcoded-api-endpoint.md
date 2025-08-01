# 53 Hardcoded API Endpoint in JS (leak staging or dev endpoints)

## Problem
Endpoint API untuk staging atau dev di-hardcode dan ikut terkirim ke production.

## Risk
- Potensi data bocor ke environment yang salah.
- Bisa digunakan attacker untuk menemukan endpoint internal.

## Example (Before)
```javascript
const API_URL = "http://dev.api.example.com";
```

## Solution (After)
```javascript
const API_URL = process.env.API_URL;
```

## How to Avoid
1. Gunakan environment variable.
2. Jangan hardcode endpoint dalam kode.
3. Pastikan build production tidak mengandung URL dev/staging.
