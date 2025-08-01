# 77 Default Error Boundaries Leaking Sensitive Error Details

## Problem
Error boundary menampilkan pesan lengkap dengan stack trace.

## Risk
- Bocor informasi internal aplikasi.

## Example (Before)
```jsx
<ErrorBoundary>{children}</ErrorBoundary>
```

## Solution (After)
- Ganti fallback UI dengan pesan umum.
- Log detail hanya di server.

## How to Avoid
1. Jangan tampilkan stack trace ke user.
2. Audit error boundary fallback.
3. Gunakan mode production React.
