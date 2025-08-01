# 45 Insecure Use of Web Workers (script injection di worker)

## Problem
Memuat script worker dari URL dinamis.

## Risk
- Remote code execution di worker context.

## Example (Before)
```javascript
const worker = new Worker(userProvidedUrl);
```

## Solution (After)
- Worker hanya memuat script trusted dari aplikasi.

## How to Avoid
1. Jangan load worker dari input user.
2. Validasi URL worker.
3. Gunakan CSP untuk worker-src.
