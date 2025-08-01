# 26 Exposing API Keys in Source Maps (map file di production)

## Problem
Source map production tidak dihapus, memungkinkan attacker melihat kode asli termasuk key atau endpoint.

## Risk
- Bocornya API key
- Pengetahuan penuh tentang struktur kode

## Example (Before)
// build menghasilkan .map dan tetap dipublish

## Solution (After)
// matikan source map di production build
```javascript
// vue.config.js
productionSourceMap: false
```

## How to Avoid
1. Matikan source map di production.
2. Jangan pernah commit key ke frontend.
3. Audit hasil build sebelum deploy.
