# 22 Client-side Authorization Logic tanpa Server-side Check

## Problem
Kontrol akses hanya di frontend (misal: hide button), tanpa validasi di server.

## Risk
- User bisa akses data atau fitur terlarang via request langsung.

## Example (Before)
```javascript
if(!user.isAdmin) hideAdminPanel();
```

## Solution (After)
- Tambahkan validasi role di backend.
- Frontend hanya untuk UX, bukan security utama.

## How to Avoid
1. Selalu cek izin di server.
2. Audit endpoint untuk memastikan otorisasi.
3. Jangan percaya data role yang dikirim dari client.
