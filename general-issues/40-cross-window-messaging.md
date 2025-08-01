# 40 Cross-Window Messaging tanpa Origin Check

## Problem
`postMessage` menerima pesan dari semua origin tanpa validasi.

## Risk
- Data bocor ke domain tak dipercaya
- Eksekusi perintah dari origin berbahaya

## Example (Before)
```javascript
window.addEventListener('message', (e) => handleMessage(e.data));
```

## Solution (After)
```javascript
window.addEventListener('message', (e) => {
  if(e.origin !== "https://trusted.com") return;
  handleMessage(e.data);
});
```

## How to Avoid
1. Selalu cek origin di event.data.
2. Gunakan whitelist origin.
3. Audit semua penggunaan postMessage.
