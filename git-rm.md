# How to Delete a File from a Git Repository

## 1. Remove a file from both the Git repository and your local file system:

Use `git rm` command:

```bash
git rm file1.txt
git commit -m "Remove file1.txt"
```

## 2. Remove a file only from the Git repository, but keep it on your local system:

Use use the `--cached` option:

```bash
git rm --cached file1.txt
git commit -m "Remove file1.txt from Git, but keep locally"
```

## 3. Push your changes to the remote repository:

After committing, push the changes to the desired branch:

```bash
git push origin branch_name
```

## Recursively Remove Files

To recursively remove all tracked files from the Git repo (without deleting them locally), run:

```bash
git rm -r --cached .
git commit -m "Remove all tracked files from Git, keep locally"
git push origin branch_name
```

<img src="https://github.com/user-attachments/assets/c664de35-fbac-449f-8310-9ac552f1ad2a" alt="git rm -r --cached ." width="600" />
