# 75 Improper Key Prop Usage causing DOM Reuse

## Problem
Key yang salah menyebabkan DOM elemen reuse tidak semestinya.

## Risk
- Data salah ditampilkan, bisa memanipulasi UI.

## Example (Before)
```jsx
{list.map((item, index) => <div key={index}>{item.name}</div>)}
```

## Solution (After)
```jsx
{list.map((item) => <div key={item.id}>{item.name}</div>)}
```

## How to Avoid
1. Gunakan key unik dan stabil.
2. Jangan gunakan index sebagai key.
3. Audit komponen dengan dynamic list.
