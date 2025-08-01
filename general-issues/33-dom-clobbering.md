# 33 DOM Clobbering melalui ID & Name Conflict

## Problem
ID atau name tertentu dapat menimpa properti DOM global.

## Risk
- attacker dapat injeksi elemen dengan id global tertentu (misal `id=form`)
- Script terganggu atau berperilaku aneh

## Example (Before)
```html
<form id="form"></form>
<script>
if(form) form.submit();
</script>
```

## Solution (After)
```javascript
const formEl = document.getElementById('form');
if(formEl) formEl.submit();
```

## How to Avoid
1. Hindari rely pada ID sebagai variable global.
2. Gunakan querySelector atau getElementById dengan scope.
3. Audit ID yang digunakan di template.
