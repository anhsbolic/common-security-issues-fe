# 74 Using useEffect without Cleanup causing Memory Leak

## Problem
useEffect memanggil event listener tanpa cleanup.

## Risk
- Memory leak, potensi race condition yang mempengaruhi security.

## Example (Before)
```javascript
useEffect(() => {
  window.addEventListener('resize', handleResize);
}, []);
```

## Solution (After)
```javascript
useEffect(() => {
  window.addEventListener('resize', handleResize);
  return () => window.removeEventListener('resize', handleResize);
}, []);
```

## How to Avoid
1. Tambahkan cleanup di useEffect.
2. Gunakan ESLint react-hooks untuk memaksa best practice.
3. Audit event listener di komponen.
