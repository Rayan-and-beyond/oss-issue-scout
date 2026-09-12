# Security

oss-issue-scout only reads public GitHub data. It never asks for your password and never needs a privileged token for normal use.

- Do not post personal access tokens, OAuth secrets, or private repository URLs in a public issue. For rate-limit testing, use a throwaway fine-grained token with public-read scope only, and revoke it after.
- Unit tests use mocked GitHub responses and make no network calls. If a smoke test against the real API leaks a token into logs, redact before pasting.
- Report a bug that exfiltrates tokens or writes unexpected data through GitHub private vulnerability reporting. Include the affected version and a redacted reproduction.
- Supported release: the latest `main`.
