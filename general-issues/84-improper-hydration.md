# 84 Improper Hydration causing Flash of Sensitive Data

## Problem
Data sensitif muncul sekejap sebelum React menginisialisasi.

## Risk
- Informasi sensitif bisa dilihat di DOM awal.

## Example (Before)
```html
<div id="root">{JSON.stringify(user)}</div>
```

## Solution (After)
- Render placeholder, ambil data setelah autentikasi selesai.

## How to Avoid
1. Jangan pre-render data sensitif.
2. Gunakan placeholder di hydration.
3. Audit DOM awal di production.
