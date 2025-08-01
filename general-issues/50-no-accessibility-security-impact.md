# 50 No Accessibility Consideration yang Mengakibatkan Security Impact

## Problem
Fitur aksesibilitas diabaikan, menyebabkan user menggunakan bypass atau cara tidak aman.

## Risk
- ARIA skip link digunakan untuk melewati langkah keamanan UI.
- Potensi misuse oleh user yang butuh aksesibilitas.

## Example (Before)
// Tidak ada fokus management, user lompat langsung ke aksi berbahaya.

## Solution (After)
- Tambahkan ARIA role dan fokus management dengan benar.

## How to Avoid
1. Perhatikan aksesibilitas di desain UI.
2. Uji dengan user screen reader.
3. Pastikan kontrol keamanan tidak dapat dilewati.
