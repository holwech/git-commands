# Useful git-commands
#### Branching
Make branch, checkout to branch, push to remote and track

```
git checkout -b branch_name
git push -u origin branch_name
```
---
Delete branch locally
```
git branch -d branch_name
```
---
Delete branch on remote
```
git push origin --delete branch_name
```
---
Track remote branch

```
git branch --track branch_name origin/branch_name
```
or just
```
git checkout branch_name
```
Which automatically tracks the branch if the name corresponds to the remote branch name.
---

#### Initializing and creating new repositories
Create  a folder and clone into it

```
git clone github.com/repo_url folder_name
```
---
Create a new repository locally and push to remote. (Requires a already made repo on github)
```
$ cd folder_name
$ git init
$ echo "This is my readme-file. Not required if already initialized on github" > README
$ git add .
$ git commit -m "First commit"
$ git remote add origin https://github.com/username/repo_name.git
$ git push origin master
```

#### Commiting
Unstage a commit (unsure about this one, use at own risk)
```
git reset --soft HEAD^
```
