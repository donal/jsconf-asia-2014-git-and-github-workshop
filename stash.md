
#### 1. Edit a file

Edit your `student-questions/<your_github_username>-workshop-question.md`, make
a change, and quit the file.

#### 2. Check `git status`
```
git status
```
And you'll see that file under the "Changes not staged for commit" title.

#### 3. Stash the changes
```
git stash
```

Now run:
```
git status
```
And you'll see that there is "nothing to commit, working directory clean".

#### 4. View the stash
```
git stash list
```

#### 5. Apply the stash
```
git stash apply
```
Or:
```
git stash pop
```

Now run:
```
git status
```
And you'll see that file you edited is again listed under the "Changes not
staged for commit" title.

*Donal says*: The stash is a stack. You can `git stash pop` the top item, but
you can also `git apply` a specific item in the stash. You can change branches
then `git apply` a stash so be careful as this may cause merge conflicts.
