# CODEX — Git Instructions for Claude and Codex

This file tells AI agents how to commit and push changes to this repository.

## Repository

- **GitHub:** https://github.com/Khonikatechnology/WaveCraft
- **Remote:** `git@github.com:Khonikatechnology/WaveCraft.git` (SSH) or `https://github.com/Khonikatechnology/WaveCraft.git` (HTTPS)
- **Branch:** `main`

## What belongs in this repo

This is a **showcase-only** repository. It contains:
- `README.md` — marketing page with screenshots and links to the live site
- `images/` — screenshots of the live WaveCraft app
- `CODEX.md` — this file

**Do NOT push source code.** The actual WaveCraft source code lives at `/Users/shahsharif/ChipVision/WaveCraft` and is deployed via Cloudflare Workers separately.

## How to add or update screenshots

1. Take a new screenshot or copy from `/Users/shahsharif/ChipVision/WaveCraft/scripts/*.png`
2. Copy it to `/tmp/wavecraft-github/images/`
3. Commit and push (see below)

## How to commit and push

### With a GitHub token

```sh
cd /tmp/wavecraft-github

# Stage changes
git add .

# Commit
git commit -m "your message here"

# Push using token
git remote set-url origin https://TOKEN@github.com/Khonikatechnology/WaveCraft.git
git push origin main
```

Replace `TOKEN` with a GitHub personal access token that has `repo` scope.
Generate one at: https://github.com/settings/tokens

### With SSH (if SSH key is set up)

```sh
cd /tmp/wavecraft-github

git remote set-url origin git@github.com:Khonikatechnology/WaveCraft.git
git add .
git commit -m "your message here"
git push origin main
```

## If /tmp/wavecraft-github doesn't exist (fresh machine)

The `/tmp` directory is cleared on reboot. Re-clone the repo:

```sh
git clone https://github.com/Khonikatechnology/WaveCraft.git /tmp/wavecraft-github
cd /tmp/wavecraft-github
```

Then make your changes and push as above.

## How to update the README

Edit `/tmp/wavecraft-github/README.md`, then:

```sh
cd /tmp/wavecraft-github
git add README.md
git commit -m "update README"
git push origin main
```

## Sandbox note

The Apple Claude Code sandbox blocks `github.com` by default. Before pushing, ensure it is in the allowlist:

```
/Users/shahsharif/.claude/apple/dangerous_allowed_domains.csv
```

Add `github.com` if not already present.
