
Following on from [branching](branch.md) (in other words, you want to do this
exercise on you `<your_github_username>-asks-a-question` branch):

#### 1. Write a question

In the `student-questions` directory, write a file named
`<your_github_username>-workshop-question.md` and ask a question in that file!

*Donal says*: The file suffix `.md` stands for
[Markdown](http://daringfireball.net/projects/markdown/). The
[writing-on-github](https://help.github.com/categories/writing-on-github/) page
describes how to use Markdown including [GitHub flavoured
Markdown](https://help.github.com/articles/github-flavored-markdown/).

#### 2. Get the status of the file
```
git status
```

Will show that the file is "untracked".

If you want to just see the short version of the git status, run this:
```
git status -s
```

#### 3. View the file differences
```
git diff
```

*Donal asks*: What will this show? Why?

#### 4. Add file to staging
```
git add student-questions/<your_github_username>-workshop-question.md
```

Then:
```
git status
```

Will show that the file is "staged".

#### 5. View the file differences
```
git diff --staged
```

This will show you the patch view of the differences between the **staged**
files and what was in the last commit.

#### 6. Commit your question file
```
git commit -m "add question file"
```

Then:
```
git status
```

Will show that the file is "committed".

*Donal says*: Your file has been committed but only to your local repository.

#### 7. Push your question file to GitHub
```
git push origin <your_github_username>-asks-a-question
```

