# harvest-xyz-snapshot

Public snapshot feed from [digit-life/harvest](https://github.com/digit-life/harvest) for [awesome-xyz](https://github.com/digit-life/awesome-xyz) (#116 / harvest #358).

- **Writer:** harvest `awesome-project` only
- **Reader:** xyz CI on public runners (`git fetch`, no LAN)
- **Layout:**
  - `manifest.json` — `snapshotId`, `exportVersion`, `generatedAt`, per-site `siteSpecHash`
  - `sites/<appId>/candidates.json` — xyz `candidatesFileSchema` (evidence + `aiReview`)
- **Tags:** `snapshot-<ISO>` with colons stripped (`snapshot-2026-08-20T023000.000Z`) so git refs stay valid. Old tags remain readable if harvest stops updating.

Do not open PRs that change snapshot files. Human review / `registry.json` stays in xyz.
