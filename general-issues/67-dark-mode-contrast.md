# 67 Failure to Implement Dark Mode Security Considerations (color contrast attacks)

## Problem
Dark mode menyebabkan teks keamanan atau konfirmasi tidak terlihat.

## Risk
- User salah membaca informasi penting (misalnya peringatan keamanan).

## Example (Before)
// Warna teks terlalu mirip dengan background

## Solution (After)
- Uji kontras warna dengan WCAG.

## How to Avoid
1. Pastikan kontras minimal sesuai standar.
2. Uji mode gelap pada semua komponen kritis.
3. Audit aksesibilitas terkait keamanan.
