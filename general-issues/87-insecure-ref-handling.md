# 87 Insecure Handling of useRef exposing Sensitive DOM Node

## Problem
DOM node sensitif (misalnya form password) diekspos lewat ref.

## Risk
- Node bisa dimanipulasi oleh script luar.

## Example (Before)
```javascript
window.passwordRef = passwordInputRef;
```

## Solution (After)
- Jangan expose ref ke global.
- Gunakan event handler internal.

## How to Avoid
1. Gunakan ref hanya internal.
2. Hapus semua debug expose di production.
3. Audit penggunaan ref di komponen.
