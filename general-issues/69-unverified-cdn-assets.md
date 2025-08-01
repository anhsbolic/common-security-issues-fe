# 69 Unverified CDN Asset Load

## Problem
Mengambil asset dari CDN tanpa integrity check.

## Risk
- Asset bisa diubah pihak ketiga.

## Example (Before)
```html
<script src="https://cdn.example.com/lib.js"></script>
```

## Solution (After)
```html
<script src="https://cdn.example.com/lib.js" integrity="sha384-..." crossorigin="anonymous"></script>
```

## How to Avoid
1. Gunakan SRI (Subresource Integrity).
2. Audit asset eksternal secara berkala.
3. Pertimbangkan self-host untuk asset kritis.
