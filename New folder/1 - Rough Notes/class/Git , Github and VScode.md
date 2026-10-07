05/08/2026

Status : #baby 

Tags : [[cgclass]],


# Git , GitHub and VScode
## Index
## Index

- [[#Git , GitHub and VScode]]
  - [[#Notes 10/08/26]]
    - [[#Format of naming in github branches]]
    - [[#Issues]]
  - [[#Notes 11/08/26]]
    - [[#some git commands]]
  - [[#Notes 12/08/26]]
    - [[#Working Directory]]
    - [[#Staging Area]]
    - [[#Check Repository Status]]
    - [[#Creating Folder and moving to it]]
    - [[#How to View Logs in Git]]
    - [[#To view changes]]
    - [[#Basic Git Workflow]]
    - [[#hw]]
  - [[#Notes 13/08/26]]
    - [[#git rm --cached]]
    - [[#git restore and git restore --stage]]
    - [[#git push and git push -u]]
- [[#Further link]]
- [[#References]]







Today 6/8/26 
- explore github readme images

College Event Management System
**Branches**
	- Treasurer
	- Designer
	- Cateress

### Notes 10/08/26
**Tags :** [[github]],[[format]],[[repositories]]

#### Format of naming in github branches

```
feature/<feature-name>
bugfix/<bug-name>
hotfix/<issue-name>
docs/<documentation-name>
refactor/<change-name>
test/<test-name>
```

##### Some Suggestions
- Use lowercase letters.
- Use hyphens to separate words.
- Keep the name short and meaningful.
- Mention the purpose of the branch.
- Avoid spaces.

#### Issues
Learnt Creating issues
##### Proojects
learnt creating project
in repo of projects `settings > gernal > features section > tick issue to create issue for all users `

### Notes 11/08/26
**Types of version control System**
- Local Version control system 
	- which operates locally on your computer
	- (**Drawback :** no server backup )
	- **Example** : VSE in RCS (revision Control System)
- Centralized Version control system
	- which operate at centralized server
	- (**Drawback :** need internet )
	- **Example** : SVN/ Subversion 
- Distributed Version control system
	- `Which works both Locally and Online`
	- **Example** : Git
#### some git commands
to enter username and email

``` bash
git config --global user.name "Your Name"

git config --global user.email "your-email@example.com"
```

To see all Git configuration values:

``` bash
git config --list
```


To check only your configured name:

``` bash
git config --global user.name
```

To check only your configured email:

``` bash
git config --global user.email
```

To move forward in folder - we use change directory(cd)
```
cd <folder_name>
```

- if don't want to type full name
	- just type folder name till few character till unique and press tab

To move backward in folder - we use change directory(cd)
```
cd ..
```


To run git
``` bash
git init
```

`git init` creates a new Git repository in the current directory.


### Notes 12/08/26

``` text
Working Directory
       |
       | git add
       v
Staging Area
       |
       | git commit
       v
Local Repository
```


#### Working Directory
This is the actual folder where you create and modify files.(`to track files we send files from working directory to Staging area`)

#### Staging Area
- The staging area contains changes that you have selected for the next commit
``` bash
git add <file_name>
```

- Or stage all changes:

``` bash
git add .
```

`The . means the current directory and its relevant contents.
`
####  Check Repository Status
``` bash
git status
```

It tells you:

-   Which files are untracked.
-   Which files are modified.
-   Which files are staged.
-   Which branch you are currently on.
-   Whether there are changes waiting to be committed.gitgit 

#### Creating Folder and moving to it
### Windows

``` bash
mkdir git-practice
```

### macOS / Linux

``` bash
mkdir git-practice
```

The same `mkdir` command works in Git Bash as well.

``` bash
cd git-practice
```

Check your current location if needed:

``` bash
pwd
```

On Windows Command Prompt, you can also use:

``` cmd
cd
```


#### How to View Logs in Git
Use:

``` bash
git log
```

Example:

``` text
commit abc123...
Author: Rahul Sharma
Date: ...

    Add initial HTML page
```

`For a shorter history:`

``` bash
git log --oneline
```

Example:

``` text
a1b2c3d Add initial HTML page
```

The short value is part of the commit's unique identifier.

#### To view changes 
Use:

``` bash
git diff
```

This shows changes in the `working directory` that have not been staged.

After staging changes, use:

``` bash
git diff --staged
```

This shows changes currently in the `staging area.`

#### Basic Git Workflow
``` text
1. Create / modify files
          |
          v
2. git status
          |
          v
3. git add
          |
          v
4. git status
          |
          v
5. git commit
          |
          v
6. git log
```

#### hw 
- create index.html
- and create other 3 files 
- then practice all todays commands

### Notes 13/08/26
#### git rm --cached
`git rm --cached` removes a file from Git's tracking but **does not delete the file from your computer**.

```bash
git rm --cached <file>
```

##### Important

```text
git rm --cached file.txt
```

means:

```text
Remove from Git trackingigin 
Keep the file on computer
```

Whereas:

```bash
git rm file.txt
```

means:

```text
Remove from Git tracking
Remove the file from computer
```



#### git restore and git restore --stage
##### git restore
`git restore` is used to restore files to a previous state.

The most common use is to discard **unstaged changes**.

###### example
Suppose:

```bash
git status
```

shows:

```text
modified: index.html
```

You changed `index.html`, but you do not want those changes.

Run:

```bash
git restore index.html
```

Git restores the file to the version from the latest ==commit.==

`Important`

Be careful when using:

```bash
git restore <file>
```

Your uncommitted changes can be lost.

##### git restore --staged

`git restore --staged` removes a file from the **staging area**.

It does not remove your changes from the file.

###### example

Create or modify:

```text
index.html
```

Then:

```bash
git add index.html
```

Now the file is staged.

Check:

```bash
git status
```

###### To unstage it:

```bash
git restore --staged index.html
```

The file is no longer staged, but your changes remain.

###### Difference

```bash
git restore index.html
```

Discards unstaged changes.

```bash
git restore --staged index.html
```

Unstages the file but keeps the changes.

###### Easy way to remember

```text
restore
    ↓
Remove changes

restore --staged
    ↓
Remove from staging
```


##### git clone
`git clone` creates a local copy of an existing remote repository.

It downloads:

- Project files
- Git history
- Branch information
- Commit information

**Syntax**

```bash
git clone <repository-url>
```


###### Examples 

```bash
git clone https://github.com/username/my-project.git
```

Git creates a folder using the repository name.

Example:

```text
my-project/
```

Then enter the folder:

```bash
cd my-project
```

Check the repository:

```bash
git status
```


###### What happens when you clone?

```text
GitHub Repository
       |
       | git clone
       v
Your Computer
       |
       v
Local Repository
```

The cloned repository also gets a remote named:

```text
origin
```

You can check it using:

```bash
git remote -v
```


#### git push and git push -u
##### git push
`git push` sends your local commits to a remote repository.

Think:

```text
Local Repository
       |
       | git push
       v
Remote Repository
```

###### Example

```bash
git push
```

This works when Git already knows which remote branch the current branch should push to.

##### git push -u
When pushing a branch for the first time, use:

```bash
git push -u origin main
```

Here:

```text
git       → Git command
push      → Send commits
-u        → Set upstream branch
origin    → Remote repository name
main      → Branch name
```

After using:

```bash
git push -u origin main
```

Git remembers the relationship between your local `main` branch and the remote `main` branch.

After that, you can usually use:

```bash
git push
```

instead of:

```bash
git push origin main
```

### Notes 13/08/26
##### git pull
`git pull` gets changes from a remote repository and integrates them into your current branch.

Basic command:

```bash
git pull
```

###### For example:

```bash
git pull origin main
```

means:

```text
Get changes from origin/main
        +
Integrate them into current branch
```



##### git show




##### HW
do [Assignment](https://github.com/codinggita/CGxSU_Semester_1/blob/Notes/Git/Semester_1/git_%26_github(sem_01)/00.Git/01.Git-Working-With-Remote-Repository/Assignment.md)

**Checklist**
###### Part 1: Create Repo on GitHub

- [x] Create repo `Codinggita-git` (public, with README)
- [x] Copy HTTPS URL

###### Part 2: Desktop Folder

- [x] Create `git-practice` folder on Desktop
- [x] Open in terminal, check path with `cd`

###### Part 3: Clone Repo

- [x] `git clone <repo-url>` inside `git-practice`

###### Part 4: Navigate

- [x] `cd Codinggita-git`
- [x] Practice `cd` in/out of folder

###### Part 5: Check Status

- [x] Run `git status`
- [x] Note current branch, changes, untracked files

###### Part 6: Create HTML Files

- [x] Create `index.html`
- [x] Create `login.html`
- [x] Create `signup.html`

###### Part 7: Status Check

- [x] Run `git status`
- [x] Confirm 3 files show as untracked

###### Part 8: git diff Practice

- [x] Edit `index.html` (add `<h2>`)
- [x] Run `git diff`
- [x] Note: unstaged, which file changed

###### Part 9: Stage Files

- [x] `git add .`
- [x] `git status`
- [x] `git diff` (should be empty)
- [x] `git diff --staged`

###### Part 10: First Commit

- [x] `git commit -m "Add home login and signup pages"`
- [x] `git status` (clean tree)

###### Part 11: Commit History

- [x] `git log`
- [x] `git log --oneline`
- [x] Note first commit ID

###### Part 12: git show

- [x] `git show`
- [x] `git show <commit-id>`
- [x] Identify author, message, files, diff

###### Part 13: Another Change

- [x] Add `<nav>` block to `index.html`
- [x] `git status`
- [x] `git diff`

###### Part 14: Add File on GitHub

- [x] Create `about.html` directly on GitHub
- [x] Commit it on GitHub (not locally yet)

###### Part 15: Pull Changes

- [x] `git status`
- [x] `git pull`
- [x] Confirm `about.html` now local

###### Part 16: Push Local Code

- [x] `git add .`
- [x] `git commit -m "Update HTML pages"`
- [x] `git push`
- [x] Verify all 4 files on GitHub

###### Part 17: Create Branch

- [x] `git branch feature-pages`
- [x] `git branch` (list)
- [x] `git checkout feature-pages`
- [x] `git branch` (confirm switch)

###### Part 18: Branch Changes

- [x] Edit `index.html` (Feature Branch heading)
- [x] Edit `login.html` (login paragraph)
- [x] Edit `signup.html` (signup paragraph)

###### Part 19: Commit Branch Changes

- [x] `git status`
- [x] `git diff`
- [x] `git add .`
- [x] `git diff --staged`
- [x] `git commit -m "Improve authentication pages"`
- [x] `git log --oneline`
- [x] `git show`

###### Part 20: Push Branch

- [x] `git push -u origin feature-pages`
- [x] Verify branch visible on GitHub

###### Part 21: Create Pull Request

- [x] Open PR: `feature-pages` → `main`
- [x] Add meaningful title + description

###### Part 22: Review PR

- [x] Check changed files, additions/removals, commits
- [x] Leave 1 review comment
- [x] Resolve comment if needed

###### Part 23: Merge PR

- [x] Merge `feature-pages` into `main`
- [x] Confirm PR shows "Merged"

###### Part 24: Update Local Main

- [x] `git branch`
- [x] `git checkout main`
- [x] `git pull`
- [x] Confirm feature changes present locally

###### Final Deliverables

- [x] Repo has `index.html`, `login.html`, `signup.html`, `about.html`
- [x] At least 2 branches, multiple commits
- [x] Feature branch pushed, PR created/reviewed/merged
- [x] Create `answers.md` with all 15 Q&A answered
- [x] All required commands demonstrated
- [x] Submit repo URL

Submit https://github.com/itsdguptacg/Codinggita-git


### Notes 18/08/26
#### Delete a remote branch
`git push origin --delete <branch name>`
#### To see barnch
- locally : `git branch`
- remote : `git branch -r`
- all : `git branch -a`

#### Git ignore
create file with file name `.gitignore`

`git checkout -b <branch name>` = `git branch -c <branch name>`

### Notes 13/08/26
#### how to restore
##### file
Git checkout
```
git checkout <commit_id> -- <file name>
```

##### branch
- 1st
```
git reflog
```
- this is used to get id of any activity in git
- 2nd
```
git checkout -b feature/login <commit id from git reflog>
```

==`git log --oneline` displays the linear commit history of your current branch, while `git reflog` records a local history of every action you have taken, including branch changes, resets, and deleted commits==


### Notes 20/08/26
#### homework
- in assignment first we hat to unstage using `git restore --staged about.html` then `git restore about.html` works
- in assignment 3 make sure that restore snapshot should exist in that snap shot.
- **What happened to the content from Version 2 and Version 3?**
	- it is removed27 from current file but it is still stored in commit



### Notes 24/08/26
- temp switches to old commit id
```bash
git checkout commit_id
```
- 

## git stach
```bash
 git stash push -m "Your Message"
```


```bash
git stash
```

```bash
git stash push
```

```bash
git stash list
```

```bash
git stash apply
```

```bash
git stash apply <stash id> or <stash number>
```

```bash
git stash pop
```

```bash
git stash drop
```




- difference between pop , drop , apply


### Notes 11/09/2026

**git cherry pick** 

- Git cherry-pick allows you to apply a specific commit from one branch onto another without merging the entire branch.

```bash
git cherry-pick <commit-it>
```

- multi commit

```bash
git cherry-pick <commit1> <commit2> <commit3>
```


| Command | What it does |
|---|---|
| `git cherry-pick <commit-id>` | Applies one specific commit to the current branch. |
| `git cherry-pick <commit1> <commit2>` | Applies multiple specific commits. |
| `git cherry-pick A^..D` | Applies a consecutive range, including `A` and `D`. |
| `git cherry-pick --continue` | Continues after resolving a conflict. |
| `git cherry-pick --abort` | Cancels the current cherry-pick and returns to the previous state. |
| `git cherry-pick --no-commit <commit-id>` | Applies changes without automatically creating a commit. |
| `git cherry-pick -n <commit-id>` | Short form of `--no-commit`. |




---
### Further link
- 
---
### References
-

