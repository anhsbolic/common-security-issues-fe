# 47 Misconfigured Service Worker Cache (private response cached public)

## Problem
Service Worker meng-cache response privat dan menyajikannya tanpa otorisasi.

## Risk
- Data sensitif bisa diakses offline atau oleh user lain.

## Example (Before)
```javascript
caches.open('app-cache').then(cache => cache.put(req, res));
```

## Solution (After)
- Jangan cache response dengan data privat.
- Gunakan cache control header yang tepat.

## How to Avoid
1. Audit strategi cache di Service Worker.
2. Gunakan runtime caching hanya untuk asset publik.
3. Hapus cache saat user logout.
