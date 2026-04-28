# FEBQI Lab Homepage

Homepage of the **FEBQI (Floating Electrons and Beyond for Quantum Information) Lab**, led by Erika Kawakami at the RIKEN Center for Quantum Computing.

- **Live site (production):** https://febqi.github.io/lab-hp/
- **Live site (development):** separate staging site (URL not listed here)

## Development workflow

1. Edit files in this repository (`erikawa-e/lab-hp`)
2. Push to verify: `git push`
3. When ready to publish to `febqi/lab-hp`: trigger the **Mirror to febqi/lab-hp** workflow from the [Actions tab](https://github.com/erikawa-e/lab-hp/actions/workflows/mirror-to-febqi.yml)

### Mirror workflow setup

The workflow (`.github/workflows/mirror-to-febqi.yml`) pushes `main` from `erikawa-e/lab-hp` to `febqi/lab-hp` on demand (manual trigger only).

**Required secret in `erikawa-e/lab-hp`:**

| Secret name | Value |
|---|---|
| `FEBQI_TOKEN` | Classic Personal Access Token with `repo` + `workflow` scopes, belonging to an account with write access to `febqi/lab-hp` |

To regenerate: [github.com/settings/tokens](https://github.com/settings/tokens) → Generate new token (classic) → check `repo` and `workflow` → save as `FEBQI_TOKEN` in [repository secrets](https://github.com/erikawa-e/lab-hp/settings/secrets/actions).

## Built with

[multi-language-al-folio](https://github.com/george-gca/multi-language-al-folio) — a multilingual Jekyll theme for academics. Hosted on GitHub Pages.

## Languages

English (`_pages/en-us/`, `_posts/en-us/`, `_data/en-us/`) and Japanese (`_pages/ja/`, `_posts/ja/`, `_data/ja/`).
