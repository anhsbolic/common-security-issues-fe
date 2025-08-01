# 18 Misuse of Async/Await menyebabkan Race Condition

## Problem
Memanggil fungsi async bergantung data sebelum promise selesai.

## Risk
- Data salah atau undefined
- Bug keamanan karena alur eksekusi tidak sesuai

## Example (Before)
```javascript
getUser();
getPosts(user.id);
```

## Solution (After)
```javascript
await getUser();
await getPosts(user.id);
```

## How to Avoid
1. Pahami urutan async/await.
2. Gunakan Promise.all hanya untuk task independen.
3. Tambahkan test async di unit test.
