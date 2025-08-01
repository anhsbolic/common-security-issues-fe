# 34 Missing Output Encoding untuk URL Parameters (open redirect risk)

## Problem
URL parameter langsung digunakan tanpa encoding.

## Risk
- Open redirect atau XSS via URL injection

## Example (Before)
```javascript
location.href = '/redirect?url=' + userUrl;
```

## Solution (After)
```javascript
const safeUrl = encodeURIComponent(userUrl);
location.href = '/redirect?url=' + safeUrl;
```

## How to Avoid
1. Encode semua parameter output.
2. Validasi domain tujuan sebelum redirect.
3. Gunakan library helper untuk URL building.
