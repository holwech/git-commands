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
cd folder_name
git init
echo "This is my readme-file. Not required if already initialized on github" > README
git add .
git commit -m "First commit"
git remote add origin https://github.com/username/repo_name.git
git push origin master
```

#### Commiting and stashing

Stashing
```
git stash
```
List all stash data
```
git stash list
```
Unstash most recent stash
```
git stash apply
```
Unstash older data (given there is as stash with number 2}
```
git stash apply stash@{2}
```
Remove stashed data
```
git stash drop stash@{0}
```
or remove most recent stash
```
git stash pop
```

---

Unstage a commit (unsure about this one, use at own risk)
```
git reset --soft HEAD^
```

#### Tracking, untracking and more, for files and folders
Files and directory(folder)  are adressed as
```
filename
// or
folder/
```
You have to choose depending on what you want to do.
In the examples below mostly filename is used for simplicity.

---

Remove file from repository and untrack (Does not delete the actual file)
```
git rm --cached filename
```
Remove folder from repository and untrack (Does not delete delete the actual folder)
```
git rm -r --cached folder
```
Remove the `--cached` to also delete the file/folder.
