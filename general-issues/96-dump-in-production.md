# 96 Leaking Sensitive Data via @dd atau @dump di Production

## Problem
Menggunakan @dd atau @dump yang menampilkan detail internal.

## Risk
- Bocornya konfigurasi atau data user.

## Example (Before)
```blade
@dd($user)
```

## Solution (After)
- Hapus semua debug directive di production.

## How to Avoid
1. Gunakan logging bukan dump.
2. Audit kode sebelum release.
3. Tambahkan linter untuk mendeteksi @dd.
