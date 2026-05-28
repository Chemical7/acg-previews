# ACG previews

Internal mockups of pages destined for `africacommunicationsgroup.com`. Hosted via GitHub Pages.

| Preview | URL |
|---|---|
| Index | https://chemical7.github.io/acg-previews/ |
| Africa Scope · May 2026 | https://chemical7.github.io/acg-previews/africa-scope/may-2026/ |
| ATI · Insights That Move Africa | https://chemical7.github.io/acg-previews/ati/insights-that-move-africa/ |

All pages are `noindex,nofollow`. The repo is public for GitHub Pages free-tier compatibility — content is ACG mockups only, no internal data.

## Source of truth

The canonical authoring lives in the private `materia` repo at `docs/`. This repo mirrors that folder. To update, edit there and copy across:

```powershell
cp -r ../materia/docs/* .
git add .
git commit -m "sync: <what changed>"
git push
```
