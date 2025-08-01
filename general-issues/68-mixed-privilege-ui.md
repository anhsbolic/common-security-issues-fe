# 68 Mixed Privilege UI Elements (admin & user features in one view)

## Problem
Fitur admin dan user digabung tanpa pemisahan visual atau kontrol yang jelas.

## Risk
- User mengakses fitur admin secara tidak sengaja atau sengaja.

## Example (Before)
// Tombol admin dan user di halaman yang sama

## Solution (After)
- Pisahkan halaman/komponen berdasarkan peran.

## How to Avoid
1. Gunakan role-based access di UI.
2. Tambahkan konfirmasi untuk aksi berisiko.
3. Audit layout halaman dengan peran campuran.
