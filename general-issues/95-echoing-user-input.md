# 95 Echoing User Input tanpa Escaping {{ $var }}

## Problem
Menampilkan input user tanpa sanitasi.

## Risk
- XSS injection.

## Example (Before)
```blade
{{ $userInput }}
```

## Solution (After)
- Escape input atau gunakan filter sanitasi.

## How to Avoid
1. Jangan tampilkan input mentah.
2. Gunakan package HTML Purifier jika perlu render HTML.
3. Audit semua variable user di view.
