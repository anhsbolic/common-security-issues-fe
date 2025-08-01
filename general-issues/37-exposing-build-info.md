# 37 Exposing Build Info di Frontend

## Problem
Versi framework, commit hash, atau path build ditampilkan di console log.

## Risk
- Memberi informasi tambahan ke attacker (fingerprinting)

## Example (Before)
```javascript
console.log("Build version:", process.env.COMMIT_HASH);
```

## Solution (After)
- Hilangkan log versi di production atau tampilkan hanya untuk admin.

## How to Avoid
1. Gunakan flag untuk matikan log di production.
2. Audit penggunaan console.log sebelum release.
3. Jangan embed commit hash sensitif di frontend.
