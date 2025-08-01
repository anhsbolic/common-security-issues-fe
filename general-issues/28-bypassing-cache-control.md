# 28 Bypassing Cache-Control (private data bisa di-cache browser)

## Problem
Data privat tidak diberi header cache-control yang benar.

## Risk
- Data sensitif tersimpan di browser/public cache

## Example (Before)
// Tidak ada header cache-control

## Solution (After)
```http
Cache-Control: no-store, no-cache, must-revalidate
```

## How to Avoid
1. Tambahkan header cache-control pada data sensitif.
2. Gunakan HTTPS.
3. Hindari penyimpanan PII di local cache.
