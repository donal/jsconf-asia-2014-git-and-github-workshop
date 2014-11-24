> When I add a folder and a file in that folder, why does git status only show the new folder and not both the new folder and new file?

Great question. This digs down into how Git is structured.

Git stores normal files as `blob` objects, and it stores directories as `tree`
objects. The `tree` objects specify which `blob` objects (ie. files) are in
that directory, and the name of the files (objects are otherwise only
identified by their SHA-1 value).

Therefore until the `tree` object is at least in the staging index (via `git
add`), Git can't know the status of any files in the new directory.

Note that if you create an empty directory and run `git status`, Git will not
recognise it *until* you put a file in there (which is why you'll see the
convention of putting an empty `.keep` file in otherwise empty directories).

