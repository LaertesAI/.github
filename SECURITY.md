# Security

## Supported versions

| Repository | Supported |
|---|---|
| [Penelope](https://github.com/LaertesAI/Penelope) | the newest version on the branch `main` |

Older versions get no fixes.

## Report a weakness

1. Open the repository on GitHub and choose Security, then "Report a vulnerability".
   For Penelope: https://github.com/LaertesAI/Penelope/security/advisories/new
2. Name the version, the command or the tool call, and the smallest steps that show the problem.
3. Replace every real key, token and password in the report with a made-up value.

Write no public issue for a weakness. One developer reads the reports, so no fixed answer time exists.

## What counts

- A secret in a known format that reaches a model, the screen, the transcript or a stored file unmasked.
- A command outside the safe list that runs without a yes under `"run_policy": "safe"`.
- A change to a file that happens without a yes under `"edit_policy": "ask"`.
- A scout that changes a file or runs a command outside the safe list.
- A key that is written to `config.json`, to a session file or to any log.

## What is a known limit

`docs/ROADMAP.md` of Penelope lists these under "Limits known today". They are no weakness in the sense of this file.

- The privacy filter works with fixed rules. A secret without a known prefix and without a key name passes.
- The level `pii` knows e-mail addresses and IBANs only.
- `"run_policy": "all"` and `"edit_policy": "all"` switch the questions off. The user chose that.
- The `claude` command keeps its own record of every session. Penelope does not filter that record.
