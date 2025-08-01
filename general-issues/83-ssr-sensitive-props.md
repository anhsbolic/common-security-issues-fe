# 83 Server-side Rendering (SSR) leaking Sensitive Props

## Problem
Props sensitif ditulis langsung ke HTML output.

## Risk
- Data sensitif muncul di source HTML.

## Example (Before)
// getServerSideProps return full token

## Solution (After)
- Filter props sebelum render.
- Kirim hanya data yang dibutuhkan ke browser.

## How to Avoid
1. Jangan kirim token atau credential di SSR props.
2. Gunakan API protected di client setelah render.
3. Audit output HTML SSR.
