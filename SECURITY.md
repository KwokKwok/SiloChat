# Security Policy

Silo is a pure front-end, self-hostable multi-model AI client. It does not provide a central backend proxy for user conversations, but it does handle security-sensitive browser-side workflows such as API key storage, provider configuration, extension behavior, and release artifacts.

## Security Scope

Security reviews are especially valuable in these areas:

- User-provided API keys stored in the browser.
- Optional deployment-provided provider keys, including encrypted paid keys.
- OpenAI-compatible and custom provider request flows.
- Browser extension permissions and content-script behavior.
- PWA and Docker/self-hosted deployment configuration.
- Dependency updates, build workflows, and release artifacts.

## Reporting a Vulnerability

Please do not include active API keys, tokens, private prompts, or other sensitive data in public issues.

If GitHub private vulnerability reporting is available for this repository, please use it. Otherwise, open a minimal public issue that says you would like to report a security issue, without exploit details or secrets, and the maintainer will coordinate a private follow-up channel.

Useful information to include privately:

- Affected version, commit, or release.
- Whether the issue affects the web app, PWA, browser extension, Docker image, or all builds.
- A short reproduction path.
- The security impact, such as credential exposure, unexpected data transmission, permission overreach, or unsafe provider behavior.

## Maintainer Response

The maintainer will triage security reports as soon as practical, prioritize issues that could expose user credentials or browser data, and publish fixes through normal releases when appropriate.

## Notes for Users

Silo stores user-configured keys in the browser. Only use it on devices and browser profiles you trust. If you self-host with provider keys or paid keys, treat those deployment variables as sensitive credentials and rotate them if exposure is suspected.
