## Day 1
<h2>Git</h2>
Git is type of Version Control Sytem tools that helps to track changes in code. It is popular,  free & open source, Fast & scalable.

- It helps in track the Code history.
- It helps to collabrate with other.
<h2>GitHub</h2>
GitHub is a website that allow developers to store and manage their code using Git. (https://github.com).

- All the code and file are uploaded into github in form of Folder called **repository**(repo).

- Steps to Create New Repo:-
    1. Go to new tab
    2. give name of Repo
    3. keep repo public/private
    4. Initilize README (Keep short summary about repo)
<h3>Setting up Git</h3>
Download Gitbash and VS code. <br> To check verison of github :- git --version

- **Configureing Git**: it is used to configure your github account into gitbash.(~ show root directory)
---
## Day 2
<h2>Clone & status</h2>
This is the command used to clone the Remote repository on local machine(own laptop).<br>
git clone <-link of repo->.

- Mostly we used HTTPS to clone any repo. 
- cd is used to change the directory and ls -a used to see hidden file.
- Some symbole is used to indicate -
    a. **Untracked**(U) :  it denote file is newly created. new file that git doen't yet track.
    b. **Modified**(M) : it denoted there is some modification is done in that file.
    c. **Staged**(A) : File is ready to be committed.
    d. **Unchanged**: File after commited is shown unchanged.
<h2>Command</h2>

- Add : adds new or changed file in your woking directory to the git staging area
- Commit : it is the record of change
- Push: used to upload local repo/file content to remote repo.
- Init : used to create a new git repo from local machine
---
## Day 3
<h2>WorkFlow</h2>
Local Git

```
Github --> clone repo --> changes --> Add --> commit --> push
```
<h2>Branches</h2>

```
                                              ---------         
                                              [Feature]
                                              ---------                
                                                 |
                                                 V
                            ------O------O-------O--
                           /                        \
                          /                          \    -------
            O------O-----/-------O-------O-------O---O <--|Merge|
                                                 ^        -------
                                                 |
                                            --------
                                            |Master|
                                            --------
```
<h2>Pull Request</h2>
It lets you tell other about changes you've pushed to a branch in a repository on GitHub.

- Pull:  Used to fetch and download content from a remote repo and immediately update the local repo to match that content. eg:- *git pull origin main*

<h3>Merge Conflicts</h3>
An event that takes place when Git is Unable to automatically resolve differences in code between two commits.

<h2>Undoing Changes</h2>

- Case 1: staged changes *git reset <-file name->* <br>
        *git reset*
- Case 2: commited changes (for one commit). *git reset HEAD~1*
- Case 3: commited changes(for many commits). *git reset <- commit hash->*
        *git reset --hard <-commit hash->*
        *git log* (used to see the hash and other details of commit)
<h2>Fork</h2>
A fork is a new repository that shares code and visibility settings with tha original "upstream" repository.<br>
Fork is a rough copy.

---
## Day 4
<h2>Ticket, Issue & Board</h2>

<h3>Ticket</h3>
A ticket is a task or work item used to track a specific job, bug, feature, or improvement. In project management, every ticket usually has a unique ID and information such as title, description, priority, assignee, and status.

- Helps to organize work
- Makes it easier to track progress
- Allows team members to know what is pending, in progress, or completed

<h3>Issue</h3>
An issue is a GitHub item used to track work, bugs, enhancements, or discussions related to a repository. It is similar to a ticket but commonly used in GitHub workflows.

- Examples: bug report, feature request, documentation task
- Can be assigned to a person
- Can have labels, milestones, and comments
- Can be linked with pull requests and commits

<h3>Project Board</h3>
A project board is a visual way to manage issues and tasks using columns such as To Do, In Progress, Review, and Done.

- Helps teams see the workflow clearly
- Makes task progress easy to monitor
- Supports Kanban-style project management

Example board:

```
To Do  ->  In Progress  ->  Review  ->  Done
```

In GitHub, issues can be added to a project board so that each task is visible and can be moved as work progresses.

- Issue = a single task/bug/feature request
- Ticket = the same idea in project management workflows
- Board = the place where tickets/issues are organized and tracked visually

This workflow helps teams stay organized and manage software development efficiently.
---

## Day 5

<h2>Git Configuration and the Daily Workflow</h2>

Git records snapshots of your project. A normal local workflow has three main areas:

1. **Working tree**: the files you are editing.
2. **Staging area (index)**: the changes selected for the next commit.
3. **Repository**: the committed history stored by Git.

Configure the author information Git records in new commits:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

Use `--local` instead of `--global` to configure a value for only the current repository. GitHub account authentication is separate from this commit identity.

```bash
git status
git add README.md
git add .
git diff
git diff --staged
git commit -m "Add project documentation"
git log --oneline
```

- `git diff` shows unstaged changes; `git diff --staged` shows staged changes.
- Stage only the files that belong in the commit. Review the staged diff before committing.
- A commit is a local snapshot; it is not uploaded to GitHub until it is pushed.

**Practice:** Create or edit a small file, inspect the unstaged diff, stage it, inspect the staged diff, and create a descriptive commit.

---
## Day 6

<h2>Branches and Feature Branch Workflow</h2>

A branch is a movable reference to a commit. Branches let work proceed independently without changing the main line of development until it is ready.

```bash
git branch
git switch -c feature/add-readme-section
git status
# Make and commit a small change on this branch.
git add README.md
git commit -m "Add learning goals"
git switch main
git branch -d feature/add-readme-section
```

`git switch -c` creates and switches to a branch. The older equivalent is `git checkout -b`. To switch to an existing branch, use `git switch <branch-name>`. Delete a branch only after its work has been merged or is no longer needed.

**Feature branch workflow:**

1. Start from an up-to-date `main` branch.
2. Create a focused branch for one task.
3. Make small commits with clear messages.
4. Push the branch and open a pull request.
5. Review, merge, and remove the finished branch.

Common strategies include feature branches, release branches, and short-lived branches that merge frequently. Teams should document their chosen branch names and protection rules.

**Practice:** Create a feature branch, make two related commits, and compare its history with `main` using `git log --oneline --graph --all`.

---

## Day 7

<h2>Merging, Rebasing, and Merge Conflicts</h2>

Merging combines branch histories and can create a merge commit. Rebasing replays commits on top of another base to create a linear history.

```bash
# Merge a completed feature branch into main
git switch main
git merge feature/add-readme-section

# Rebase a feature branch onto the latest main
git switch feature/add-readme-section
git fetch origin
git rebase origin/main
```

- Merge is useful when the team wants to preserve the branch's history.
- Rebase can make a feature branch's history easier to follow.
- Do not rebase commits that other people already depend on unless the team has agreed how to handle the rewritten history.
- A merge conflict means Git cannot safely choose between competing changes. Open each conflicted file, decide the correct final content, remove conflict markers, then test the result.

```bash
git status
# Edit each conflicted file and remove <<<<<<<, =======, and >>>>>>> markers.
git add <resolved-file>
git merge --continue
# For a rebase conflict, use:
git rebase --continue

# Cancel an in-progress operation if needed:
git merge --abort
git rebase --abort
```

**Practice:** Make conflicting edits to the same line on two branches, merge the branches, resolve the conflict, and verify the final file.

---

## Day 8

<h2>Remotes, Clone, Fetch, Pull, and Push</h2>

A **remote** is a named reference to another repository, commonly a GitHub repository. `origin` is the conventional name for the remote created by `git clone`.

```bash
git clone https://github.com/OWNER/REPOSITORY.git
cd REPOSITORY
git remote -v
git fetch origin
git pull origin main
git push -u origin main
```

- `git fetch` downloads remote commits and references but does not merge them into the current branch.
- `git pull` fetches and then integrates the upstream changes into the current branch (by merge or, when configured, rebase).
- `git push` uploads local commits to a remote branch. The `-u` option sets the upstream for future pushes and pulls.
- If a project uses a branch other than `main`, use that branch name in commands.

For a new local project, connect it to an existing GitHub repository:

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/OWNER/REPOSITORY.git
git branch -M main
git push -u origin main
```

**Practice:** Clone a repository, create a branch, commit a change, push the branch, and inspect the remote branch on GitHub.

---

## Day 9

<h2>Pull Requests and Code Review</h2>

A pull request (PR) proposes changes from one branch into another. It is a place to discuss, review, test, and approve changes before they are merged; it is not the same as the `git pull` command.

**A useful PR includes:**

- A clear title and summary of the change.
- The reason for the change and any relevant issue link.
- Test steps and results.
- Screenshots or examples when they help reviewers.

**Review workflow:**

1. Push the feature branch to GitHub.
2. Open a PR with the correct base and compare branches.
3. Review the diff and automated checks.
4. Leave specific, respectful comments or request changes.
5. Update the branch, respond to feedback, and rerun checks.
6. Merge using the method selected by the repository maintainers.

Reviewers should focus on correctness, readability, tests, scope, and possible regressions. Authors should treat review as collaboration, not as a personal judgment.

**Practice:** Open a PR for a small documentation change. Review the diff as if you were a teammate and add a concise description and verification steps.

---

## Day 10

<h2>GitHub Collaboration and Open Source</h2>

### Fork and upstream workflow

A fork is your GitHub-hosted copy of another repository. It allows you to propose changes without write access to the original repository.

```bash
git clone https://github.com/YOUR-USERNAME/REPOSITORY.git
cd REPOSITORY
git remote add upstream https://github.com/ORIGINAL-OWNER/REPOSITORY.git
git remote -v
git fetch upstream
git switch main
git merge upstream/main
git switch -c docs/fix-typo
```

Push your branch to your fork, then open a PR against the original repository. Read the contribution guide and code of conduct first, and make one focused contribution at a time.

### Issues, labels, milestones, and team work

- **Issues** describe bugs, feature requests, questions, and planned work. Include steps to reproduce a bug and the expected versus actual behavior.
- **Labels** classify issues and PRs, for example `bug`, `documentation`, or `good first issue`.
- **Milestones** group issues and PRs toward a release or project goal.
- **Assignees** identify who is working on an item. Link related issues and PRs so progress is traceable.
- **Tickets** are the general project-management term for trackable work; GitHub Issues often serve this purpose.
- **Project boards** organize work into views or statuses such as Todo, In Progress, Review, and Done.

For professional collaboration, keep changes scoped, communicate blockers early, and avoid pushing directly to a protected default branch.

### GitHub profile, stars, and watches

Keep a profile README, useful project descriptions, and pinned repositories up to date. A **star** bookmarks or signals interest in a repository; **watch** controls notifications about repository activity. Neither grants repository access.

**Practice:** Find an appropriate open issue, read the repository contribution instructions, and draft a focused contribution plan before making changes.

---