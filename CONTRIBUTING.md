# Contributing

Thanks for helping keep this list honest — credit programs change amounts, tiers, and eligibility constantly, and PRs are the only way this list stays trustworthy.

## What makes a good entry

- **Notable**: a real, running program with genuine startup value — not a one-off promo or a landing page that collects emails.
- **A verified official URL**: the program's own page. Links must resolve for humans (not just bots).
- **A one-line description**: what the program offers and who it's for, in plain language.
- **No invented amounts**: credit amounts change often. Quote the figure the official page shows, and flag it with `verified` / `verified_date` in the JSON. If you couldn't verify the figure yourself, set `verified: false` and say why in `notes` — unverified entries are welcome as stubs, honestly flagged.
- **A status tag when it's not plain active**: `(beta)`, `(legacy)`, `(sunsetting)`, `(acquired by X)` — with the detail logged in [docs/status-changes.md](docs/status-changes.md).

## Checklist for a PR

1. Add the entry to the right section of `README.md`, keeping alphabetical-ish grouping sensible (sections are roughly ordered by prominence, not strictly alphabetical).
2. Add the matching object to `data/startup-credits.json` with fields: `id` (slug), `name`, `url`, `category` (one of `cloud_infra`, `ai_api`, `software_devtools`, `cash_grants`), `amount`, `description`, `eligibility`, `verified` (boolean — true **only** if you personally checked the official program page), `verified_date` (`YYYY-MM-DD`), `notes`.
3. If the entry changes a status (shutdown, acquisition, sunset), update `docs/status-changes.md` too.
4. Make sure CI passes: JSON validation and the lychee link check run on every PR.

## Updating or removing entries

Programs that shut down, get acquired, or sunset should be **updated, not deleted** — the status log is part of the list's value. Only remove entries that were never real (dead on arrival, renamed with a redirect in place).

## License of contributions

By contributing, you agree your contributions are released under the repository's [MIT License](LICENSE).
