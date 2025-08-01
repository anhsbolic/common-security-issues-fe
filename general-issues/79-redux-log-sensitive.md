# 79 Redux Store Logging Sensitive Data di Production

## Problem
Redux store di-log lengkap ke console.

## Risk
- Data sensitif terlihat di devtools / console.

## Example (Before)
```javascript
console.log(store.getState());
```

## Solution (After)
- Hapus log di production.
- Gunakan middleware untuk filter.

## How to Avoid
1. Matikan logging di production build.
2. Gunakan redux-logger hanya di dev.
3. Audit konsol untuk data sensitif.
