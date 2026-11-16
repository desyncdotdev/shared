# desyncdotdev/shared

Shared configuration for desyncdotdev repositories.

## Renovate

`default.json` is the org-wide Renovate preset:

- `config:recommended`
- GitHub Actions pinned to digests (`helpers:pinGitHubActionDigests`)
- Semantic commits (`:semanticCommits`), with `ci` as the type for GitHub Actions updates
- A 7-day grace period (`minimumReleaseAge`) before a new release is proposed

To use it, extend it in a repo's `renovate.json` and add repo-specific settings next to it:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>desyncdotdev/shared"]
}
```
