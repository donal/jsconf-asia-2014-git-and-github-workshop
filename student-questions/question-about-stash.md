> What will happen if the code is stash pop back to the master and there is conflicts?

Then you'll get a merge conflict and the stashed changes won't be applied until
you resolve the conflict (or you can always `git merge --abort` to ensure the
changes are not applied).

> How to fix them?

Just fix them in the normal way you'd handle a merge conflict - decide which
are the final changes you want, then `git add` and `git commit` those files.
