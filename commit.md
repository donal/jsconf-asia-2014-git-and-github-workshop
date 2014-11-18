
Following on from [branching](branch.md) (you want to do this exercise on you
`<your_github_username>-asks-a-question` branch):

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

#### 3. Add file to staging
```
git add student-questions/<your_github_username>-workshop-question.md
```

Then:
```
git status
```

Will show that the file is "staged".

#### 4. Commit your question file
```
git commit -m "add question file"
```

Then:
```
git status
```

Will show that the file is "committed".

*Donal says*: Your file has been committed but only to your local repository.

#### 5. Push your question file to GitHub
```
git push origin <your_github_username>-asks-a-question
```

