# How to delete a file from a Git repo?

(1) Use `git rm` if you want to delete the file from **both the Git repository and your file system**.

```bash
git rm file1.txt
git commit -m "remove file1.txt"
```

(2) Use `git rm --cached` if you only want to remove the file **from the Git repository** but keep it on your system.

```bash
git rm --cached file1.txt
git commit -m "remove file1.txt"
```

And to push changes to remote repo:

```bash
git push origin branch_name
```
