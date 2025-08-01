# 72 Leaking Sensitive State to Window Object

## Problem
Menyimpan state sensitif ke window global.

## Risk
- Data mudah diakses oleh script lain atau extension.

## Example (Before)
```javascript
window.appState = store.getState();
```

## Solution (After)
- Jangan expose state ke window.
- Gunakan context atau Redux store internal.

## How to Avoid
1. Batasi debug hanya di dev.
2. Hindari log state sensitif.
3. Gunakan env flag untuk mode debug.
