---
title: "how to manually deploy to @heroku from @bitbucket @github or @gitlab repos"
date: 2021-01-22
categories: 
  - "vizz"
---

how to manually deploy to @heroku from @bitbucket @github or @gitlab repos

- clone your repo
- add a heroku git remote to your @bitbucket @github or @gitlab repo
- push to your repo
- push to your heroku git remote

example

```
CLONE YOUR REPO 

$ git clone yourrepo
$ cd yourrepo
$ heroku create (git:remote ?)

CHECK YOU HAVE TWO REMOTES

$ git remote -v

CHANGE YOUR CODE

$ git push (to bitbucket/github/gitlab)
$ git push heroku main
```
