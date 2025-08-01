# 81 Custom Hooks exposing Sensitive Info through Return Values

## Problem
Custom hook mengembalikan informasi sensitif yang bisa digunakan sembarang komponen.

## Risk
- Data sensitif bocor jika hook dipakai di tempat yang salah.

## Example (Before)
```javascript
function useUser() {
  return { token: localStorage.getItem('token'), user: getUser() };
}
```

## Solution (After)
- Jangan expose token ke UI langsung.
- Return hanya data non-sensitif.

## How to Avoid
1. Audit semua custom hook yang memproses data sensitif.
2. Gunakan context terisolasi.
3. Jangan persist data sensitif ke state global.
