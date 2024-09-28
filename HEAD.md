# What is `HEAD`?

`HEAD` is a reference to the commit currently checked out in your Git repo. 

## Symbolic Reference

* `HEAD` is a **symbolic reference**.
  * A symbolic reference is a **reference that points to another reference**, rather than directly to a data object or value.
  * `HEAD` is a symbolic reference that points to a branch reference, which then points to the actual commit object.
    
For example, when you are on the `master` branch, `HEAD` points to the branch reference, which in turn points to the latest commit. 

You can see this in the `.git/HEAD` file:

```bash
$ cat .git/HEAD
ref: refs/heads/master
```
