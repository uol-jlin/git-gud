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

## Example of Using `HEAD@{x}`

`HEAD@{x}` is useful for referencing a specific state from your reflog history. For example:

### To reset your branch to the state before the most recent commit:

```bash
git reset --hard HEAD@{1}
```

This will reset the current branch to the commit before the most recent `HEAD` change, which could be from a commit, merge, or rebase.

### To checkout the state of the branch two changes ago:

```bash
git checkout HEAD@{2}
```

This is useful if you want to explore or inspect how the branch looked two changes prior.
