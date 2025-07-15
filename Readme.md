# GIT practice repo
## This is a demo project to practice git commands
*this is an italic text*<br>
**this is a bold text**<br>
~~this is a strikethrough text~~<br>
**this text is nested bold and _italic_ text**<br>
***this text is both bold and italic***<br>
this is a <sub>subscript</sub> text<br>
this is a <sup>superscript</sup> text<br>
this is an <ins>underlined</ins> text<br>
<hr>

## Tracking changes on git repository
### 1. Initializing a git repository
cd \<git repo folder\><br>
git init<br>
### 2. staging the changes
git add \<file name\><br>
git add . (. adds all the files changed in current directory)<br>
git add --all (adds all the changed files)<br>
### 3. committing changes
git commit -m "\<main commit message\>" -m "\<secondary commit message\>"<br>
### 4. pushing changes to the remote repository
git push origin master<br>
<hr>

## generating ssh key to authenticate to github
### 1. generate key pair using ssh-keygen
ssh-keygen -t rsa -b 4096 -C "\<your github email address\>" <br>
-t = type of encryption<br>
-b = strength of the encrypted key (no. of bits) <br>
<hr>

## checking difference using git diff
### checking difference b/w current work space & staging area(if no changes staged, then latest commit is in the staging area)
git diff<br>
### checking difference b/w staging area & localrepo latest commit(HEAD)
git diff --staged HEAD<br>
we can change the "HEAD" with commit id if we want to check the diff W.R.T  any other commit id<br>
### comparing changes with different local commits
git diff \<commit id 1\> \<commit id 2\>
<hr>

## git branching
by default main/master branch is the only branch, it's the main branch on which we are working<br>
### 1. creating a new branch
git checkout -b \<new branch name\>
### 2. switching to another branch
git checkout \<branch name\>
### 3. merging branches
to merge a feature branch into master branch<br>
git checkout master<br>
git merge \<feature branch name\><br>
### 4. Pull requests
usually we dont merge directly, we push the branch to the remote git repo and raise the Pull Request(PR)<br>
this PR will be reviewed by the reviewers and later be merged if everything is alright.

## git pull
using git pull, we can get the changes from the remote repository to our local repository<br>
### using git pull
git pull origin master<br>
<hr>