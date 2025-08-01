# 08 Improper use of v-html menyebabkan XSS (VueJS)

## Problem
Penggunaan `v-html` pada Vue tanpa sanitasi memungkinkan injeksi script dari input user.

## Risk
- Eksekusi script jahat di browser user
- Pencurian data session

## Example (Before)
```vue
<div v-html="userInput"></div>
```

## Solution (After)
```javascript
import DOMPurify from 'dompurify';
this.safeHtml = DOMPurify.sanitize(userInput);
```
```vue
<div v-html="safeHtml"></div>
```

## How to Avoid
1. Hindari penggunaan `v-html` untuk input user.
2. Gunakan library sanitasi jika harus render HTML.
3. Tambahkan CSP ketat.
