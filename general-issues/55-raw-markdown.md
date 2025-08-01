# 55 Rendering Raw Markdown without Sanitization

## Problem
Markdown ditampilkan tanpa proses sanitasi.

## Risk
- XSS via tag HTML di dalam markdown.

## Example (Before)
```javascript
<div id="preview"></div>
preview.innerHTML = markdownInput;
```

## Solution (After)
```javascript
import DOMPurify from 'dompurify';
preview.innerHTML = DOMPurify.sanitize(markdownInput);
```

## How to Avoid
1. Gunakan library sanitasi sebelum render markdown.
2. Tambahkan CSP ketat untuk memblokir inline script.
3. Jangan izinkan HTML mentah dalam markdown jika tidak perlu.
