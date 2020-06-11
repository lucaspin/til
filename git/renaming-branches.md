# Renaming branches

Renaming a local branch:

```bash
git checkout <old-name>
git branch -m <new-name>
```

Pushing it to remote:

```bash
git push origin -u <new-name>
git push origin --delete <old-name>
```
