# Step 1

### create main branch locally, taking the history from master

```code
git branch -m master main
```

# Step 2

### push the new local main branch to the remote repo (GitHub)

```code
git push -u origin main
```

# Step 3

### switch the current HEAD to the main branch

```code
git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main
```

# Step 4

### change the default branch on GitHub to main

```code
aws codecommit update-default-branch --repository-name MyDemoRepo --default-branch-name MyNewBranch
```

# Step 5

### delete the master branch on the remote

```code
git push origin --delete master
```
