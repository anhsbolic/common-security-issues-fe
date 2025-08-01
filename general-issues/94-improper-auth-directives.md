# 94 Improper Validation sebelum @auth atau @guest Directives

## Problem
Mengandalkan Blade directive untuk kontrol akses tanpa cek di controller.

## Risk
- Kontrol akses hanya di UI, bukan di logic.

## Example (Before)
```blade
@auth
  <a href="/admin">Admin</a>
@endauth
```

## Solution (After)
- Tambahkan cek role di controller atau middleware.

## How to Avoid
1. Gunakan middleware untuk otorisasi.
2. Jangan hanya rely pada directive view.
3. Audit semua akses admin/user.
