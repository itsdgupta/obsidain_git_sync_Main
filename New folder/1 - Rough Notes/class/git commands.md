20/08/2026

Status : #baby 

Tags : 

By Divyansh Gupta

# git commands

### Git Installation & Version

```bash
git --version
```
Checks the currently installed version of Git on your system.

### Git Configuration

```bash
git config --global user.name "Your Name"
```
Sets the global author name that will be associated with your commit history.

```bash
git config --global user.email "your-email@example.com"
```
Sets the global author email address that will be associated with your commits.

```bash
git config --list
```
Displays a list of all your current Git configuration values.

### Repository Initialization

```bash
git init
```
Initializes a new, empty Git repository in your current directory by creating a hidden `.git` folder.

### Staging Changes

```bash
git add index.html
```
Stages a specific file (e.g., `index.html` or `file.txt`) so its changes are ready to be included in the next commit.

```bash
git add .
```
Stages all untracked and modified files in the current directory for the next commit.

### Committing Changes

```bash
git commit -m "message"
```
Creates a saved checkpoint (commit) of your staged changes in the local repository, along with a descriptive message.

### Checking Repository State

```bash
git status
```
Shows the current state of your working directory and staging area, detailing which files are untracked, modified, or staged.

```bash
git diff
```
Shows the exact lines of code that have been modified in your working directory but have not yet been staged.

```bash
git diff --staged
```
Shows the exact changes that have been added to the staging area and are ready to be committed.

### Viewing Commit History

```bash
git log
```
Displays the full, detailed commit history of the repository, including authors, dates, and commit messages.

```bash
git log --oneline
```
Displays a shorter, compact version of the commit history, showing only the shortened commit ID and the commit message.

### Repository Initialization & Cloning

```bash
git init
```
Initializes a new local Git repository.

```bash
git clone <repository-url>
```
Creates a local copy of an existing remote repository, downloading all files, history, and branches.

### Tracking & Staging

```bash
git add .
```
Adds all modified and untracked files in the working directory to the staging area.

```bash
git status
```
Shows the current state of the working directory and the staging area.

```bash
git rm <file>
```
Removes a file from Git tracking and deletes it from your working directory, staging the deletion.

```bash
git rm --cached <file>
```
Removes a file from Git's tracking but keeps the file on your local computer.

### Committing & History

```bash
git commit -m "Describe the change"
```
Records the staged changes to the local repository with a descriptive message.

```bash
git show
```
Displays detailed information about a Git object, usually the latest commit (including author, date, and changes).

```bash
git log --oneline
```
Shows the commit history in a concise, single-line format to easily find commit IDs.

### Undoing Changes

```bash
git restore <file>
```
Discards unstaged changes in the working directory, restoring the file to the latest committed version.

```bash
git restore --staged <file>
```
Removes a file from the staging area without discarding the actual changes made to the file.

### Branching

```bash
git branch
```
Lists all local branches in the repository and highlights the current branch.

```bash
git branch -r
```
Lists all remote-tracking branches that Git knows about.

```bash
git branch -a
```
Lists both local and remote-tracking branches.

```bash
git branch <branch>
```
Creates a new local branch but does not switch to it.

```bash
git switch <branch>
```
Switches your working directory to the specified branch.

```bash
git switch -c <branch>
```
Creates a new branch and immediately switches to it in one step.

```bash
git checkout <branch>
```
An older alternative command used to switch between branches.

```bash
git branch -d <branch>
```
Safely deletes a local branch, preventing deletion if there are unmerged changes.

```bash
git branch -D <branch>
```
Force deletes a local branch regardless of its merge status.

### Remote Repositories & Syncing

```bash
git remote
```
Shows the names of the remote repositories connected to your local repository.

```bash
git remote -v
```
Displays the remote repository names along with their fetch and push URLs.

```bash
git remote add origin <url>
```
Connects your local repository to a remote repository URL and names it 'origin'.

```bash
git remote remove origin
```
Removes the connection to the specified remote repository.

```bash
git fetch
```
Downloads changes from the remote repository to your local repository without integrating them into your current branch.

```bash
git pull
```
Fetches changes from a remote repository and integrates (merges) them into your current local branch.

```bash
git push
```
Sends your committed local changes to the remote repository.

```bash
git push -u origin <branch>
```
Pushes a local branch to the remote repository for the first time and sets up the upstream tracking relationship.

```bash
git push origin --delete <branch>
```
Deletes a specified branch from the remote repository.

### Reviewing Changes & Merging

```bash
git diff
```
Shows the differences between your working directory and the staging area.

```bash
git diff --staged
```
Shows the differences between the staging area and the last commit.

```bash
git merge <branch>
```
Combines the changes from the specified branch into your current active branch.


### Git Checkout

Switch to an existing branch:
```bash
git checkout <branch>
```

Create a new branch and switch to it immediately:
```bash
git checkout -b <branch>
```

Restore a specific file from an older commit:
```bash
git checkout <commit> -- <file>
```

Temporarily switch to a specific tag or old commit (detached HEAD state):
```bash
git checkout <tag-or-commit>
```

Create a new branch starting from a specific older commit:
```bash
git checkout -b <branch> <commit>
```

Create a local branch that tracks an existing remote branch:
```bash
git checkout -b <branch> <remote>/<branch>
```

### Git Restore & Recovery

View a log of all recent local reference updates (useful for recovering deleted branches):
```bash
git reflog
```

Download objects and refs from another repository without merging:
```bash
git fetch <remote>
```

Push a newly recreated local branch to the remote repository and set upstream tracking:
```bash
git push -u <remote> <branch>
```

Create a new commit that undoes the changes of a previous commit:
```bash
git revert <commit>
```

### Git Tag

Create a simple, lightweight tag at the current commit:
```bash
git tag <tag-name>
```

Create an annotated tag (recommended for releases) containing a custom message:
```bash
git tag -a <tag-name> -m "<message>"
```

List all tags present in the local repository:
```bash
git tag
```

Display the details and commit information associated with a specific tag:
```bash
git show <tag-name>
```

Show a concise, one-line summary of the commit history:
```bash
git log --oneline
```

Retroactively add an annotated tag to a specific past commit:
```bash
git tag -a <tag-name> <commit> -m "<message>"
```

Push a specific tag to the remote repository:
```bash
git push <remote> <tag-name>
```

Push all local tags to the remote repository at once:
```bash
git push <remote> --tags
```

Delete a tag from your local repository:
```bash
git tag -d <tag-name>
```

Delete a tag from the remote repository:
```bash
git push <remote> --delete <tag-name>
```

### Git Commit Amend

Replaces the latest commit with a new commit containing the current staged changes and opens the configured editor to edit the message.
```bash
git commit --amend
```

Modifies the latest commit and directly provides the new commit message without opening an editor.
```bash
git commit --amend -m "message"
```

Replaces the latest commit with new staged changes but keeps the existing commit message.
```bash
git commit --amend --no-edit
```

Creates a standard commit using a specified message.
```bash
git commit -m "message"
```

Used to modify older commits in the branch history rather than just the latest one.
```bash
git rebase -i
```

Stages a specific newly created or modified file (e.g., style.css or signup.css) for the next commit.
```bash
git add style.css
```

Updates the staging area with all new, modified, or deleted files in the current directory.
```bash
git add .
```

Checks the current status of the working directory and the staging area.
```bash
git status
```

Displays the three most recent commits in a condensed single-line format.
```bash
git log --oneline -3
```

Displays the statistics and file changes of the most recent commit.
```bash
git show --stat HEAD
```

Shows the full details and differences of the most recent commit.
```bash
git show HEAD
```

Shows the changes currently in the staging area compared with HEAD.
```bash
git diff --cached
```

Shows the differences between the working directory and the latest commit.
```bash
git diff HEAD
```

A safer option used to push amended or rewritten commits to a remote shared branch.
```bash
git push --force-with-lease
```

Forcefully pushes changes to a remote repository, which should be avoided casually on shared branches.
```bash
git push --force
```

Vim commands
```bash
i = enter insert mode
esc = exit insert mode
:wq = save and exit vim
:q! = not save and exit
```






---
### Further link
- 
---
### References
- 