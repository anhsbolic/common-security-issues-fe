# 100 Not Using @method Spoofing for Non-GET/POST Routes Securely

## Problem
Route PUT/DELETE tidak menggunakan spoofing dengan benar.

## Risk
- Potensi CSRF atau kesalahan method.

## Example (Before)
```blade
<form action="/user/1" method="POST">
</form>
```

## Solution (After)
```blade
<form action="/user/1" method="POST">
  @method('PUT')
  @csrf
</form>
```

## How to Avoid
1. Gunakan @method dengan benar.
2. Audit semua form dengan method non-GET/POST.
3. Pastikan middleware CSRF aktif.
