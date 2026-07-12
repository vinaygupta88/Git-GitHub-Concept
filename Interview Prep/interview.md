# GitHub Interview Questions with Answers

## Basic Level (10 Questions)

1. What is Git and how is it different from GitHub?
   - Answer: Git is a distributed version control system used to track changes in source code. GitHub is a web-based platform that hosts Git repositories and provides collaboration features like pull requests, issues, and code review.

2. What is a repository in GitHub?
   - Answer: A repository is a storage location for a project, containing files, folders, commit history, and branch information. It can be public or private.

3. How do you create a new repository on GitHub?
   - Answer: Go to GitHub, click the New repository button, enter a name, choose visibility (public/private), optionally add a README, and then click Create repository.

4. What is the purpose of a README file in a repository?
   - Answer: A README explains what the project does, how to set it up, usage instructions, and important project details. It helps visitors understand the repository quickly.

5. What is the difference between a local repository and a remote repository?
   - Answer: A local repository exists on your machine and is used for development. A remote repository is hosted online on GitHub and is used for sharing and collaboration.

6. What does the `git clone` command do?
   - Answer: `git clone` copies an existing GitHub repository from a remote location to your local machine so you can work on it.

7. What is the purpose of `git status`?
   - Answer: `git status` shows the current state of the repository, including modified, staged, and untracked files.

8. What is the difference between `git add` and `git commit`?
   - Answer: `git add` stages changes, preparing them to be saved. `git commit` creates a permanent snapshot of the staged changes in the repository history.

9. What does `git push` do?
   - Answer: `git push` uploads local commits to the remote GitHub repository so others can access them.

10. What is a branch in Git, and why is it useful?
   - Answer: A branch is a separate line of development. It lets developers work on features or fixes independently without affecting the main codebase until the changes are merged.

## Intermediate Level (10 Questions)

11. What is a pull request, and how is it useful in a team workflow?
   - Answer: A pull request is a request to merge code from one branch into another. It allows teammates to review, discuss, and approve changes before merging them.

12. Explain the difference between `git pull` and `git fetch`.
   - Answer: `git fetch` downloads updates from the remote repository without merging them. `git pull` fetches and immediately merges the remote changes into the current branch.

13. What are merge conflicts, and how do you resolve them?
   - Answer: Merge conflicts happen when two branches modify the same part of a file differently and Git cannot automatically decide the correct result. You resolve them by editing the conflicted file, choosing the correct content, and then committing the resolution.

14. What is the difference between staging and committing changes?
   - Answer: Staging is selecting which modified files are included in the next commit. Committing records those staged changes as a snapshot in the repository history.

15. How do you create a new branch and switch to it?
   - Answer: You can use `git checkout -b branch-name` or `git switch -c branch-name` to create and move to a new branch.

16. What is the purpose of `git log`, and what information does it show?
   - Answer: `git log` displays the history of commits in a repository, showing commit hashes, author names, dates, and commit messages.

17. What is a fork in GitHub, and how is it different from a clone?
   - Answer: A fork is a personal copy of someone else's repository on GitHub under your own account. A clone is a local copy of a repository on your machine.

18. How do you undo a staged change before committing?
   - Answer: You can use `git reset <file-name>` to unstage a file, or `git restore --staged <file-name>` in newer Git versions.

19. What is the difference between a public repository and a private repository?
   - Answer: A public repository is visible to everyone, while a private repository is restricted to selected users or collaborators.

20. Why is `git init` used, and when would you use it?
   - Answer: `git init` initializes a new Git repository in a folder. It is used when starting a project locally and wanting to track its changes with Git.

## Advanced Level (10 Questions)

21. Explain the workflow of collaborating on a GitHub project using clone, branch, commit, push, and pull request.
   - Answer: A developer clones the repository, creates a branch for a task, makes changes, commits them, pushes the branch to GitHub, and opens a pull request for review and merging into the main branch.

22. What are the common causes of merge conflicts, and what strategy do you use to resolve them correctly?
   - Answer: Conflicts usually happen when multiple developers edit the same lines or files. The strategy is to inspect the conflict markers, combine the intended changes carefully, test the result, and commit the resolved version.

23. How does Git store commit history, and why is commit hash important?
   - Answer: Git stores commit history as a chain of snapshots connected by hashes. Each commit has a unique SHA hash that identifies it and helps track exact versions of the project.

24. What is the difference between `git reset --soft`, `git reset --mixed`, and `git reset --hard`?
   - Answer: `--soft` moves HEAD back but keeps changes staged. `--mixed` moves HEAD back and unstages the changes. `--hard` resets HEAD and discards changes completely from the working directory.

25. How would you revert a commit that was already pushed to the remote repository?
   - Answer: You can create a new commit that undoes the changes, using `git revert <commit-hash>`, which is safer than deleting history when the commit is already shared.

26. What is the difference between rebasing and merging a branch?
   - Answer: Merging creates a merge commit and preserves branch history. Rebasing replays commits onto another branch, creating a cleaner linear history but rewriting commit history.

27. How do you handle a situation where multiple developers modify the same file in parallel?
   - Answer: Coordinate through branches and pull requests, frequently pull updates, resolve conflicts carefully, and communicate with team members to avoid overlapping changes.

28. Why are pull requests important in code review and collaboration workflows?
   - Answer: They improve code quality by enabling review, discussion, validation, and approval before merging. They also provide traceability and a clear history of changes.

29. How do you secure a GitHub repository for team use, and what are some common best practices?
   - Answer: Use private repositories when needed, set branch protection rules, require pull request reviews, enable two-factor authentication, manage permissions, and use signed commits where required.

30. Explain how GitHub supports collaboration, version control, and project tracking in software development.
   - Answer: GitHub provides Git-based version control, branching, pull requests, issue tracking, project boards, wikis, and code review tools that help teams collaborate efficiently and manage projects effectively.
