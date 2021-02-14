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

## Pull request on github
* Create a branch using github interface (e.g. feature1)

* git pull
```sh
git pull
```

* switch to the branch
```sh
git checkout feature1
```

* Make changes to code

* Add them and commit
```sh
# add your changes
git add . 

#commit your change
git commit -m "Explaining what I changed"

#push the changes to github
git push
```

* On github choose "Compare & Pull request"
	* Make sure you are trying to merge `feature1` branch into the `main` branch
	* Describe your pull request
	* Click "Create pull request"


* That's is, now someone with permission can merge this pull request.

## Mergin when working alone
```sh
# get latest version - assuming you are on `main` branch (the default)
git pull

#create a branch
git branch feature1

#switch to the new branch
git checkout feature1

# or just: 
#	git checkout -b feature1
# in a single command

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

#try to merge branch with main
git merge feature1

#if merge successful, do not keep the branch.
git branch -d feature1
```

In case there are any conflict, solve them and try to re-add the conflicted files, commit again, and finally push:
```sh
git push origin main
```

# Git log
```sh
git log --oneline
```

# Stashing
```sh
git stash
```

```sh
#to list
git stash list 
```


```sh
git stash pop
```

# Revert
Go back to an earlier commit, by creating a brand new commit.

Two options:
1. Revert last commit
```sh
git revert HEAD
```

2. Choose a commit hash from the logs:
```sh
git log --oneline
```
Run revert:
```sh
git revert HASH
```
