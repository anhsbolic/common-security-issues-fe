# 86 Static Site Generation (SSG) Caching Sensitive Data

## Problem
Data user spesifik ikut ter-cache di halaman statis.

## Risk
- Halaman cache dibagikan ke user lain.

## Example (Before)
// getStaticProps return data user

## Solution (After)
- Jangan gunakan SSG untuk data user spesifik.

## How to Avoid
1. Gunakan SSG hanya untuk data publik.
2. Gunakan SSR untuk data dinamis.
3. Audit caching strategy.
