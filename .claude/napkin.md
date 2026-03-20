# Napkin

## Corrections
| Date | Source | What Went Wrong | What To Do Instead |
|------|--------|----------------|-------------------|
| 2026-03-19 | self | Assumed `gh` would target the fork repo automatically and hit `qonversion/web-sdk` instead of `catloafsoft/qonversion-web-sdk`. | Pass `-R catloafsoft/qonversion-web-sdk` on all PR and review commands for this repo. |

## User Preferences
- Use `example.com` domains in tests.

## Patterns That Work
- `gh api graphql` against `reviewThreads` is the reliable fallback when local helper scripts assume the wrong GitHub repo context.

## Patterns That Don't Work
- The bundled PR comment fetch script is not reliable in this fork because it resolves the upstream repo by default.

## Domain Notes
- This SDK now exposes `QonversionConfigBuilder.setApiUrl(...)` for trusted HTTPS proxy routing.
