# 70 Hardcoded Feature Flags in Production Build

## Problem
Feature flag di-hardcode sehingga fitur tersembunyi bisa diaktifkan dengan mudah.

## Risk
- Fitur belum siap diakses publik.

## Example (Before)
```javascript
const enableBeta = true;
```

## Solution (After)
- Gunakan sistem konfigurasi dinamis atau environment variable.

## How to Avoid
1. Jangan hardcode flag fitur.
2. Gunakan config server-side atau remote config.
3. Audit semua flag sebelum deploy.
