
#### 1. Make sure you're on the `master` branch
```
git checkout master
```

#### 2. View your branches
```
git branch
```

#### 3. Delete a branch

Assuming there's a branch, delete it:
```
git branch -d <your_github_username>-asks-a-question
```

If it's fully merged into `master` then it will be deleted. If not, you'll get
an error like:
```
error: The branch '<your_github_username>-asks-a-question' is not fully merged.
If you are sure you want to delete it, run 'git branch -D <your_github_username>-asks-a-question'.
```

*Donal says*: Be *very* careful using the `branch -D` command as you can lose
commits (actually, it *maybe* possible to retrieve them by inspecting the
`git reflog`).

