# Deutsch Daily — public source snapshot

A German practice application with original exercises, vocabulary tools and optional server-backed learning history and AI coaching.

This is a sanitized source export, not a backup of a learner account. The introduction is fictional sample text. No learning history, recordings, credentials, database contents or original Git history is included. Publisher exam text/media and generated audio are excluded; official exam rehearsal is disabled. Original practice remains available. See THIRD_PARTY_ASSETS.md.

## Local setup

Requires Node >=22.13 and pnpm 11.25.0. Run `pnpm install --frozen-lockfile`, then `pnpm dev`. Run `pnpm build` to build. The original Sites/Vinext/Cloudflare adapters are retained. Local mock authentication is for loopback development only.

## Deployment boundary

Configure your own Cloudflare D1 database, apply the schema migrations in drizzle/, and provide your own trusted authentication gateway before enabling server endpoints on a public host. app/chatgpt-auth.ts trusts Sites-authenticated headers; an ordinary host must strip user-supplied headers and supply authenticated identity itself. An unconfigured arbitrary host is not a secure production deployment. Configure provider secrets through deployment secret storage, never committed files. Existing live-site state and credentials are not transferable through this export. The template hosting config has no original project ID.

No license grant for original application code is invented by this export. Dependency and third-party content licenses remain applicable.
