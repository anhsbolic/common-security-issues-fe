# 73 Storing Tokens in React Context Persisted to LocalStorage

## Problem
Token disimpan di Context lalu diserialisasi ke LocalStorage.

## Risk
- Token bisa diambil dari browser.

## Example (Before)
```javascript
localStorage.setItem('auth', JSON.stringify(contextValue));
```

## Solution (After)
- Simpan token di HttpOnly cookie.
- Jangan persist token di LocalStorage.

## How to Avoid
1. Gunakan memory state untuk token.
2. Pastikan logout menghapus semua session data.
3. Audit context provider yang memuat data sensitif.
