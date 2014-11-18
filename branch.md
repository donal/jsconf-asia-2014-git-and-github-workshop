
#### 1. Make sure you're on the `master` branch
```
git checkout master
```

#### 2. Create a new branch
```
git branch <your_github_username>-asks-a-question
```

#### 3. Switch to the new branch
```
git checkout <your_github_username>-asks-a-question
```

*Donal says*: You can do the last two commands in one step:
```
git checkout -b <your_github_username>-asks-a-question
```

#### 4. Write a question

In the `student-questions` directory, write a file named
`<your_github_username>-workshop-question.md` and ask a question in that file!

*Donal says*: The file suffix `.md` stands for
[Markdown](http://daringfireball.net/projects/markdown/). The
[writing-on-github](https://help.github.com/categories/writing-on-github/) page
describes how to use Markdown including [GitHub flavoured
Markdown](https://help.github.com/articles/github-flavored-markdown/).

#### 5. Commit your question file
```
git add student-questions/<your_github_username>-workshop-question.md
git commit -m "add question file"
```

#### 6. Push your question file to GitHub
```
git push origin <your_github_username>-asks-a-question
```

