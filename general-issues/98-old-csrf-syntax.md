# 98 Using Old @csrf Directive Syntax Incorrectly

## Problem
Salah menggunakan directive CSRF atau lupa menambahkan.

## Risk
- Form tanpa token CSRF.

## Example (Before)
```blade
<form>@csrf_token</form>
```

## Solution (After)
```blade
<form>@csrf</form>
```

## How to Avoid
1. Gunakan syntax terbaru Laravel.
2. Audit semua form view.
3. Gunakan middleware default.
