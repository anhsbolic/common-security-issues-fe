# 48 Insecure Local Development Config Pushed ke Repo (contoh: .env.dev dengan secrets)

## Problem
Config lokal dengan secret ikut terpush ke repo publik.

## Risk
- Secrets bocor (API key, credential database).

## Example (Before)
// .env.dev committed ke repo

## Solution (After)
- Tambahkan .env ke .gitignore.
- Rotasi secrets yang sudah terlanjur bocor.

## How to Avoid
1. Jangan commit config lokal dengan secret.
2. Gunakan vault atau secret manager.
3. Audit repo untuk file sensitif.
