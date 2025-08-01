# 88 Improper Lazy Loading mengungkap Data Sensitif di Bundle

## Problem
Lazy load module dengan data sensitif di import.

## Risk
- Data ikut terbawa di bundle terpisah.

## Example (Before)
```javascript
const Secret = React.lazy(() => import('./Secret'));
```

## Solution (After)
- Pisahkan module sensitif dari bundle client.

## How to Avoid
1. Jangan masukkan data sensitif di kode client.
2. Audit hasil bundling.
3. Gunakan dynamic import hanya untuk komponen UI.
