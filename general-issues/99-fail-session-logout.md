# 99 Failure to Invalidate Session Token on Logout

## Problem
Session tidak dihapus ketika logout.

## Risk
- Session hijack.

## Example (Before)
```php
Auth::logout();
```

## Solution (After)
```php
Auth::logout();
$request->session()->invalidate();
$request->session()->regenerateToken();
```

## How to Avoid
1. Invalidate session di logout.
2. Regenerasi token CSRF setelah logout.
3. Audit semua route logout.
