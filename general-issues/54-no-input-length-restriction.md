# 54 No Input Length Restriction on Form Fields

## Problem
Field input tanpa batas panjang, memungkinkan input sangat besar.

## Risk
- Denial of Service di sisi server.
- Buffer overflow di beberapa kasus.

## Example (Before)
```html
<input type="text" name="username">
```

## Solution (After)
```html
<input type="text" name="username" maxlength="50">
```

## How to Avoid
1. Tambahkan batas panjang input.
2. Validasi panjang input di backend juga.
3. Gunakan library validasi untuk standar konsisten.
