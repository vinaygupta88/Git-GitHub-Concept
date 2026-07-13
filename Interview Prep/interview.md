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

## Branch Visualization

### 1. Simple Branch Workflow

```text
main:      A---B---C---M
                 \
feature:            D---E---F
```

- `main` is the stable branch.
- `feature` is created from `main` to develop a new feature.
- After review, the feature branch is merged into `main`.

### 2. Pull Request Flow

```text
Developer A        Developer B
   |                   |
   |--- create branch --|
   |                   |
   |--- commit changes -|
   |                   |
   |--- push branch ---->|
   |                   |
   |<-- open PR --------|
   |                   |
   |--- review/approve -|
   |                   |
   |--- merge into main |
```

### 3. CI/CD Flow in GitHub

```text
Code Push / PR
      ↓
GitHub Repository
      ↓
Build Trigger
      ↓
Run Tests / Linting
      ↓
Deploy to Staging
      ↓
Manual or Automatic Production Deployment
```

### 4. Branch Strategy Example

```text
develop:    A---B---C---D---E
            \            \
feature1:     F---G       H---I
                          \
feature2:                    J---K
```

- Separate branches are used for different tasks.
- Features are merged into `develop` or `main` after testing.

## Additional CI/CD Interview Questions

31. What is CI and why is it important in GitHub workflows?
   - Answer: CI stands for Continuous Integration. It means automatically building and testing code whenever changes are pushed to a repository. It helps catch bugs early and keeps the codebase stable.

32. What is CD and how is it different from CI?
   - Answer: CD stands for Continuous Delivery or Continuous Deployment. CI focuses on automated testing and build validation, while CD automates the release process to staging or production.

33. How does GitHub Actions help with CI/CD?
   - Answer: GitHub Actions lets developers define workflows triggered by events like push, pull request, or release. These workflows can build, test, and deploy applications automatically.

34. What is the purpose of a workflow file in GitHub Actions?
   - Answer: A workflow file defines the automation steps, such as installing dependencies, running tests, and deploying the app.

35. How do branches and deployments relate in CI/CD?
   - Answer: Different branches often map to different environments, such as `develop` for staging and `main` for production. This helps isolate work and manage release flow safely.

## Extra GitHub Features Frequently Asked in Interviews

36. What are GitHub Issues, and how are they used?
   - Answer: GitHub Issues are used to track bugs, feature requests, tasks, and discussions related to a project. They help teams organize work and communicate progress.

37. What is GitHub Projects and how is it useful?
   - Answer: GitHub Projects is a project management board that helps team members track tasks using columns like To Do, In Progress, and Done. It integrates with issues and pull requests.

38. What is a GitHub Action?
   - Answer: A GitHub Action is an automation workflow that runs based on repository events such as push, pull request, or release. It is commonly used for CI/CD, testing, and deployment.

39. What is GitHub Pages?
   - Answer: GitHub Pages is a hosting service that allows developers to publish static websites directly from a GitHub repository.

40. What is a release in GitHub?
   - Answer: A GitHub release marks a specific version of the project and often includes source code archives and release notes for deployment or distribution.

41. What is the difference between a branch and a tag?
   - Answer: A branch is a movable pointer for ongoing development, while a tag is a fixed reference used to mark a specific point in history such as a release version.

42. What is a commit message, and why is it important?
   - Answer: A commit message describes what changed in the code. Clear commit messages make project history easier to understand and debug.

43. What is GitHub Desktop?
   - Answer: GitHub Desktop is a graphical user interface for Git that makes cloning, committing, and pushing changes easier for developers who prefer not to use the command line.

44. What is branch protection in GitHub?
   - Answer: Branch protection enforces rules such as requiring pull request reviews, requiring status checks, and preventing direct pushes to important branches like `main`.

45. How do team permissions work in GitHub repositories?
   - Answer: GitHub allows repository owners to assign roles such as read, write, triage, maintain, or admin. These permissions control what users can do in the project.

46. What is the purpose of GitHub Codespaces?
   - Answer: GitHub Codespaces provides a cloud-based development environment that allows developers to code, build, and test projects directly in the browser or VS Code.

47. What is the difference between Git and GitHub Desktop?
   - Answer: Git is the underlying version control system, while GitHub Desktop is a client application that simplifies interactions with Git repositories for users.

48. What is a `.gitignore` file?
   - Answer: `.gitignore` tells Git which files or folders should not be tracked, such as build artifacts, local environment files, or secrets.

49. Why should secrets never be committed to GitHub?
   - Answer: Secrets like API keys or tokens can be exposed to others, leading to unauthorized access, service misuse, or security incidents.

50. What are the best practices for a clean GitHub workflow?
   - Answer: Use descriptive branch names, commit messages, pull requests, code reviews, branch protection, regular pulls, testing before merge, and avoid committing sensitive files.
