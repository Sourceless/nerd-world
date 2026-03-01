# Nerd World

A West Marches D&D campaign site, built with Jekyll and hosted on GitHub Pages.

**Live site:** https://Sourceless.github.io/nerd-world/

---

## For Players

- [Quick Start Guide](https://Sourceless.github.io/nerd-world/) — new here? Start here.
- [Session Reports](https://Sourceless.github.io/nerd-world/sessions/) — read about past adventures.
- [Rules](https://Sourceless.github.io/nerd-world/rules/) — house rules and campaign info.
- [Character Creation](https://Sourceless.github.io/nerd-world/characters/) — step-by-step guide.

## For DMs

- [DM Guide](https://Sourceless.github.io/nerd-world/dm-guide/) — how to run a session and post a report.

---

## Posting a Session Report

DMs can post session reports directly through the GitHub web interface — no coding required.

1. Go to the [`_posts/`](_posts/) folder
2. Click **Add file → Create new file**
3. Name it `YYYY-MM-DD-short-title.md` (e.g. `2026-04-19-old-mill-mystery.md`)
4. Paste and fill in the front matter template (see [DM Guide](https://Sourceless.github.io/nerd-world/dm-guide/))
5. Click **Commit new file** — the site updates automatically within ~2 minutes

---

## Technical

Built with [Jekyll](https://jekyllrb.com/) and deployed via [GitHub Actions](.github/workflows/pages.yml). Custom theme, no gem dependencies.

**GitHub Settings required (one-time, repo owner only):**
- Settings → Pages → Source → set to **GitHub Actions**
- Settings → Collaborators → add each DM's GitHub username
