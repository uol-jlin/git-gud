# Merge Strategies

## Explicit Merge (a.k.a. non fast-forward)
* Creates a **new merge commit**. (this will happen if you use `--no-ff`)

<img src="https://i.sstatic.net/eWwAH.gif" alt="Non fast forward merge" width="600" />

## Fast Forward Merge
* Forward rapidly. Does not create a new commit.

<img src="https://i.sstatic.net/Wne9D.gif" alt="Fast forward merge" width="600" />

## Rebase
* Integrates changes from one branch into another by changing the base of your current branch.
* Creates a **linear commit history**.

<img src="https://i.sstatic.net/4iiIv.gif" alt="Rebase" width="600" />

## Squash
* Combines all commits from a branch into a **single commit** when merging into the main branch.

<img src="https://i.sstatic.net/wzol8.gif" alt="Rebase" width="600" />
