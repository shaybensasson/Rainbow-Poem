# Rainbow-Poem

[Github for starters](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV)

Can be skipped:
* 1.5
* 1.7

> Another line from the past: commit 11546750cf189da7894804e9fc11b988c7e24d83

# Git snippets

## Git commit -a
Stage all changes and commit with a message
```sh
git commit -a -m "A message"
```

## Git config
List all relevant configs
```sh
git config --list
```

## `Git Remote` Information
Get the repo remote (e.g. Origin) and the associated urls of github.

```sh
git remote -v
```

## Starting from local computer and attaching a repo

```sh
git init

# create an empty repository on GitHub with no files

git remote add origin <REPO_URL>
```

## Creating a pull request
```sh
# get latest version - assuming you are on `main` branch (the default)
git pull

#create a branch
git branch feature1

#switch to the new branch
git checkout feature1

# Make your changes

# add your changes
git add . 

#commit your change
git commit -m "Explaining what I changed"

### ========================== ###

#switch to main
git checkout main

# get latest version - get any changes that were pushed since the branch creation
git pull

#switch to our branch
git checkout feature1

#try to merge branch with main
git merge main
```

In case there are any conflict, solve them and try to re-add the conflicted files, commit again, and finally push:
```sh
git push origin main
```