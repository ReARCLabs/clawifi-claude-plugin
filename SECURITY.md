# Security policy

Please do not report security issues in a public issue or Discussion.

For a potentially exploitable issue, use GitHub's private vulnerability reporting on this repository
(Security tab → Report a vulnerability), or email clawifisupport@rearclabs.com. If the issue is safe to disclose,
open a minimal issue without API keys, tokens, or raw logs.

## Supported versions

Security fixes are released for the latest version of this plugin and of the `clawifi` package it pins.

## Handling secrets

The plugin reads your Clawifi API key from the `api_key` user setting, which Claude Code stores as sensitive.
Never commit API keys or paste them into issues.
