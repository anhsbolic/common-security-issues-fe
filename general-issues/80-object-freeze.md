# 80 Not Freezing Object.freeze on Config leading to Tampering

## Problem
Konfigurasi global tidak dibekukan, memungkinkan modifikasi runtime.

## Risk
- Attacker dapat mengubah konfigurasi aplikasi.

## Example (Before)
```javascript
const config = { featureEnabled: true };
window.config = config;
```

## Solution (After)
```javascript
const config = Object.freeze({ featureEnabled: true });
```

## How to Avoid
1. Bekukan object konfigurasi dengan Object.freeze.
2. Jangan expose config sensitif ke window.
3. Audit variable global di production.
