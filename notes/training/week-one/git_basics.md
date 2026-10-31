
# Git Version 2

---

### What is git?
#### Version Control System
- Software designed to **record changes** made to files over time.
- Ability to **revert back** to a previous file version or project version.
- **Compare changes** made to files from one version to another.
- Version control any plain text file, not just source code.

<br>

### 3 stages of a file
1. Committed - safely stored in local database
2. Modified - file has been altered from the last commited version
3. Staged - take the changes to be commited

#### Untracked Files
- Untracked files - added to the project since the last commit snapshot.
- To track untracked file, add to git project to be staged. 

<br>

### 3 states of a git project
1. git directory - files commited and recorded to the project as version snapshot.
2. working directory - changes in files, not yet added to staging
3. staging area - files modified and added to be staged the the next commit snapshot

<br>

### Command Line
- `pwd` (print working directory) - returns current folder path location
- `cd` (change working directory) - move to another directory
  - `cd ..` - go one directory upwards 
  - `cd ~` - home folder
- `dir` (windows), `ls` (mac,linux) - list files in a directory
- `copy con` (windows), `touch` (mac,linux) - create a new empty file
- `mkdir` - create a new empty folder

<br>

### Configure Git
- `git --version` - verify installation
- `git config --global user.name "your-name"`  - to set username
- `git config --global user.email "your-email"`  - to set email address
- `git config --list`   - check config settings
- `git config user.name` - check specific setting (like the username)
- ~~`man git`~~ ~~full git manual~~
- `git help config` - to get specific git manual
- `git help` - shorter list of commands used most of the time

<br>

### Git Repository (repo)

#### virtual storage of a project
- `git init` - initializing a git repository

<br>

### Basic Commands of Everyday Git
- clear - clears window
- `git status` - check status of your project
- `git add <file>` - track files
- `git status -s` - concise status
- `git diff --staged --no-renames` - show not only status but the actual changes
- `git commit -a -m "message"` - short for stage(-a) + commit

<br>

### Extended Commands of Everyday Git

#### Push to Remote origin
- `git push origin main` - push to origin project

#### Check commit history
- `git log` - commit history
- `git log -1` - limit 1 commit history to show
- `git log --oneline` - concise commit history
- `git log --stat` - detailed commit information
- `git log --patch` - more detailed commit information

#### Remove and Move files
- `git rm <filename>` - stop tracking the file and remove a file from git project, stop tracking the file
- `git rm --cached <filename>` - untrack a file, but not remove in a git project
- `git mv <filename> <new filename>` - rename files

#### Branches
- branch - a lightweight movable pointer to a commit made in a project
- `git checkout -b <branch_name>` - create and switch to a new branch
- `git checkout <branch_name>` - switch to a specific branch

#### Stash
- `git stash` - to record current state of our working directory and staging area
- `git stash list` - list of work in progress changes 
- `git stash pop` - get change out of stash, into working directory

#### Merge
- `git merge <branch_name>` - merge the specified branch <branch_name> into the current branch
  - hit `i` for interactive mode to add commit message, when done hit `esc` key, followed by `:wq` (`w` saves changes `q` quits vim)

#### Reset
- `git reset <commit hash>` - moves commit from history, back into working directory
- `git reset --soft` - moves commits from history, back into staging area
- `git reset --hard` - moves changes(working directory and staging) to the trash, whn you messed with making changes 

#### Clone
- `git clone <url>` - clone origin(remote) repo






















