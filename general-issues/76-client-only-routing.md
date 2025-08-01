# 76 Client-side Only Routing untuk Protected Routes

## Problem
Protected route hanya dicek di frontend.

## Risk
- User bisa akses API langsung tanpa autentikasi.

## Example (Before)
```javascript
if(!isLoggedIn) redirect('/login');
```

## Solution (After)
- Tambahkan validasi di server.
- Gunakan JWT atau session server-side.

## How to Avoid
1. Jangan hanya rely pada frontend routing.
2. Gunakan middleware di server.
3. Audit semua route yang dianggap protected.
