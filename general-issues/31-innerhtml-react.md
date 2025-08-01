# 31 Using InnerHTML secara langsung di Framework lain (React dangerouslySetInnerHTML)

## Problem
Menggunakan `dangerouslySetInnerHTML` di React tanpa sanitasi input.

## Risk
- XSS jika input berasal dari user
- Eksekusi script tidak sah

## Example (Before)
```jsx
<div dangerouslySetInnerHTML={{ __html: userInput }} />
```

## Solution (After)
```jsx
import DOMPurify from 'dompurify';
<div dangerouslySetInnerHTML={{ __html: DOMPurify.sanitize(userInput) }} />
```

## How to Avoid
1. Hindari dangerouslySetInnerHTML kecuali benar-benar diperlukan.
2. Selalu gunakan sanitasi sebelum render HTML.
3. Tambahkan Content Security Policy (CSP).
