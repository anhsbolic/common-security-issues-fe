# 90 Unsafe Portal Target

## Problem
Portal render ke elemen yang dapat dimanipulasi user.

## Risk
- Manipulasi konten portal.

## Example (Before)
```javascript
ReactDOM.createPortal(<Dialog />, document.getElementById(userInputTarget));
```

## Solution (After)
- Gunakan target portal statis dan aman.

## How to Avoid
1. Jangan gunakan target dinamis dari input user.
2. Audit semua penggunaan portal.
3. Validasi keberadaan target DOM sebelum render.
