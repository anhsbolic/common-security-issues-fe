# 42 Ignoring Tabnabbing Risk pada External Link (target="_blank" tanpa rel="noopener")

## Problem
Link dengan target="_blank" tanpa rel="noopener" memungkinkan halaman tujuan mengontrol window opener.

## Risk
- Phishing dengan mengganti tab asli.
- Eksekusi script jahat di tab induk.

## Example (Before)
```html
<a href="https://external.com" target="_blank">Link</a>
```

## Solution (After)
```html
<a href="https://external.com" target="_blank" rel="noopener noreferrer">Link</a>
```

## How to Avoid
1. Selalu tambahkan rel="noopener noreferrer".
2. Audit semua link eksternal.
3. Gunakan linting rules untuk memaksa rel attribute.
