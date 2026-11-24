# Contributing to Laertes

These rules hold for every public repository of Laertes that has no CONTRIBUTING file of its own. Today that is
[Penelope](https://github.com/LaertesAI/Penelope). One developer maintains the code, so an answer can take days.

## Before you write code

1. Search the open issues of the repository.
2. Open an issue for a bug or an idea and wait for one answer. A pull request without an issue may be closed.
3. Read `docs/ROADMAP.md` of the repository. It lists every known limit and every planned part.

## What a change needs

| Rule | Check |
|---|---|
| One pull request holds one change. | The title names it in one sentence. |
| The build is clean. | `cargo build --release` ends without a warning. |
| Every test passes. | `cargo test` in `cli/`, no test calls a model. |
| A new part has a test. | One unit test without a model call. |
| A number names its run. | Model, date and count of runs stand next to it. |
| A changed command, key or setting is in the README. | The diff holds both files. |
| No secret is in the diff. | No key, token, password or private address. |

## Rules for tools in Penelope

1. The output a model reads passes the privacy filter.
2. A tool that changes something outside `.penelope` asks first, unless a policy setting says otherwise.
3. The first line of a result says what happened in under 160 characters.
4. A refusal starts with `NOT` and names the reason and the way out.

## Text

- Code, comments, commit messages and documents are English.
- Sentences are short and name numbers and files.
- A claim that was not measured says so.
- A commit message is one sentence that says what changed.

## Licence

A contribution is published under the licence of its repository. Penelope uses the MIT licence.
