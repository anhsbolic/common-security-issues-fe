# 89 Weak Default Value in React Context

## Problem
Context memiliki default value yang tidak aman (misalnya user admin).

## Risk
- Komponen fallback bisa pakai default tidak benar.

## Example (Before)
```javascript
const UserContext = React.createContext({ role: 'admin' });
```

## Solution (After)
- Default value harus null atau state aman.

## How to Avoid
1. Gunakan default minimal (null).
2. Inisialisasi nilai context di provider.
3. Audit semua context default.
