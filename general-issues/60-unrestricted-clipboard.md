# 60 Unrestricted Clipboard Access via execCommand or Clipboard API

## Problem
Aplikasi mengakses clipboard tanpa izin atau validasi.

## Risk
- Potensi pencurian atau injeksi data clipboard.

## Example (Before)
```javascript
document.execCommand('paste');
```

## Solution (After)
- Gunakan Clipboard API dengan izin eksplisit.
- Beri notifikasi ke user.

## How to Avoid
1. Batasi akses clipboard hanya untuk aksi user.
2. Jangan mengakses clipboard otomatis.
3. Review penggunaan execCommand (deprecated).
