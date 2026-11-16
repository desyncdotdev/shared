# desyncdotdev/renovate-config

The org-wide Renovate preset for desyncdotdev repositories, in `default.json`:

- `config:recommended`
- GitHub Actions pinned to digests (`helpers:pinGitHubActionDigests`)
- Semantic commits (`:semanticCommits`), with `ci` as the type for GitHub Actions updates
- A 7-day grace period (`minimumReleaseAge`) before a new release is proposed

To use it, extend it in a repo's `renovate.json` and add repo-specific settings next to it:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>desyncdotdev/renovate-config"]
}
```

This repo is public on purpose: Renovate does not let a public repository extend a preset from a private one, and some desyncdotdev repositories are public. Keep anything private out of it.
