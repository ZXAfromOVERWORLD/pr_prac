
So First Step in PR submission is creating a fork
1) Create fork of repo;
2) Clone Repo
3) git remote add upstream git.link
4) ***Important Never Work On Main*** create a separate branch feature/name
5) Make Changes
6) Push to fork checkout point 7 first
```
git checkout main
git fetch upstream
git merge upstream/main
git push origin main
```
7) Keep your fork up to date before any push to fork
8) Merging is messier so people use rebase
9) git rebase -i HEAD~3
This is how to squash Commits together



BEFORE CREATING A PR
```
# Step 1: Update branch
git fetch upstream
git rebase upstream/main

# Step 2: Clean commits
git rebase -i HEAD~N   # squash commits

# Step 3: Push (force required after rebase)
git push origin branch-name --force
```


FINAL FLOW

```
# sync fork
git fetch upstream
git checkout main
git merge upstream/main

# create branch
git checkout -b fix/login-bug

# work
git add .
git commit -m "Fix login validation bug"

# push
git push origin fix/login-bug

```

