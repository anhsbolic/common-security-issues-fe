# 32 Using Inline Event Handlers (onclick, onload) yang rentan XSS

## Problem
Menggunakan atribut inline event (onclick, onload) langsung di HTML.

## Risk
- Menyediakan vektor XSS
- Sulit memisahkan logic & view

## Example (Before)
```html
<button onclick="handleClick()">Klik</button>
```

## Solution (After)
```javascript
document.querySelector('button').addEventListener('click', handleClick);
```

## How to Avoid
1. Pisahkan kode JS dari HTML.
2. Gunakan addEventListener atau binding framework.
3. Gunakan linter untuk melarang inline handler.
