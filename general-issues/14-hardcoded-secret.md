# 14 Hardcoded Secret di File .env dan Config.js

## Problem
API key atau credential disimpan langsung di source frontend.

## Risk
- Kunci bocor ke publik (bundle JS dapat di-inspect)
- Penyalahgunaan API

## Example (Before)
```javascript
export const API_KEY = "ABC123SECRET";
```

## Solution (After)
```javascript
// Ambil key dari server-side, bukan frontend
fetch('/api/config').then(...);
```

## How to Avoid
1. Jangan simpan secret di frontend.
2. Gunakan proxy backend untuk akses API.
3. Rotasi key yang sudah bocor.
