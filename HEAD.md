# What is `HEAD`?

`HEAD` is a reference to the commit currently checked out in your Git repo. 

## Symbolic Reference

* `HEAD` is usually a **symbolic reference**.
  * A symbolic reference is a **reference that points to another reference**, rather than directly to a data object or value.
  * `HEAD` is a symbolic reference that points to a branch reference, which then points to the actual commit object.
    
For example, when you are on the `master` branch, `HEAD` points to the branch reference, which in turn points to the latest commit. 

You can see this in the `.git/HEAD` file:

```bash
$ cat .git/HEAD
ref: refs/heads/master
```

## Detached `HEAD` State

In some cases, `HEAD` directly **points to a specific commit** instead of a branch.

This is known as the detached `HEAD` state, which can occur when you check out:

* A specific commit (e.g., `git checkout <commit-hash>`)
* A tag (e.g., `git checkout v1.0.0`)
* A remote branch without creating a local tracking branch

In detached `HEAD` state, the `.git/HEAD` file shows the SHA-1 hash of the commit:

```bash
$ cat .git/HEAD
5f47d61c3e...
```

<img src="https://github.com/user-attachments/assets/9d75d422-8af8-458e-a88a-873b121d2558" alt="HEAD as symbolic ref vs. detached HEAD state" width="600" />
