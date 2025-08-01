# 85 Exposing Build Environment Variables via process.env

## Problem
process.env.* disalin ke bundle tanpa filtering.

## Risk
- Key atau URL internal bocor.

## Example (Before)
```javascript
console.log(process.env);
```

## Solution (After)
- Filter env hanya yang perlu di-expose.

## How to Avoid
1. Gunakan prefix (misalnya REACT_APP_) untuk variable yang aman.
2. Jangan log env di production.
3. Audit konfigurasi build.
