
#### 1. View current remotes
Run the command:
```
git remote -v
```

This should show that you have one remote, something like:
```
origin  git@github.com:<your_github_username>/jsconf-asia-2014-git-and-github-workshop.git (fetch)
origin  git@github.com:<your_github_username>/jsconf-asia-2014-git-and-github-workshop.git (push)
```

#### 2. Add `project` as a new remote
```
git remote add project git@github.com:donal/jsconf-asia-2014-git-and-github-workshop.git
```

*Donal says*: There's nothing special about the "origin" name (or the "project"
name) for a remote. "origin" is the default value.

Now run the command:
```
git remote -v
```

This should show that you now have two remotes, something like:
```
origin  git@github.com:<your_github_username>/jsconf-asia-2014-git-and-github-workshop.git (fetch)
origin  git@github.com:<your_github_username>/jsconf-asia-2014-git-and-github-workshop.git (push)
project git@github.com:donal/jsconf-asia-2014-git-and-github-workshop.git (fetch)
project git@github.com:donal/jsconf-asia-2014-git-and-github-workshop.git (push)
```

*Donal asks*: What will happen if you try to push to the `project` remote?

#### 3. Get changes from `project` remote

Assuming there have been new commits on the `project` remote, get them:
```
git fetch project
```

This has pulled the changes down but it hasn't applied them.

#### 4. View all branches

It's worth having a look at all the branches your local repository knows about:
```
git branch -a
```

Now you can see the branches on your remotes.

*Donal says*: These remote branches are pointers to the commit on the remote
(the commit has also been pulled down to your local repository) and they can't
be modified locally.

#### 5. Compare the changes
```
git diff master..project/master
```

*Donal says*: This `git diff` specifies a range, in this case it's the
difference between two branches.

You can also run:
```
git diff --name-only master..project/master
```
To see only the names of files that are different.

#### 6. Merge the changes

Finally you can merge the changes into your `master` branch.
```
git checkout master
git merge project/master
```

And at this point there shouldn't be a conflict.

*Donal says*: You *might* want to merge these changes from `master` into your
feature branch. This would be typical of a long lived branch which you need to
keep up-to-date.

#### 7. Push the changes to your `origin` remote

The changes from the `project` remote are now in your local repository, but
they're not yet in your `origin` (ie. GitHub) remote. So run:
```
git push origin master
```

#### 8. `git pull`

The `git pull` command combines the `git fetch` and `git merge` commands into
one. While this may seem like a useful shortcut, in practice it can cause
problems so it's strongly recommended to avoid using it.
