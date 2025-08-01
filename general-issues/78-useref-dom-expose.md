# 78 Improper useRef exposing DOM nodes

## Problem
Mengexpose DOM node langsung dari useRef ke window/global.

## Risk
- Script eksternal bisa memanipulasi DOM.

## Example (Before)
```javascript
window.node = ref.current;
```

## Solution (After)
- Jangan expose ref DOM ke global.
- Gunakan mekanisme internal React.

## How to Avoid
1. Gunakan ref hanya dalam komponen.
2. Jangan log ref DOM ke console di production.
3. Audit penggunaan useRef.
