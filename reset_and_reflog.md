
#### 1. Make sure you're on the `master` branch
```
git checkout master
```

#### 2. Create a new branch and switch to it
```
git checkout -b try-reset
```

#### 3. Create and commit reset1.md file

Create a file named "reset1.md", put some text in it and save it.
```
git add reset.md
git commit -m "add reset1 file"
```

#### 4. Create and commit reset2.md file

Create a file named "reset2.md", put some text in it and save it.
```
git add reset.md
git commit -m "add reset2 file"
```

#### 5. Create and commit reset3.md file

Create a file named "reset3.md", put some text in it and save it.
```
git add reset.md
git commit -m "add reset3 file"
```

#### 6. View commit log
```
git lg
```

#### 7. Move HEAD back one commit
```
git reset --soft HEAD^
```
Or:
```
git reset --soft HEAD~1
```

Now run:
```
git lg
```
And:
```
git status
```

#### 8. Recommit the file
```
git commit -m "add reset3 file"
```

#### 9. Move HEAD back two commits and update staging to this
```
git reset HEAD~2
```

Now run:
```
git lg
```
And:
```
git status
```

#### 10. Stage and recommit the files
```
git add reset2.md
git commit -m "add reset2 file"
git add reset3.md
git commit -m "add reset3 file"
```

#### 11. Reset everything back one commit
```
git reset --hard HEAD^
```

Now run:
```
git lg
```
And:
```
git status
```

*Donal asks*: What happens if you do a `git reset --hard` when there is an
untracked file?

#### 12. Recover commit from reflog

The reflog shows all commits that were done against HEAD.
```
git reflog
```

Using the SHA value (you can also use the `HEAD@{x}` value) move HEAD again to
recover the lost commit:
```
git reset --hard <SHA>
```

