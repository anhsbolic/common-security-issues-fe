# 82 Overusing Global State causing Data Leakage between Components

## Problem
Semua data, termasuk sensitif, disimpan di global state.

## Risk
- Komponen yang tidak berhak dapat membaca data.

## Example (Before)
```javascript
const store = createStore(reducer);
```

## Solution (After)
- Pisahkan state sensitif.
- Gunakan selector dengan izin akses.

## How to Avoid
1. Hindari menyimpan semua data di global state.
2. Gunakan modul state terpisah.
3. Audit akses state secara rutin.
