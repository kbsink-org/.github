# kbsink-org (GitHub organization profile)

This repository provides the **organization profile README** shown on [github.com/kbsink-org](https://github.com/kbsink-org).

GitHub requires:

- A **public** repo named **`kbsink-org`** (same as the organization)
- The file **`profile/README.md`** in this repo

## Publish

```bash
cd kbsink-org
git init   # if new
git add profile/README.md README.md
git commit -m "docs: add organization profile README"
git remote add origin git@github.com:kbsink-org/kbsink-org.git
git push -u origin main
```

After push, refresh the org **Overview** tab. Optionally **pin** `obsidian-kbsink`, `kbsink-cli`, and `kbsink-org.github.io` on the org page.

## Logo in README

The profile references `https://kbsink-org.github.io/assets/logo.svg`. Deploy [kbsink-org.github.io](https://github.com/kbsink-org/kbsink-org.github.io) first, or copy `logo.svg` into `profile/` here and point the image to:

`https://raw.githubusercontent.com/kbsink-org/kbsink-org/main/profile/logo.svg`

## Not the same as the website repo

| Repo | Purpose | URL |
|------|---------|-----|
| **kbsink-org** (this) | Org profile README on GitHub | `github.com/kbsink-org` |
| **kbsink-org.github.io** | Static site | `https://kbsink-org.github.io/` |
