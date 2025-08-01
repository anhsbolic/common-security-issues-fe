# 62 Unrestricted Push Notification Permission Requests

## Problem
Aplikasi meminta izin push notification tanpa konteks atau terlalu awal.

## Risk
- User menjadi korban phishing melalui notifikasi.
- Meningkatkan risiko social engineering.

## Example (Before)
```javascript
Notification.requestPermission();
```

## Solution (After)
- Tampilkan konteks mengapa izin dibutuhkan sebelum memanggil requestPermission.

## How to Avoid
1. Jangan minta izin tanpa konteks.
2. Hanya minta izin ketika benar-benar dibutuhkan.
3. Audit UX terkait push notification.
