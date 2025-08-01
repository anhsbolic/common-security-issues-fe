# 91 Using {!! !!} untuk Unescaped Output leading to XSS

## Problem
Menggunakan sintaks {!! $var !!} tanpa sanitasi di Blade.

## Risk
- XSS jika variabel berasal dari input user.

## Example (Before)
```blade
{!! $userInput !!}
```

## Solution (After)
```blade
{{ $userInput }}
```

## How to Avoid
1. Gunakan {{ }} untuk auto-escape.
2. Jika harus HTML, gunakan sanitasi seperti Purifier.
3. Audit semua view Blade untuk {!! !!}.
