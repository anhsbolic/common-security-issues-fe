# 61 Improper Cache Busting (Sensitive JS served from stale cache)

## Problem
Asset JS sensitif tidak memiliki cache-busting, sehingga browser bisa menyajikan versi lama.

## Risk
- Patch keamanan tidak langsung diterapkan.
- Potensi eksekusi kode lama yang rentan.

## Example (Before)
```html
<script src="/app.js"></script>
```

## Solution (After)
```html
<script src="/app.js?v=12345"></script>
```

## How to Avoid
1. Gunakan hash atau versi unik pada asset.
2. Gunakan build tools yang mendukung cache-busting otomatis.
3. Audit caching policy pada production.
