# 10 Over-permissive CORS di Development & Production

## Problem
Mengizinkan semua origin (`*`) pada konfigurasi CORS membuat API bisa diakses domain mana pun.

## Risk
- Pencurian data API oleh pihak ketiga
- Penyalahgunaan API oleh attacker

## Example (Before)
```javascript
res.header('Access-Control-Allow-Origin', '*');
```

## Solution (After)
```javascript
const allowed = ['https://app.example.com'];
if (allowed.includes(req.headers.origin)) {
  res.header('Access-Control-Allow-Origin', req.headers.origin);
}
```

## How to Avoid
1. Gunakan whitelist domain.
2. Bedakan konfigurasi dev dan production.
3. Audit konfigurasi secara berkala.
