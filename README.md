# Mental Melook (MGC)

A mental-health self-monitoring keyboard: an Android IME that passively
tracks typing rhythm, backspace rate, and app-usage patterns on-device, plus
an optional clinician-facing server for those who choose to share their
trends with a hospital/clinician.

## Layout

- `App/` — the Android app (keyboard IME, on-device dashboard, SQLCipher-encrypted local storage). Fully local/offline by default: no account, no network calls, unless a user explicitly opts in via Settings > Clinical Bridge.
  Repo: https://github.com/toonzzzrock/MGC-MeLook
- `Server/` — optional server side of Clinical Bridge: Express/SQLite backend, React clinician/hospital dashboard, Cloudflare Tunnel config. Only relevant to users who opt in on-device; nothing here runs unless someone stands it up.
  Repo: https://github.com/toonzzzrock/MGC-hospital-dashboard
  Quick start: `Server/scripts/dev.sh` (see `Server/README.md`)
- `Documents/` — product pitch and planning docs.

Each of `App/` and `Server/` is its own git repository — they're versioned
and pushed independently.
