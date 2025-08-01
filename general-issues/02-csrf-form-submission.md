# 02 Cross-Site Request Forgery (CSRF) di Form Submission

## Problem
Form atau request AJAX tidak memiliki mekanisme validasi asal request. Hal ini memungkinkan attacker mengirimkan permintaan atas nama user tanpa sepengetahuan mereka.

## Risk
- Perubahan data tanpa izin (contoh: update profil, transaksi)
- Eksekusi aksi kritis oleh attacker (misalnya transfer saldo)

## Example (Before)
```html
<form action="/update-email" method="POST">
  <input name="email" />
  <button type="submit">Submit</button>
</form>
```
*(Tidak ada token CSRF)*

## Solution (After)
```html
<form action="/update-email" method="POST">
  <input type="hidden" name="_token" value="{{ csrf_token() }}">
  <input name="email" />
  <button type="submit">Submit</button>
</form>
```

## How to Avoid
1. Gunakan token CSRF unik per session atau per request.
2. Validasi token CSRF di server sebelum memproses request.
3. Gunakan SameSite cookie untuk meminimalkan risiko.
