# Orchard Development Workflow

This checkout is the local WSL development repo for Orchard.

## Remotes

- `origin`: Orchard fork at `https://github.com/lisarodgers/orchard.git`
- `upstream`: original ezBookkeeping repo at `https://github.com/mayswind/ezbookkeeping.git`

## Everyday Work

Use `main` for the current Orchard base unless a feature branch is needed.

```bash
git status
git pull
git push
```

By default, local `main` tracks `origin/main`.

## Pulling Upstream Fixes

Fetch upstream intentionally:

```bash
git fetch upstream
```

Preview upstream changes before merging:

```bash
git log --oneline main..upstream/main
git diff main..upstream/main
```

Merge upstream fixes only when ready:

```bash
git merge upstream/main
```

Then push the updated Orchard fork:

```bash
git push origin main
```

## Production Boundary

Mercury is production only. Do not edit the running production install directly.

Orchard development happens locally in WSL under:

```text
/home/stargazer/projects/orchard
```
