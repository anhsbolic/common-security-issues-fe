# 59 Sensitive Data in URL Hash (Fragment Leak)

## Problem
Data sensitif dikirim di URL hash (#).

## Risk
- Bocor di referer atau log.

## Example (Before)
```javascript
window.location.hash = "token=abc123";
```

## Solution (After)
- Jangan kirim data sensitif via URL fragment.
- Gunakan mekanisme sesi yang aman.

## How to Avoid
1. Gunakan cookie HttpOnly.
2. Hapus fragment setelah digunakan.
3. Audit mekanisme login/SSO.
