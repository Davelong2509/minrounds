# MindRounds GitHub setup

Target: Davelong2509/minrounds
Source commit: b8ad198bd653327b9a667780c59407de392b0839

## Local setup
Use Node.js 24 (minimum 22.13.0) and the pnpm version in package.json. Run `pnpm install --frozen-lockfile`, then `pnpm dev`. Copy `.env.example` to `.env` and supply your own server-side credentials. Read README.md for local D1 setup.

## Runtime
This project uses Vinext, Cloudflare Workers and D1 binding DB, with Supabase over HTTPS. Supabase SQL is in database/migrations; D1 migrations are in drizzle. The live Supabase foundation schema has already been applied. The Google service account must have read access to the parent course folder. Root folder configuration discovers child courses automatically.

Secrets belong in host secret settings, never GitHub source. No runtime secrets, Git history, private materials, learner databases, node_modules or build outputs are included. The export contains a placeholder `.env.example`.

Authentication relies on trusted ChatGPT Sites dispatch headers. Moving to another host requires real authentication and protection against forged identity headers before exposing admin operations. Copying code does not transfer databases, secrets, deployment settings or daily automation. The current live app remains unchanged.

## Upload
Extract and upload the contents, including hidden `.openai/hosting.json` and `.gitignore`. Review existing repository files before replacing anything. Prefer a private repository. Automatic GitHub mirroring is not configured by this export.
