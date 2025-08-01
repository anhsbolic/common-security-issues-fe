# 05 Mixed Content (HTTP vs HTTPS) di Asset Load

## Problem
Halaman yang di-load lewat HTTPS mengambil resource (JS, CSS, gambar) via HTTP. Hal ini membuka peluang man-in-the-middle attack.

## Risk
- Penyisipan kode berbahaya ke dalam resource
- Hilangnya jaminan integritas konten

## Example (Before)
```html
<script src="http://cdn.example.com/lib.js"></script>
```

## Solution (After)
```html
<script src="https://cdn.example.com/lib.js"></script>
```

## How to Avoid
1. Pastikan semua resource menggunakan HTTPS.
2. Gunakan Content Security Policy `upgrade-insecure-requests`.
3. Audit dependency dan CDN secara berkala.
