# 24 Autocomplete Form Aktif pada Field Sensitif (misalnya password)

## Problem
Field password atau data sensitif memiliki autocomplete aktif, menyimpan data di browser.

## Risk
- Data tersimpan di browser shared/public
- Potensi penyalahgunaan oleh orang lain

## Example (Before)
```html
<input type="password" name="pin">
```

## Solution (After)
```html
<input type="password" name="pin" autocomplete="off">
```

## How to Avoid
1. Matikan autocomplete untuk field sensitif.
2. Gunakan password manager integration jika perlu.
3. Review semua form di UI.
