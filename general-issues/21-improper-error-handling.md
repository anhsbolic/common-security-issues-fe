# 21 Improper Error Handling Bocorin Stack Trace

## Problem
Menampilkan error detail (stack trace) langsung di UI, termasuk path file atau konfigurasi internal.

## Risk
- Bocornya struktur aplikasi
- Memberi informasi tambahan untuk attacker melakukan reconnaissance

## Example (Before)
```javascript
try {
  riskyOperation();
} catch (err) {
  document.getElementById('error').innerText = err.stack;
}
```

## Solution (After)
```javascript
try {
  riskyOperation();
} catch (err) {
  console.error('Internal error', err);
  document.getElementById('error').innerText = 'Terjadi kesalahan. Coba lagi.';
}
```

## How to Avoid
1. Tampilkan pesan error generik ke user.
2. Log detail error hanya di console atau server.
3. Matikan debug mode di production.
