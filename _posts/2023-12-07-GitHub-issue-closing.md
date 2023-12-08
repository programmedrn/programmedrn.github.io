---
title: Github Issues Closing from Commits
categories:
- tip
- git
- commit
excerpt: |
  Github Issues can be closed from committing, when there are issue number and keyword for closing.
feature_text: |
  ## Github Issue Closing from Commits
  Github Issues can be closed from committing, when there are issue number and keyword for closing.
feature_image: "/FirstBlog/assets/insertedImg/2023-12-07-GitHub-issue-closing/githubImage.png"
# image: "/FirstBlog/assets/insertedImg/2023-12-07-GitHub-issue-closing/githubImage.png"
# aside: true
# heads: true
---

## Goal of this article
Github issuses can be closed by commit. It can be achived by two things in your commit message.
1. #{an issuse number}
1. a closing keyword

## Test1

### sub 1
### sub 2

## test3
### sub 4

### sub 5

### Issue Number
You can check your issue's number from issues page of your repository. Check below.

{% include figure.html image="/FirstBlog/assets/insertedImg/2023-12-07-GitHub-issue-closing/issue_examples.png" width="200em"  %}

For each issues, there are numbers below the name of one. For example, I have 6 issues and the first issue's number from the image is 6. 

### Closing Keywords

You may find closing keywords from below. You can use one of these.

- close
- closes
- closed
- fix
- fixes
- fixed
- resolve
- resolves
- resolved

As you can see, the points are 'close, fix, resolve'. I think this is becuase there are three types of Github Issues: **Bug report, Feature request, Help request**'. So each can be fixed, closed or resolved.

### Usage

You can commit like this.

```bash
git commit -m "resolved some issues. #4, #5"
```

As you can see, you may close several issues at the same time.

### Advanced

You also can link an issue from other repository by

```bash
git commit -m "resolved owner/repositoryName#52"
```

### References

[Linking a pull request to an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue/ "Linking a pull request to an issue")