# 12 Mass Assignment di Vuex Store atau Data Binding

## Problem
Menggunakan `Object.assign` untuk update state tanpa validasi field.

## Risk
- Attacker dapat menambahkan field baru (contoh: `isAdmin:true`)
- State korup atau hak akses naik

## Example (Before)
```javascript
mutations: {
  updateUser(state, payload) {
    Object.assign(state.user, payload);
  }
}
```

## Solution (After)
```javascript
mutations: {
  updateUser(state, payload) {
    const allowed = ['name', 'email'];
    allowed.forEach(f => { if(payload[f]) state.user[f] = payload[f]; });
  }
}
```

## How to Avoid
1. Gunakan whitelist field yang boleh diubah.
2. Validasi payload di component sebelum commit.
3. Tambahkan unit test untuk update state.
