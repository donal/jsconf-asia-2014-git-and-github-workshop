
#### 1. Make sure you're on the `master` branch
```
git checkout master
```

#### 2. Edit the `README.md` file

On line 2, which currently reads:
```
Workshop exercises and outstanding student questions for JSConf Asia 2014.
```
Change the year to "2015".

#### 3. Get changes from `project` remote

Assuming there have been new commits on the `project` remote, get them:
```
git fetch project
```

#### 4. Try to merge the changes

You can try merge the changes into your `master` branch.
```
git merge project/master
```

At this point there *should* be a conflict:
```
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
```

#### 5. Run `git status`

Running:
```
git status
```
Will show you which file(s) have conflicts.

#### 6. Fix conflicts

Edit the `README.md` file. You'll see something like:
```
<<<<<<< HEAD
Workshop exercises and outstanding student questions for JSConf Asia 2015.
=======
Workshop exercises and outstanding student questions for JSConf Asia 2013.
>>>>>>> origin/master
```

It's up to you to decide what is the correct version that you want to keep (or
perhaps just change it back to "2014").

Save and exit the file once you've cleaned up the conflict.

#### 7. Commit
If you run `git status` again you'll see the same error. You still have to:
```
git add README.md
```

Then commit it. If you commit it like this:
```
git commit --verbose
```
It will open your `$EDITOR` editor, eg. vim, with a pre-prepared "merge
conflict" commit message.

