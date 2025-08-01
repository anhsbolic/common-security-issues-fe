# 57 Misuse of WebSockets without Origin Validation

## Problem
Menerima koneksi WebSocket dari semua origin.

## Risk
- Data real-time dapat diakses pihak tak berwenang.

## Example (Before)
```javascript
const ws = new WebSocket('ws://example.com/socket');
```

## Solution (After)
- Validasi origin di server.
- Gunakan WSS (WebSocket Secure).

## How to Avoid
1. Gunakan whitelist origin.
2. Terapkan autentikasi untuk koneksi WebSocket.
3. Gunakan TLS (WSS).
