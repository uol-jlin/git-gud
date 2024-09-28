# `HEAD` and `ORIG_HEAD`

## `ORIG_HEAD`
* `ORIG_HEAD` stores the previous state of `HEAD` before executing risky commands.
* It is set by commands that change `HEAD` by more than one commit (e.g. `merge`, `rebase`, `reset`).
  * `ORIG_HEAD` is **not always set**, as it only updates during these specific operations.

## `HEAD@{1}`
* `HEAD@{1}` refers to the last value of `HEAD` before the most recent change.
* Unlike `ORIG_HEAD`, `HEAD@{1}` is always available.
  * It pulls from the reflog specific to the current branch, tracking the changes made to that branch rather than just `HEAD`.

> __Note__: `@` refers to the current commit that `HEAD` points to.
