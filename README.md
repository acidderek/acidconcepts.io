# acidconcepts.io — deployed build output

This repo is the **deploy artifact** for the public Acid Concepts website,
served by nginx from `/var/www/acidconcepts` on `jobmanager-01`.

- **Source of truth:** private repo `acidderek/acid-concepts-launchpad`, branch `self-host`
  (React 18 + Vite + TypeScript; self-hosted API client — no Supabase/Lovable/Vercel runtime deps)
- **Build:** `npm ci && npm run build` in the source repo, then replace the contents of this repo with `dist/`
- **Backend:** `acidderek/acidconcepts-api` (`acid-api.service`, `/opt/acid-platform` on jobmanager-01)
- **Deploy on box:** `sudo git -C /var/www/acidconcepts pull`

Do not edit files here by hand — they are generated. History note: prior to
2026-10-13 this repo held an April 2026 bundle whose source was a modified
Lovable build (custom Supabase shim); that lineage is superseded by the
`self-host` rebuild.
