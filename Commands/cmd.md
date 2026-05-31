# 🚀 Getting Started

## Install Git

### Windows

Download Git from:
https://git-scm.com/

### Check Git Version

```bash
git --version
```

---

# 🔥 Basic Git Commands
<h3>Configuring Git</h3>

```
git config --global user.name "My Name"
git config --global user.email "xyz@gmail.com"
git config --list
```
<h3>Clone & Status</h3>

```
git clone <-link of repo->
git status
```
<h3>Add & Commit</h3>

```
git add <-link of repo->
git commit -m "Some Message"
```
<h3>Push</h3>

```
git push origin main
```
<h3>Init </h3>

```
git init
git remote add origin <-link of original repo created on github account->
git remote -v (used to verify remote)
git branch (to check branch)
git branch -M main (to rename branch)
```
<h3>Branching</h3>

```
git branch      (to check branch)
git branch -M main  (to remote branch)
git checkout <-branch name->    (to navigate)
git checkout -b <-new branch name-> (to create new branch)
git branch -d <- branch name->      (to delete branch)
```
<h3>Merging</h3>

```
git diff <-branch name->    (to compare commits, branches, file & more)
git merge <-branch name->   (to merge two branches)
```
<h3>Pull</h3>

```
git pull origin main
```
<h3>Undoing Changes</h3>

```
Case 1: git reset <-file name->     (staged changes)
        git reset  
Case 2: git reset HEAD~1            (commited changes)
Case 3: git reset <- commit hash->  (commited changes[for many commits])
        git reset --hard <-commit hash->
        git log                      (used to see the hash and other details of commit)

```
