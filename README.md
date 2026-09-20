# GameBase https://zendex00.github.io/GameBase/

Static Steam current-player tracker for GitHub Pages.

## Upload structure

```text
GameBase.html
README.md
data/player-counts.json
.github/workflows/update-ccu.yml
```

Enable GitHub Pages from the repository's Pages settings using the branch/folder containing `GameBase.html`.

The CCU workflow runs every 5 minutes and updates `data/player-counts.json` from Steam's current-player endpoint.

## Security notes

- No API keys or private credentials are included.
- The workflow uses least-purpose repository write permission and a pinned `actions/checkout` commit.
- The page includes a browser-side Content Security Policy, `no-referrer`, and object/embed restrictions.
- The site is static; no server-side secrets are exposed to visitors.

A browser-delivered site cannot be made literally "hackproof" or "stealproof": visitors necessarily receive HTML, CSS and JavaScript and can inspect or copy it. The package hardens the deployment and removes unnecessary third-party runtime dependencies, but it cannot prevent source copying or attacks against GitHub itself.
