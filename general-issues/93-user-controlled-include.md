# 93 Including User-controlled Blade Template Paths

## Problem
Path view berasal dari input user.

## Risk
- Remote Code Execution jika attacker bisa memilih file.

## Example (Before)
```php
return view(request('template'));
```

## Solution (After)
- Validasi input template terhadap whitelist.

## How to Avoid
1. Jangan izinkan input user menentukan template path.
2. Audit semua view dynamic.
3. Gunakan mapping aman untuk view.
