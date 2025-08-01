# 71 dangerouslySetInnerHTML tanpa Sanitasi (React)

## Problem
Menggunakan `dangerouslySetInnerHTML` tanpa pembersihan konten.

## Risk
- XSS langsung dari input user.

## Example (Before)
```jsx
<div dangerouslySetInnerHTML={{ __html: userContent }} />
```

## Solution (After)
```jsx
import DOMPurify from 'dompurify';
<div dangerouslySetInnerHTML={{ __html: DOMPurify.sanitize(userContent) }} />
```

## How to Avoid
1. Hindari dangerouslySetInnerHTML jika tidak perlu.
2. Gunakan library sanitasi seperti DOMPurify.
3. Audit semua komponen yang render HTML mentah.
