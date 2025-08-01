# 13 Lack of Rate Limiting di API Calls dari Vue App

## Problem
Tidak ada pembatasan frekuensi request, memungkinkan spam atau brute force.

## Risk
- Denial of Service (DoS) ringan dari sisi client
- API dibanjiri request

## Example (Before)
```javascript
axios.post('/login', credentials);
```

## Solution (After)
```javascript
let last = 0;
function submit() {
  const now = Date.now();
  if(now - last < 3000) return alert("Tunggu sebentar!");
  last = now;
  axios.post('/login', credentials);
}
```

## How to Avoid
1. Gunakan debounce/throttle di UI.
2. Implement rate limit di backend.
3. Tambahkan CAPTCHA untuk aksi berulang.
