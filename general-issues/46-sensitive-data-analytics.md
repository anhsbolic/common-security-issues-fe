# 46 Sensitive Data in Analytics Event (PII dikirim ke tracking service)

## Problem
Mengirim data PII (misalnya email, nomor KTP) ke service analytics pihak ketiga.

## Risk
- Pelanggaran privasi.
- Potensi kebocoran data ke pihak tidak berwenang.

## Example (Before)
```javascript
analytics.track('signup', { email: user.email });
```

## Solution (After)
- Kirim event tanpa data PII atau anonimisasi data.

## How to Avoid
1. Hindari mengirim PII ke analytics.
2. Gunakan metode hashing/anonymization.
3. Review semua event tracking.
