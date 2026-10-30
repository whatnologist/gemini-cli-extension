# Sync with GitHub

Canonical source: **`integrations/gemini-cli-extension/`** in the private SHOUTapp repo (not this public repo).

**Published here:** https://github.com/whatnologist/gemini-cli-extension

## When to republish

- Any change to **`httpUrl`** in `gemini-extension.json` (listing paths or hostnames)
- User-facing changes in `GEMINI.md` or `README.md`
- Bump **`"version"`** in `gemini-extension.json` for every publish

Server-only MCP changes (tool text, OAuth behavior) do **not** require a repo update — clients read live from `www.getshouting.app`.

## Steps

1. Copy these files from the private repo into this public repo: `gemini-extension.json`, `GEMINI.md`, `README.md`, `LICENSE`, `SYNC.md`.
2. Commit on `main`.
3. Create a GitHub Release tagged **`v{version}`** (e.g. `v1.0.1` when `"version": "1.0.1"`).
4. Keep the GitHub topic **`gemini-cli-extension`** on this repo.
5. Smoke-test: `gemini extensions install https://github.com/whatnologist/gemini-cli-extension` and OAuth sign-in.

Full policy (engineers): `docs/documentation_architecture/MCP_EXTERNAL_INTEGRATIONS.md` in the SHOUTapp repo.
