# Issue types and labels

Every repository in jcrenshaw-dev uses the same issue types and labels. This page says what each one means.

Report a security problem privately, never in a public issue.

## Issue types

Every issue gets one type. Pull requests don't have types.

| Type | Use it for |
|---|---|
| Bug | Something behaves differently from what the docs say or the code clearly intends. |
| Enhancement | New behavior, or an improvement to existing behavior. |
| Docs | A documentation change with no code change. |
| Task | Upkeep work like dependency bumps, CI changes and release steps. |

## Severity

Every bug gets one severity label.

| Label | What it means | What happens |
|---|---|---|
| `sev: critical` | It loses or corrupts data, opens a security hole, or the tool won't run at all. There's no workaround. | Other work stops and a patch release ships. |
| `sev: high` | A main feature is broken or gives wrong results, and there's no reasonable workaround. | It's fixed before the next release. |
| `sev: medium` | Something is broken but has a workaround, or the bug is only in a rarely used path. | It's fixed in whichever release it fits. |
| `sev: low` | Cosmetic or minor issues like wording, formatting and small annoyances. | It's fixed when convenient. |

Two rules settle the hard calls:

- A bug that fits two levels gets the higher one.
- A bug that silently gives wrong results ranks one level above the same bug failing with an error, because nobody knows to work around a wrong answer.

There is no priority label. Severity sets the order bugs are fixed in.

The bug form also asks the reporter for an Impact choice: "Stops me working", "Wrong result, I can work around it" or "Minor or cosmetic". Impact is what the bug costs the reporter. Severity is set at triage.

## Status

| Label | What it means |
|---|---|
| `needs-triage` | The issue is new and waiting for its type, plus a severity if it's a bug. It comes off once those are set. |
| `needs-info` | The reporter has been asked a question and the answer hasn't come yet. |

## Closing an issue

A fixed issue closes as completed. A duplicate closes with GitHub's duplicate reason, linked to the issue it duplicates. Every other issue closes as not planned, with one of these labels:

| Label | What it means |
|---|---|
| `wontfix` | The issue is real, but it won't be done. |
| `works-as-intended` | It was reported as a bug, but the behavior is by design. |
| `cant-reproduce` | The steps didn't reproduce it. It's reopened if the reporter brings new information. |
| `invalid` | It's not something the project can act on, like spam, the wrong repo, or a support question. |

## Other labels

| Label | What it means |
|---|---|
| `design` | A design decision or spike, or the design doc that answers one. Used on issues and pull requests. |
| `security` | A Bug that is a security problem. New security problems are reported privately, never in a public issue. |
| `good first issue` | A small, well-defined issue for a first contribution. |
| `help wanted` | Outside help is welcome on this one. |

Dependabot adds `dependencies` and a label for the package ecosystem, such as `rust` or `github_actions`, to the pull requests it opens.
