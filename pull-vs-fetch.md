# Git Pull vs. Fetch

Remember: `git pull` = `git fetch` + `git merge`

## Git Pull
* `git pull` fetches commits from a remote branch and **automatically merges them** into your current branch.
* It can lead to conflicts if you're not careful.
  * You don't get a chance to review the changes before they are merged.

## Git Fetch + Git Merge
* `git fetch` gathers new commits from the remote branch and **stores them locally without merging**.
* You can see what changes are available without affecting your current work.
  * You can choose to integrate those changes by using `git merge`.

<img src="https://github.com/user-attachments/assets/387a2a45-a7a5-41a2-9bcb-b2aed0de7513" alt="Git pull vs. fetch" width="300" />
