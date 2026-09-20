# Security Policy

## Reporting a vulnerability

Do not publish sensitive vulnerability details in a public issue. Use GitHub's private vulnerability reporting if it is enabled for the repository; otherwise contact the repository owner privately.

## Scope

GameBase is a static GitHub Pages site plus a scheduled GitHub Actions workflow that writes `data/player-counts.json`.

Do not include passwords, API keys, access tokens, or other secrets in the repository. GitHub Actions should retain the minimum permissions required by the CCU updater.
