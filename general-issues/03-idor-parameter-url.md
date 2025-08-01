# 03 Insecure Direct Object Reference (IDOR) di Parameter URL

## Problem
Aplikasi mengambil resource langsung berdasarkan parameter user tanpa otorisasi tambahan.

## Risk
- User dapat mengakses data milik orang lain (contoh: /user?id=2)
- Potensi kebocoran data pribadi atau sensitif

## Example (Before)
```javascript
fetch(`/api/user?id=${userId}`)
  .then(res => res.json())
```

## Solution (After)
```javascript
app.get('/api/user', authenticate, (req, res) => {
  if (req.user.id !== req.query.id) return res.status(403).send('Forbidden');
  // ...
});
```

## How to Avoid
1. Jangan percaya input user untuk akses langsung ke resource.
2. Tambahkan validasi otorisasi di server.
3. Gunakan identifier acak (UUID) bukan ID urut jika memungkinkan.
