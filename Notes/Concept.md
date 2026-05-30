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