# 38 Using Outdated Polyfills yang Rentan

## Problem
Polyfill usang memiliki bug keamanan.

## Risk
- Bisa dieksploitasi attacker via polyfill vulnerability

## Example (Before)
// menggunakan core-js versi lama

## Solution (After)
// update core-js atau library polyfill terbaru

## How to Avoid
1. Audit versi polyfill secara berkala.
2. Gunakan tool dependabot atau npm audit.
3. Hapus polyfill tidak digunakan.
