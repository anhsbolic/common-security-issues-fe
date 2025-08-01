# 65 Exposing Hidden Debug Routes in SPA

## Problem
Routing SPA memiliki route debug yang tidak diproteksi.

## Risk
- Akses fitur internal oleh attacker.

## Example (Before)
```javascript
{ path: '/debug', component: DebugPanel }
```

## Solution (After)
- Hapus route debug di production.
- Tambahkan autentikasi pada route sensitif.

## How to Avoid
1. Review routing sebelum deploy.
2. Gunakan environment flag untuk fitur debug.
3. Audit setiap perubahan route.
