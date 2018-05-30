## Git Basic Cheat Sheet
```sh
$ git init
```
Initializes an empty repository.
##
### Local changes
```sh
$ git status
```
Show the status of the changed or committed files in your working directory.
```sh
$ git diff
```
List the differences between tracked files since the last commit.
```sh
$ git add <filePath>
```
Add a file to the staging area.

```sh
$ git add -i
```
Interactive menu for adding and removing files from the staging area.

```sh
$ git commit -m "message"
```
Commit every file that has been added to the staging area. Commit message is mandatory and should be meaningful.
##

### Branches
```sh
$ git branch
```
Show the current active branch.
```sh
$ git branch -a
```
List all the known branches.
```sh
$ git checkout <branch>
```
Switch to another branch.
```sh
$ git branch <branchName>
```
Create a new branch.
```sh
$ git checkout -b <branchname>
```
Create and switch to a new branch.
```sh
$ git branch -d <branchName>
```
Delete a local branch.
##

### Update and Publish
In order to add a remote server to your local git repository, you must have an SSH key generated 
locally and added to the server, so it can identify you.

In Git bash:
```sh
ssh-keygen -t rsa -b 4096 -C "_your_email@example.com_"
```

GitHub how-to: 
https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

GitLab how-to:
https://docs.gitlab.com/ce/ssh/README.html
##


```sh
$ git remote add <name> <gitURL>
```
Add a new remote repository.
```sh
$ git fetch 
```
Download all changes but don't integrate them.

```sh
$ git pull
```
Download changes for the current branch and merge them.

```sh
$ git push
```
Push local changes to the remote repository.

```sh
$ git branch -dr <branchName>
```
Delete remote branch.

##
### Merge
```sh
$ git merge <branch>
```
Merge another branch into the currently active one.
```sh
$ git mergetool
```
In case of a merge conflict, use your preconfigured tool the resolve the issue.
How to configure mergetool:
https://gist.github.com/karenyyng/f19ff75c60f18b4b8149