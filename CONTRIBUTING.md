# Contributing to Silo

Thanks for taking the time to improve Silo. The project is a pure front-end AI client that supports the web app, PWA, browser extension, Docker deployment, and multiple model providers.

## Good First Contributions

- Fix provider compatibility issues.
- Improve translations or documentation.
- Add or update OpenAI-compatible provider presets.
- Improve browser extension behavior.
- Add tests or small safety checks around credential handling and provider requests.

## Local Development

Silo uses Node.js and pnpm.

```bash
pnpm install
pnpm run dev
```

Useful commands:

```bash
pnpm run build
pnpm run lint
pnpm run dev:ext
pnpm run build:chrome
pnpm run zip:chrome
```

## Pull Request Checklist

Before opening a pull request, please check:

- The change is focused and has a clear reason.
- The web build still works.
- Browser extension changes are tested with `pnpm run dev:ext` or `pnpm run build:chrome`.
- Provider changes do not log or expose API keys.
- New environment variables are documented in `README.md` and `README_EN.md`.
- Security-sensitive changes mention their impact in the PR description.

## Security-Sensitive Changes

Please be careful with changes touching:

- API key storage or display.
- `localStorage`, `sessionStorage`, or browser extension storage.
- Authorization headers and provider request construction.
- Browser extension permissions, content scripts, and web-accessible resources.
- Build, Docker, release, and store-submission workflows.

For vulnerabilities, follow `SECURITY.md` instead of opening a detailed public issue.
