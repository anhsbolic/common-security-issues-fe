# 92 Disabling CSRF Protection pada Form Routes

## Problem
Route tertentu dikecualikan dari proteksi CSRF.

## Risk
- Attacker bisa mengirimkan request palsu.

## Example (Before)
// VerifyCsrfToken middleware men-disable route
```php
protected $except = ['/update-profile'];
```

## Solution (After)
- Aktifkan kembali CSRF atau gunakan metode aman seperti token API.

## How to Avoid
1. Jangan disable CSRF kecuali benar-benar perlu.
2. Audit daftar except pada VerifyCsrfToken.
3. Gunakan SameSite cookie untuk tambahan proteksi.
