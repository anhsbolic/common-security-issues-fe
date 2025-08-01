# 66 No Session Timeout Indicator on Client UI

## Problem
UI tidak menunjukkan sesi hampir habis atau tidak pernah logout otomatis.

## Risk
- User tetap login di perangkat publik.
- Risiko session hijack.

## Example (Before)
// Tidak ada mekanisme timeout

## Solution (After)
- Tambahkan timer sesi dan dialog peringatan.

## How to Avoid
1. Tampilkan countdown sesi.
2. Implementasikan logout otomatis setelah idle.
3. Audit UX sesi pada aplikasi.
