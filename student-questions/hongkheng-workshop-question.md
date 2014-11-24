> What is the best way to update your feature branch that has been pushed when it is out of date with the master branch?

I would do this on my local repository. Something like:

1. `git checkout feature-branch`
1. `git merge master`
1. Deal with any conflicts.
1. `git push origin feature-branch`

Now the remote copy of your feature branch (as well as your local) have been
updated with changes that were in `master`.
