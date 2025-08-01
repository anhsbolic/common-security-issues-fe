# 07 Sensitive Data Exposure di Local Storage & Session

## Problem
Menyimpan data sensitif (token, credential) di localStorage membuatnya rentan dicuri lewat XSS.

## Risk
- Pengambilalihan akun user
- Kebocoran data sensitif ke pihak tidak sah

## Example (Before)
```javascript
localStorage.setItem('token', userToken);
```

## Solution (After)
```javascript
Set-Cookie: token=abc; HttpOnly; Secure; SameSite=Strict
```

## How to Avoid
1. Jangan simpan credential sensitif di localStorage/sessionStorage.
2. Gunakan cookie HttpOnly + Secure.
3. Pastikan session dihapus saat logout.
