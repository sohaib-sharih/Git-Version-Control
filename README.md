### Topics

| Topics                                            | Headings                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1.0 Installation                                  | 1.1 Setting up Environment Variables <br>1.2 Configuration your VSCode with GitHub<br>1.3 3 Different Levels of Git Config<br>1.4 Types of Repositories<br>1.5 How configuration precedence works?<br>1.6                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 2.0 Git Workflow                                  | 2.0 Git workflow<br>2.1 Does the file remain in the Staging Area after commit?<br>2.2 Steps of a Commit Cycle                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 3.0 Reverting to Commits                          | 3.0 Topic: Reverting to commits<br>3.1 Analysis of Head detached state<br>3.2 Next steps after reverting using git checkout HEAD~1 one.py<br>3.3 Restore your commits<br>3.4 Key Takeaways<br>3.5 Difference between `git checkout hash`, `git checkout main` and `git checkout HEAD~2 one.py`<br>3.6 How to save detached Head to a Current branch or a New branch? (GPT Answer)<br>3.7 Key Differences Between `git diff` and `git checkout<br>3.8 Additional Notes<br>3.9 Difference between Git Merge and Git Cherry-Pick commands                                                                                                                       |
| 4.0 Deleting files and reverting to deleted files | 4.0 Topic: Deleting files and reverting to deleted files<br>4.1 How to restore Deleted Files?<br>4.2 Deleting a specific commit while keeping all other recent and earlier commits in history<br>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 5.0 Git Ignore                                    | 5.0 Topic: Git Ignore<br>5.1 Git ignore file types                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 6.0 Renaming Files                                | 6.0 Topic: Renaming Files<br>6.1 How to un stage a file?<br>6.2 Why doe we use -- double dash after checkout option?                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 7.0 GitHub and Remotes                            | 7.1 Introduction to github<br>7.2 Steps to creating a new Repository using HTTPS and SSH<br>7.3 Creating a repository using HTTPS<br>7.4 HTTPS METHOD<br>7.5 Using the SSH Key<br>7.6 SSH METHOD (using Default Location)<br>7.7 How to save SSH key in a Custom location?<br>7.8 Difference between *eval "(ssh-agent -s)"* and *ssh-agent bash*<br>7.9 Update Your Git Remote to Use SSH<br>7.10 Different types of Cryptographic Methods to generate SSH Key<br>7.11 Summary of Commands using SSH Method<br>7.12 How to check which SSH Key is being used by local repository?<br>7.13 How to update/change an SSH connection to your Remote connection? |
| 8.0 Git Pull                                      | 8.1 What is the purpose of using GIT PULL and when to use it?<br>8.2 Interpretation of the git log --oneline<br>8.3 How to collaborate between Local and Remote Repositories.<br>8.4 Managing multiple commits to the same file<br>8.5 Merging: Resolving Conflict<br>8.6 Tracking and raising issues                                                                                                                                                                                                                                                                                                                                                        |
| 9.0 Branching, Merging and Rebasing               | 9.1 Merge Types<br>9.2 Topic: Conflicts during merge<br>9.3 Git stash topic<br>9.4 Moving forward: Apply the stash on another branch<br>9.5 git stash show, git stash clear<br>9.6 How stash works (applies on the current branch or globally?)                                                                                                                                                                                                                                                                                                                                                                                                              |
| 10.0 Rebase                                       | 10.0 Rebase<br>10.1 Difference between git merge and git rebase<br>10.2 When to use git rebase?                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 11.0 Git clone                                    | 11.0 Git clone<br>11.1 Cloning from git repository                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 12.0 Forking                                      | 12.0 Forking<br>12.1 What is forking used for?<br>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 13.0 Layout of Github \| Git Branches             | 13.0 Layout of Github Remote Repository/Dashboard<br>13.1 Git Branches                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 14.0 Scenerios                                    | 14.1 How to use a local repository for both Github and gitLab?<br>14.2 How do you initialize git one level up after already having pushed the current folder to github & gitlab?<br>14.3 Modifying an existing git repo with new sub folders and files<br>14.3.1 How to FIX it? *Option 1*<br>14.3.2 How to FIX it? *Option 2*<br>14.3.3 How to use rebase option(GPT Answer)<br>14.3.4 How to ignore a tracked file + subfolders                                                                                                                                                                                                                            |
# 1.0 Installation

2. Install Git from [[https://git-scm.com/downloads/win]]
3. Check your installation by running **git --version** on your command prompt/Windows Powershell/Bash terminal.
4. If you receive an error, after installation, then you need to add the path in your System Variables at Edit Environment Variables section.
### 1.1 Setup Environment Variables

1. Get your Git path by using **where git** command on Command prompt or **bash shell** that you can open through **VsCode** or simply search for **bash** on your Win search bar.
2. The path may look like: `C:\Program Files\Git\mingw64\bin\git.exe`
3. Search for Environment Variables on Windows, then open Environment Variables, Under System Variables click on **path**, add **new** and enter the **path**. Press ok, close the previously opened terminals, and restart the PC if need be.
4. Open a new terminal and check **where git** and **git --version**, it should give an output of the version.

### 1.2 Configuration your VSCode with GitHub

1. `git config --global user.name:` "john"
2. `git config --global user.email: "john@gmail.com"`
3. `git config --list` This enlists the configuration for *global, system and repository-specific(if initialized)* settings.
4. To check if your working or current directory is initialized or not, it will return a bool, use: `git rev-parse --is-inside-work-tree`
5. The purpose of **git configuration** is to tell **git** the details of the user + user's account you will be applying changes to or working with.
6. **Note:** This allows you to setup your github account and integrate with your **local vscode** so you don't have to connect each time you perform `git init` command.
7. **Local configuration**: In steps 1 and 2, it allows you to setup your configuration ***globally***, if you run those commands each time you work on a different folder or project, then these commands will **override** your global settings, therefore for local and **repository specific settings** to take affect such that they don't override, you can do the following:
	a. `git config user.name: "john"`
	b. `git config user.email: "john@gmail.com"`
	c. These values will now be used only for commits in the current repository.
	d. To check the **local configuration**: `git config --local --list`
16. To check **all levels of configuration** (local, global & system): **git config --list  --show-origin.** *This shows the source file for each configuration, such as `.git/config` (local), `~/.gitconfig` (global), or `/etc/gitconfig` (system).*

### 1.3 3 Different Levels of Git Config

1. System Level
2. Global Level
3. Local Level

#### System Level Configuration

1. This is the highest level where all users who use the system can use Git in which Git is installed.
2. Settings are defined using: `git config -system` 
3. These settings are saved at `/etc/gitconfig` file

#### Global Level Configuration

1. This refers to all user settings to all **repositories**.
2. Settings are defined using: `git config -global`
3. These are saved at `~/gitconfig` file. *On Windows it would be `/Users/gitconfig`*

#### Local Level Configuration

1. This refers to the USER at a repository level.
2. Settings are defined using: `git config --local OR git config`
3. These are saved at `.git/gitconfig` file.

**NOTE:** *Local* overrides *Global*, and *Global* overrides *System level* **configuration.** Failing to setting the configuration settings, Git will throw a warning, therefore *user.name* and *user.email* needs to be setup and configured.

### 1.4 Types of Repositories

1. **Local Repository:** This is the repository that resides on your local system, as a .git folder inside your project folder.
2. **Remote Repository:** This is the repository that lives outside your local system, usually on a remote server that has its own .git folder. Teams use the remote repository to exchange and share data, and also update changes.

### 1.5 How configuration precedence works?

Git applies settings in the following order (highest to lowest priority):

1. **Repository-Specific or Local (`.git/config`)**:
	a. Affects only the current repository.
	b. Does not alter global or system settings.
2. **Global (`~/.gitconfig` or `~/.config/git/config`)**:
	a. Applies to all repositories unless overridden by local settings.
3. System (`/etc/gitconfig`):
	a. Applies system-wide, unless overridden by global or local setting.

If a setting exists at multiple levels, the **repository-specific one** (`--local`) takes precedence.
### 1.6 Git Initialization

1. This is an important step before your start to establish a connection with your repository. This step allows you to setup **version control** for a project.
2. **git init** command allows you to initialize your directory of files and folders that you are working with. It creates hidden .git folder that contains all the working and configuration files that are needed to *store, change, add, update and delete* configuration of your **working directory.**
3. When you run the `git init` command, it creates a folder called .git folder, which initially is *empty.* This remains empty until you add and commit your first **working copy** or **working directory** as an *initial version.*
4. It sets up the necessary structure for Git to track changes to files within the directory.

Some important Git Commands (GPT Answer):

| Command | Description                                                                       | Explanation                                                                                                                              |
| ------- | --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| ls -ls  | Lists files with their sizes and permissions in long format, sorted by file size. | - `-l`: Long format (detailed file info: permissions, owner, size, timestamp).  <br>- `-s`: Shows file size in blocks before each entry. |
| ls -lrt | Lists files in long format, sorted by modification time (oldest first).           | - `-l`: Long format.  <br>- `-r`: Reverses order (oldest files first).  <br>- `-t`: Sorts by modification time.                          |
| ls -la  | Lists all files (including hidden ones) in long format.                           | - `-l`: Long format.  <br>- `-a`: Includes hidden files (files starting with `.`).                                                       |
| a       | Reveals hidden files                                                              |                                                                                                                                          |
| t       | sorts files in order of time                                                      |                                                                                                                                          |
| l       | indicates folder content in **long format**                                       |                                                                                                                                          |
| s       | indicates folder content in terms of file size.                                   |                                                                                                                                          |
| r       | shows content in reverse order (OLDEST to NEWEST)                                 |                                                                                                                                          |

### 1.7 Importance of README.md file

1. If you create a repository without the README.md file, you will have to initialize the repository locally by using the following commands and sequence:

```
git clone <repository-url>
cd <repository-name>
echo "# Project Title" > README.md
git add README.md
git commit -m "Initial commit"
git push origin main

```

2. If you choose to create a repository with the README.md file, then the repo gets initialized automatically which means that it will create a default branch called **main.**

Key difference between creating a repo with and without the readme.md file:

| Aspect          | Without `README.md` Option     | With `README.md` Option           |
| --------------- | ------------------------------ | --------------------------------- |
| Initial Content | Repository is empty.           | Includes a `README.md` file.      |
| Default Branch  | Not created initially.         | Default branch is `main`.         |
| Immediate Clone | Requires local initialization. | Can be cloned immediately.        |
| Usage           | For fully custom setup.        | For quick project initialization. |
3. **Initialization** creates a default branch. The name of the branch depends on the default settings in your local system as well as the settings at your git hub repository. If you initialize your local repo using **git init**, then it will create a default branch name called ***master***. If you create a repository with the *readme.md* file on github, then it gets initialized using the common name called ***main**.* However, we can change both the settings in the following way:

### 1.8 Change *default branch settings* locally:

***Before creating the repository***, you should follow these steps to change the default branch name:

```
git config --global init.defaultBranch my-branch
```

You can also check the current default branch name by the following command:

```
git config --list

Output:
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master  ---> DEFAULT BRANCH NAME
user.name=Sohaib Sharih
user.email=sohaib.sharih@gmail.com
filter.lfs.smudge=git-lfs smudge -- %f

```

### 1.9 Change *default branch settings* on github repository:

1. Click on the github repository you want to change the name of default branch name.
2. On top right, click on *settings*. Scroll down under Default Branch, you can rename the default branch name mentioned in the field.


# 2.0 Topic: Git Workflow(simplilearn)

1. Git maintains 3 snapshots of a file in 3 separate directories.
	a. Working Directory: Git Status will indicate ***Untracked***
	b. Staging Area (.git/index file): Git status will indicate **Tracked***
	c. Local Repository
2. When a file is created after initializing the git repository, it is stored as **untracked file*** in the working directory. Then, using the **git add** command, it allows you to save the file in the **staging area(.git/index file)**, which means that the file has been moved from the **working directory*** to the **staging area**. Finally, it is then moved to the **local repository** using the **git commit command.**
3. When you use the **git commit** command, the Working Directory becomes clean, which means that the file in the **local repository** is in sync with the **working repository/directory.**
4. **Managing and viewing changes:** `git log`
5. **Modifying a file** entails update, add and commit.
6. `git log --oneline` will give a list of changes in a single line, rather than details in a chronological order with just git log command.

```
Steps:
49. Create a file in the working directory
50. Using git add. command, move the file from the Working Repo to the Staging Area.
51. Finally, commit the changes using git commit -m 'second change', to push the file from the staging area to the local repository.
52. Check the git status

OUTPUT:

$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

NOTE: The working repository or Working tree is CLEAN now, which means that the local repo is in sync with the working repo.


```

7. **git commit** command allows you to open the commit log to enter your changes manually in the commit file, instead of saving it using the CLI `git commit -m 'add commit message'`

```
git commit

OUTPUT

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
# Your branch is ahead of 'origin/main' by 1 commit.
#   (use "git push" to publish your local commits)
#
# Changes to be committed:
#       modified:   one.py
#
This is the third change  ----> This is the manual change in the file, .git/GITCOMMITMSG

```
8. **Tracking:** is the ability to identify changes between different versions of the same file, spread across various **repositories.**
9. There are 2 ways to check the difference between a ***working directory*** and a ***staged file***, and between a ***staged file*** and the last commit of the same file in ***local repository***

	a. **git diff:** The difference between a Working Directory and a Staged file.
	b. **git diff --staged**: The difference between a Staged file and the **last commit** of the same file in the local repository.
	
```
	git diff --staged OR git diff HEAD:
OUTPUT:
$ git diff --staged
diff --git a/one.py b/one.py
index 95f3493..6ce4307 100644
--- a/one.py
+++ b/one.py
@@ -25,5 +25,5 @@ print(answer)
 print(random.randint(num1, 20))

 """
-Lets revise classes.
+Lets revise classes. hello
 """
\ No newline at end of file

git diff

OUTPUT:

diff --git a/one.py b/one.py
index 95f3493..6ce4307 100644
--- a/one.py
+++ b/one.py
@@ -25,5 +25,5 @@ print(answer)
 print(random.randint(num1, 20))

 """
-Lets revise classes.
+Lets revise classes. hello
 """
\ No newline at end of file
```
	
10. **HEAD:** The latest commit of a file is identified by a pointer called HEAD. `Git diff --staged` is the same as `git diff HEAD`
11. When the number of commits have reached a certain number of changes, then you can use `git diff <commit hashcode>` to retrieve the difference between changes and last commit.

![[gitworkflow1.PNG]]


| Local Repository         | Commits |
| ------------------------ | ------- |
| Last Commit(Most recent) | HEAD    |
| 2nd last commit          | HEAD ~1 |
| 3rd Last commit          | HEAD ~2 |
12. Git indicates the changes in the form of ***additions*** as ++ , and ***deletions*** as --

*DEMO (using hash and diff option)*

```
git diff one.py

output:
Before making any changes after the last commit, using the 'git diff one.py' command will not give any output because the file in the LOCAL REPOSITORY is synced with the file in the STAGING AREA.

------------------

After making a change in the working file, `git diff one.py` will give the following output:

diff --git a/one.py b/one.py
index 19436f9..f1335a5 100644
--- a/one.py
+++ b/one.py
@@ -29,4 +29,5 @@ Lets revise classes. hello

 1. this refers to a 6th change
 this is the 6th change
+this is the 7th change ----> Modified, not added to staging area, nor commited.
 """
\ No newline at end of file


-------------------------

NOTE: After STAGING and COMMITTING changes, 'git diff one.py' and 'git diff --staged' will give no output, because all the files are SYNCED.

---------------------------------

git log --oneline

OUTPUT:

758b687 (HEAD -> main) 7th change
7fe0cc4 6th change
dc92c4a 5th change
371b418 fourth change
9705fa1 This is the third change
6dbfe40 second change
594b9f6 (origin/main, origin/HEAD) first commit
20f98b7 Initial commit

---------------------------

Select the HASH to track the difference between the Last commit and the specified commit.

git diff dc92c4a

OUTPUT:
diff --git a/one.py b/one.py
index 5f67726..f1335a5 100644
--- a/one.py
+++ b/one.py
@@ -28,4 +28,6 @@ print(random.randint(num1, 20))
 Lets revise classes. hello

 1. this refers to a 6th change
+this is the 6th change
+this is the 7th change
 """
\ No newline at end of file
```

### 2.1 Does the file remain in the Staging Area after commit? (GPT Answer)

| Stage                | Purpose                                                                                            |
| -------------------- | -------------------------------------------------------------------------------------------------- |
| Working Directory    | Where you make changes to your files. These changes are **not yet tracked** until they are staged. |
| Staging Area (Index) | Temporarily holds changes before committing. Helps you prepare what will be committed next.        |
| Local Repository     | Stores the committed snapshots permanently in `.git/` as a new version history.                    |
### 2.2 Steps of a Commit Cycle(gpt answer)

1. You modify a file (`file1.txt`). *This change is in the Working Directory.*
2. You stage the file: `git add .` *The file moves to the Staging Area, and the last changes are SAVED in the staging area.*
3. Commit the changes (git commit -m 'message'): *The file is moved to the Local Repository. The Staging Area is now clean, which means that the STAGED AREA FILES are now part of the repository history*
4. The Working Directory and the Local Repository are now Synced.
5. NOTE: Staging Area does not retain any files or previous commits.
6. After checking the **git status** , the working tree will indicate its clean, which means that *working directory, staging area and local repository are now in sync, but the Local repository and the Remote repository are still not synced.*
7. After pushing your local repository to github or gitlab, then the Local Repository becomes synced with the **remote repository.**

## 3.0 Topic: Reverting to commits(sl)

1. **git log:** List details of the commit associated with the file
2. **git checkout:** This will stage the file, followed by the details of the commit you want to refer to.
3. **git status:** This will share the command to **unstage** the file.
4. **git reset:** This will remove the file from the **staging area.**

**git checkout HEAD~1 < filename >**

1. This helps you revert to the changes committed in ***second last commit.*** Since HEAD refers to the last/most recent commit.
2. This command allows you to revert to changes that were commited on HEAD~1, which brings back the file to the same **state** as it was in the **HEAD~1** commit level.
3. It also places that state in the ***STAGING AREA.***
4. As next steps, you can check by `git status`: 

```
git log --online

OUTPUT:

74cbd8f (HEAD) 7th commit
240543e 6th change
dc92c4a 5th change ----> HEAD detached from dc92c4a
371b418 fourth change
9705fa1 This is the third change
6dbfe40 second change
594b9f6 (origin/main, origin/HEAD) first commit
20f98b7 Initial commit

-------------------------------------------------
git checkout HEAD one.py(Experiment with HEAD)

OUTPUT:
Updated 0 paths from 1c3a82e

------------------------------------

git status:

OUTPUT:

HEAD detached from dc92c4a
nothing to commit, working tree clean
----------------------------------------------------

git checkout HEAD~1 one.py (Experiment with HEAD~1)

OUTPUT:

Updated 1 path from 1c3a82e
----------------------------------------
git status:

HEAD detached from dc92c4a
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   one.py

NOTE: Key difference between HEAD and HEAD~1 option output is that in one it indicates the working tree is clean, in the other it indicates that the file is now modified and ready to be COMMITED from the STAGING AREA.

INTERPRETATION of HEAD detached

74. Head detached from dc92c4a
75. Once you use the **git checkout HEAD~1 one.py** command, it reverts to the 2nd last commit which is of 240543e commit level.
76. git status --> command entails that 240543e commit becomes the HEAD level commit and HEAD has been DETACHED from dc92c4a commit level and MOVED to the STAGING AREA.
77. It does not mean that all other higher level commits are discarded, they are still there, it only means that the file `one.py` was restored from an earlier commit and is now **staged** to be committed.

```

### 3.1 Analysis of Head detached state

1. git checkout HEAD one.py *does not move the HEAD to another level, it only removes the pointer that was pointing on the **main branch.***
2. In other words, the HEAD is no longer pointing to the **main branch** or to any branch.
3. After running the git status command, the line `modified: one.py` indicates that `one.py` has been staged for the next commit.
4. Since you used `git checkout HEAD~1 one.py`, the file `one.py` was restored from an earlier commit and is now **staged** to be committed.

### 3.2 Next steps after reverting using git checkout HEAD~1 one.py

1. **Option 1** is that you can commit the changes and will be added to the LAST COMMIT level, and all other levels remain intact.
2. **Option 2** is to **restore** the previous changes in the working directory. See below:
### 3.3 Restore your commits

1. If you want to undo the changes and return to the latest commit:

```
git restore --staged one.py  # Unstage the file
git checkout main            # Move back to the main branch

```

2. If you want to discard the change **permanently:**

```
git restore one.py
```
### 3.4 Key Takeaways

- You **did not** actually move HEAD back one commit.
- Instead, you **checked out only `one.py` from HEAD~1**, which modified and staged it.
- Your HEAD is **detached** at commit `dc92c4a` (5th change), meaning you are not currently on `main`.

```
EXPERIMENT Key Learnings

86. git checkout 371b418

OUTPUT:

Note: switching to '371b418'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 371b418 fourth change

----------------------------------------------------
GIT STATUS

OUTPUT:

HEAD detached at 371b418
nothing to commit, working tree clea
-------------------------------------------------------------------
git log --oneline

OUTPUT:

371b418 (HEAD) fourth change
9705fa1 This is the third change
6dbfe40 second change
594b9f6 (origin/main, origin/HEAD) first commit
20f98b7 Initial commit
-------------------------------------------------------

```

### 3.5 Difference between `git checkout hash`, `git checkout main` and `git checkout HEAD~2 one.py` (GPT Answer)

### Understanding `git checkout` Variants(GPT Answer)

| Command                      | Purpose                                | Behavior                                                                                              |
| ---------------------------- | -------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `git checkout <commit-hash>` | Switches to a specific commit          | Moves `HEAD` to the commit, causing a **detached HEAD** state                                         |
| `git checkout main`          | Switches to a branch                   | Moves `HEAD` back to the `main` branch and **discards any detached HEAD changes**                     |
| `git checkout HEAD~2 one.py` | Checks out a file from an older commit | Restores `one.py` from **2 commits before HEAD** but does **not** switch the branch or commit history |
#### Initial Commit History

```
git log --oneline
OUTPUT:
d9f1a7b (HEAD -> main) 5th change
b6e2c89 4th change
c3f4d20 3rd change
a9d8b65 2nd change
x1y2z3w Initial commit

```

#### Case 1: `git checkout <commit-hash>` (Detached HEAD)(GPT answer)

```
git checkout c3f4d20
OUTPUT:

87. `HEAD` moves to commit `c3f4d20` (3rd change).
88. You are now in **detached HEAD state**.
89. Running `git status` shows

HEAD detached at c3f4d20
nothing to commit, working tree clean

```

#### If you make changes to the file:(GPT answer)

```
echo "New changes" >> file.txt
git add file.txt
git commit -m "New change after detached HEAD"

NOTE: A new commit is created, but **it does not belong to any branch**.

If you RUN:

git checkout main

OUTPUT:

90. Your new commit **disappears** (because it was not part of any branch).
91. You are back at `d9f1a7b (5th change)` on `main`.



```

#### Case 2: `git checkout main` (gpt answer)

1. This command **moves HEAD back to `main`**.
2. Any commits made in detached HEAD mode **will be lost** (unless you create a new branch before switching).

If you want to keep the detached HEAD changes:

```
git branch new-feature  # Save the detached HEAD as a new branch
git checkout main       # Now safe to switch back

```

#### Case 3: `git checkout HEAD~2 one.py` (gpt answer)

1. This command does **not** switch commits. Instead, it **restores a single file from an older commit**.
2. `HEAD~2` means **2 commits before the current HEAD** (which is `b6e2c89`).
3. `file.txt` is restored from that commit.
4. You can now **STAGE and COMMIT this as a new change**.

#### Key Difference

1. This does **not** move HEAD, it just restores the **content** of `file.txt` from an old commit.
2. You are still on `main`, so this change is tracked in the branch history.

### 3.6 How to save detached Head to a Current branch or a New branch? (GPT Answer)

There are 2 ways to save a detached HEAD as a result of `git checkout hashCommit`:
1. Create a new branch and Merge
2. **Cherry pick** the commit to Main (your branch)

#### Option 1: Create a new branch and Merge

1. This is the **recommended** approach because detached commits can be lost if you switch branches.
2. Create a new branch from the detached HEAD state:

```
git checkout -b new-feature-branch

104. This saves your current changes under a new branch.
105. You are now working on `new-feature-branch`.
```

3. Switch back to the original branch (e.g., `main`) and merge:
```
git checkout main
git merge new-feature-branch

NOTE: Your new changes in detached mode are now part of the MAIN branch.

```

### There are 2 ways to merge

1. Use Git merge command with a Hash of Commit
	a. Use get checkout hash of commit to detach HEAD
	b. Make file changes
2. Use git merge with a new branch that is created in Detached mode.

Example (git merge command after commit made in DETACHED MODE)

```
git log --oneline (check log, and copy hash commit)

OUTPUT:

f89f1fd (HEAD -> master) Merge branch 'newBranch' Merging the newBranch with master
2bc1dfe (newBranch) new merge commit
7944c4f Merge commit '406e5c0'
406e5c0 creating a new file in detached mode, then merging
4cf3817 fourth
59ad487 7th commit
0b57667 5th commit
79dfec5 (origin/master) fourth
e2de355 third
4d72b37 second commit
6caa6f3 first commit

-----------------------------------------------

1. git checkout 406e5c0 (to detach HEAD)
2. touch mergeTwo.py
3. git add .
4. git commit -m 'detached 406e5c0, added mergeTwo.py file'
5. git log --oneline (in DETACHED MODE)

OUTPUT:

f21f532 (HEAD) detached 406e5c0, added mergeTwo.py file
406e5c0 creating a new file in detached mode, then merging
4cf3817 fourth
6caa6f3 first commit

-----------------------------------------

1. Copy the new commit -> f21f532
2. git checkout master (return to the master branch by point HEAD back to last commit)
3. git merge f21f532
4. A new commit needs to be made, an editor on terminal will open to write new commit.
5. <Merge commit after f21f532 commit was made in detached mode> --> Editor Commit Txt.
6. git log --oneline

OUTPUT:
dd8bb55 (HEAD -> master) Merge commit 'f21f532' Merge commit after f21f532 commit was made in detached mode
f21f532 detached 406e5c0, added mergeTwo.py file
f89f1fd Merge branch 'newBranch' Merging the newBranch with master
2bc1dfe (newBranch) new merge commit
7944c4f Merge commit '406e5c0'
406e5c0 creating a new file in detached mode, then merging
4cf3817 fourth
59ad487 7th commit
0b57667 5th commit
79dfec5 (origin/master) fourth
e2de355 third
4d72b37 second commit
6caa6f3 first commit

```

Example (Using git merge command after creating NEW BRANCH while in DETACHED MODE.)

```
git log --oneline (Check current log commits and select commit)

OUTPUT:

dd8bb55 (HEAD -> master) Merge commit 'f21f532' Merge commit after f21f532 commit was made in detached mode
f21f532 detached 406e5c0, added mergeTwo.py file
f89f1fd Merge branch 'newBranch' Merging the newBranch with master
2bc1dfe (newBranch) new merge commit
7944c4f Merge commit '406e5c0'
406e5c0 creating a new file in detached mode, then merging
4cf3817 fourth
59ad487 7th commit
0b57667 5th commit
79dfec5 (origin/master) fourth
e2de355 third
4d72b37 second commit
6caa6f3 first commit

--------------------------------------------

git checkout 59ad487 --> Select this commit to checkout and DETACH HEAD

OUTPUT:

Note: switching to '59ad487'.

You are in 'detached HEAD' state.

HEAD is now at 59ad487 7th commit

----------------------------------------------

$ git checkout -b mergeBranch

OUTPUT:
Switched to a new branch 'mergeBranch'

NOTE: This command allows you to create a NEW BRANCH and also POINT THE HEAD TO THE NEW BRANCH, which means that the DETACHED head from 59ad487 commit, will be stacked up inside the new branch

--------------------------------------------------

git log --oneline mergeBranch

OUTPUT:

59ad487 (HEAD -> mergeBranch) 7th commit  ---> This branch was DETACHED and now is HEAD
0b57667 5th commit
79dfec5 (origin/master) fourth
e2de355 third
4d72b37 second commit
6caa6f3 first commit

-----------------------------------------------

```

**NOTE:** If you want, instead of using `git checkout -b` command, you can checkout to a new branch, then and merge the commit that was made in DETACHED mode to the new branch. Example shown below:

Example: How to merge the last commit made in DETACHED branch into a new branch

```
git checkout mergeBranch
git log --oneline

OUTPUT:

59ad487 (HEAD -> mergeBranch) 7th commit
0b57667 5th commit
79dfec5 (origin/master) fourth
e2de355 third
4d72b37 second commit
6caa6f3 first commit

----------------------------

git checkout e2de355 (Detach HEAD at this commit)

OUTPUT:

Note: switching to 'e2de355'.

-----------------------------------

1. Add a new file
2. Made a new commit in DETACHED mode.
3. use git log --oneline to COPY the last HASH COMMIT
4. git checkout mergeBranch
5. git merge 89f38b5

git log --oneline (list commits after last commit in DETACHED mode)

OUTPUT:

89f38b5 (HEAD) new Commit ----------> Copy this HASH and checkout to mergeBranch
e2de355 third
4d72b37 second commit
6caa6f3 first commit

---------------------
git checkout mergeBranch
git merge 89f38b5

OUTPUT:

1. It will prompt to write a COMMIT Message on Terminal EDITOR.
2. Save it then it will automatically make that commit as the HEAD level commit of the current branch, mergeBranch.

------------------------------
git log --oneline(after Commit has been saved in mergeBranch)

OUTPUT:

d714d6b (HEAD -> mergeBranch) Merge commit '89f38b5' into mergeBranch --> Commit made   ---------------------------------------------------------------outside DETACHED mode.
89f38b5 new Commit -----> New commit made inside DETACHED MODE.
59ad487 7th commit (Carried from previous history of mergeBranch)
0b57667 5th commit (Carried from previous history of mergeBranch)
79dfec5 (origin/master) fourth (Carried from previous history of mergeBranch)
e2de355 third ------> It was Detached from here.
4d72b37 second commit
6caa6f3 first commit

------------------------------

```
### Option 2: Cherry-Pick the Commit to Main(or any selected branch)

## Cherry-pick option(gpt answer)

1. Cherry pick is used to assign a specific commit changes and merge it with your current branch.
2. If there are no conflicts, the cherry picked commit becomes your HEAD now.
3. If there is a conflict, you need to resolve it then **add it to the STAGING AREA**, then use `git cherry-pick 79dfec5 --continue`. *It will then become your HEAD level commit along with all other commit history(of the current branch) attached to it.*
4. Once you use git cherry-pick, it then adds it to the HEAD with a new HASH assigned to it.
5. You can ***cherry-pick*** a hash commit of another branch and merge it with another branch.

Example:

```
git checkout master
git log --oneline (check the commit history and copy the hash of commit)

OUTPUT:

59ad487 (HEAD -> master) 7th commit
0b57667 5th commit
79dfec5 (origin/master) fourth
e2de355 third
4d72b37 second commit
6caa6f3 (main) first commit

---------------------------------------

Select your commit. Example 79dfec5

git checkout main
git log --oneline

OUTPUT:

6caa6f3 (HEAD -> main) first commit

-----------------------------------

Next, run the following command:

git checkout 79dfec5

OUTPUT:

git cherry-pick 79dfec5
[main 4cf3817] fourth
 Date: Thu Feb 13 20:49:33 2025 +0500
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 six.py

NOTE: There is no conflict to resolve, therefore this command has made 79dfec5 hash commit the HEAD level commit of the current branch.

---------------------------------------------

Check the current branch Log history of commits

git log --oneline

OUTPUT:

4cf3817 (HEAD -> main) fourth
6caa6f3 first commit

```

6. Now that you know what ***git cherry-pick*** command is used for, you can also use it by ***detaching*** the HEAD from the current branch, and then make changes to the selected ***hash commit***, followed by adding and commiting the changes at ***deatched state.*** Then all you need to do is simply use the ***git log --oneline*** command to list down the hash commits, and copy the newly generated hash commit, then git checkout < main/anybranch>. Finally use the git cherry-pick < hash commit> (paste the copied hash from the detached state.)

Example:

```
git log --oneline (check the log history to select a specific HASH COMMIT)

OUTPUT:

4cf3817 (HEAD -> main) fourth
6caa6f3 first commit

--------------------------------

git checkout 6caa6f3 (Detach the head from this hash commit)

OUTPUT:

Note: switching to '6caa6f3'.

You are in 'detached HEAD' state. 

HEAD is now at 6caa6f3 first commit

---------------------------------------------

Create a new file touch newFile.py in DETACHED MODE
git add .
git commit -m '3rd commit for a file created in detached state'
git log --oneline(check the log list and commit the recent hash commit)

OUTPUT:(git log --oneline)

df0ad2b (HEAD) 3rd commit for a file created in detached state
6caa6f3 first commit

NOTE: Copy the df0ad2b hash commit

-----------------------------------------

git checkout main(return to the branch you want to add the new hash commit)
git cherry-pick df0ad2b

OUTPUT:

[main e19c75f] 3rd commit for a file created in detached state
 Date: Fri Feb 14 04:36:41 2025 +0500
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 detached.py

----------------------------------------------

git log --oneline(check the updated log list)

OUTPUT:
e19c75f (HEAD -> main) 3rd commit for a file created in detached state
4cf3817 fourth
6caa6f3 first commit

NOTE: df0ad2b hash commit has been assigned a NEW HASH for the UPDATED/CHERRY PICKED COMMIT, and now the NEW HASH is e19c75f

```
## 3.7 Key Differences Between `git diff` and `git checkout` (git answer)

| Feature         | git diff                               | git checkout                                  |
| --------------- | -------------------------------------- | --------------------------------------------- |
| Purpose         | Compares changes                       | Switches commits, branches, or restores files |
| Moves HEAD?     | NO                                     | YES                                           |
| Used for?       | Checking differences before committing | Moving between commits or branches            |
| Modifies files? | NO                                     | YES (restores or switches them)               |
| Example Command | git diff HEAD~1 HEAD                   | git checkout HEAD~2                           |
1. **Git checkout:** The `git checkout` command is used for **navigating commits or branches** and **restoring files**. Unlike `git diff`, it **does not move HEAD** to a different commit or branch.
2. **Git diff:** 
	a. Shows the difference between the working directory and the staging area.
	b. Compares changes between commits.
	c. Helps to inspect what has changed before committing.
### 3.8 Additional notes(gpt answer)

1. You can Detach the HEAD from any level using `git checkout hashcode` and then use the `git cherry-pick hashOflastCommit` to merge the changes made in DETACHED MODE into the current branch, or you can simply use the `git merge hashOfLastCommit` , *this hash commit refers to the commit made in DETACHED MODE.*
2. **git cherry-pick**: This command is used after you have **modified** the changes on **detached mode.** Then use `git checkout main(branchname)` to switch or point the HEAD to a particular branch. But before you do that you must also ensure to retrieve the HASH of the commit through `git log --online` command when you are on **detached mode.** Then from the current branch, use `git cherry-pick lastCommitHashFromDetachedMode.`
3. **git merge:** This command allows you to merge the last hash commit of the modified file from **detached mode** to be merged after you have pointed the HEAD to a particular branch of your choice.

### 3.9 Difference between Git Merge and Git Cherry-Pick commands?


#### Git Merge

1. This is used when you want to merge the history of commits of another branch to the current branch.
2. - - Creates a **merge commit** that ties together the histories of both branches.
3. It will make a new hash for merge commit, if there are **new changes** or **conflicts.**

#### Git Cherry-Pick

1. This is used when you want to select a **specific** hash commit of another branch or *from a change you made on DETACHED mode.*
2. **Git cherry-pick:** only works when there are changes or new commits, if the cherry-picks hash commit already exists, git will always return **working tree is clean, unless there is a change made or a new file created.**
3. Picks a specific commit (or series of commits) and **reapplies** them as a new commit in the current branch. `git cherry-pick 3423423 23423543 6556456`

**KEY DIFFERENCES**

| Aspect         | git merge                                                | git cherry-pick                            |
| -------------- | -------------------------------------------------------- | ------------------------------------------ |
| Scope          | Combines **all changes** from the source branch          | Selectively **copies specific commits**    |
| History Impact | Branch histories are merged, creating a **merge commit** | Histories remain **separate**              |
| Use Case       | When you want to **combine branches** entirely           | When you want to **copy specific changes** |
| Commit Hashes  | Original commit hashes are preserved                     | **New commit hashes** are created          |
| Example        | Merging a feature branch into main                       | Applying a bug fix to multiple branches    |

# 4.0 Topic: Deleting files and reverting to deleted files(sl)

1. **git rm filename** : Will delete a file from the **staging area** and the **working directory.**
2. **git rm --cached filename**: This will delete the file ONLY from the ***STAGING AREA.*** *This file will be **untracked** from the staging area.*
3. **Difference between rm, git rm and git rm --cached:**

	a. **rm:** Removes the files from the **working directory**(local system). *It doesn't tell git about the deletion.*
	b. **git rm:** Removes the files from the **working directory** and **staging area**, *it tells git about the deletion, but its removed in the next commit.*
	c. **git rm --cached:** Removes the files from the **staging area**, but keeps it inside the **working directory.**
	
4. Even after deleting the files, they still exist in the repository history. You can restore the deleted file from the repository history using the `git checkout versionHash filename`
5. After *deleting files,* you must ***add and commit the changes***, in order to record it in the ***commit history,*** so that later you can use the *commit history to restore the deleted files.*
**STEPS:**
1. Check how many files are **staged:** `git ls-files --stage`

```
git ls-files --stage

OUTPUT:

100644 e69de29bb2d1d6434b8b29ae775ad8c2e48c5391 0       a.txt
100644 e69de29bb2d1d6434b8b29ae775ad8c2e48c5391 0       b.txt
```
2. Delete files: `git rm a.txt` : *This deletes files from the **Working Directory** and **Staging Area***
3. Check again: `git ls-files --staged`

```
git ls-files --staged

OUTPUT:

100644 e69de29bb2d1d6434b8b29ae775ad8c2e48c5391 0       b.txt
```

4. Check how many files are in the **Working Directory:**

```
ls -lrt

OUTPUT:

total 0
-rw-r--r-- 1 USER 197121 0 Feb  8 05:18 b.txt
```

5. To delete the file ONLY from the STAGING AREA, use `git rm --cached b.txt`
6. Check the **Staging Area:** `git ls-files --stage`, IT will be empty in this particular example *because both files a.txt and b.txt are deleted.*
7. Check the **Working Directory Area:** `ls -lrt`

```
ls -lrt

OUTPUT:

-rw-r--r-- 1 USER 197121 0 Feb  8 05:18 b.txt

NOTE: This indicates that the file b.txt that was deleted from the STAGING AREA only, is still available in the WORKING DIRECTORY.
```

8. Check the **git status:**

```
git status:

OUTPUT:

HEAD detached at 8df95a3
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    a.txt
        deleted:    b.txt
        deleted:    c.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        b.txt

INTERPRETATION:

157. files a, b and c were all Deleted.
158. file b is the only file that was deleted from the STAGING AREA. Whereas, a and c files were deleted from both the STAGING AREA + WORKING DIRECTORY.
159. b.txt is the ONLY file that is indicating that is UNTRACKED, *because all other files don't exist in the working directory. Only the files in the WD are TRACKED or UNTRACKED.*

```

### 4.1 How to restore Deleted Files?

1. Check **git log --oneline** status

```
git log --oneline

OUTPUT:

c9f2530 (HEAD -> master) third commit
59d79a3 2nd commit
8df95a3 first commit
```

2. Even if a file is deleted, its **commit history** is still there and stored in the repository.
3. A user needs to **identify** to the **commit version**, in order to revert ***deletion.***
4. Delete the b.txt file that was previously deleted ONLY from the STAGING AREA.
5. Check `git log --oneline`

```
git log --oneline

OUTPUT:

ea487fb (HEAD -> master) Deleted files
c9f2530 third commit
59d79a3 2nd commit
8df95a3 first commit

```

6. **Restoring Files**
	a. `git checkout HEAD~1 a.txt`: This allows you to restore the a.txt file, *if the file was available on HEAD~1 level.*
	b. `git checkout HEAD~2 b.txt:` This allows you to restore the b.txt file from the commit history.
	c. When you use ***git checkout command with hashOfCommit of HEAD~1*** level, it restores files from history based on the commit level of the specified Hash/HEAD level.
	d. The file is restored from the ***Local Repository***, and moved to the **Staging Area.**
	e. You then need to use the ***Merge*** or ***Cherry pick***  method to restore the files or last changes.
	f. Another option is to use `git checkout HEAD~1 a.txt` and subsequently the same command for b.txt.
	e. `git checkout HEAD~1 A.TXT` allows you to restore the file WITHOUT ***deatching the head*** from the last commit.
	g. The command in e, will move the files from the ***local repository*** to the ***staging area*** and then you need to `git commit -m 'your message'` to restore the files as a ***new commit level.***

### 4.2 Deleting a specific commit while keeping all other recent and earlier commits in history(GPT Answer)


# 5.0 Topic: Git Ignore (simpli learn)

Sometimes its important to ignore files while creating a version of your project, these could be packages and other irrelevant files that are not needed for production, and can be installed by other users on their local systems later. One other reason could be to avoid heavy files from being transfered.
1. Files are stored inside a file called ***.gitignore***
2. This would avoid *tracking* any files or folders.
3. You can mention the ***File name + File pattern*** in the gitignore file.
4. You can also ***override*** the *filename + file pattern* using the **-f flag**.

```
1. Add the .gitignore file using vi command or touch command, and add *.txt line inside the .gitignore file, this prevents files from being tracked.
2. The .gitignore file will be untracked.
3. Create another file.
4. Add it to the staging Area then commit it.
5. Check if the commit works.

vi .gitignore

OUTPUT:

Press i for edit. Then add the following text: *.txt, this will help ignore all files ending with the .txt characters.

---------------------------------------------

touch d.txt or e.txt

OUTPUT: This will create these 2 files.

------------------------------

git status

OUTPUT:

The output will give status of new files ready to be ADDED to the STAGING AREA then commit them.

-------------------------------------

git add .
git status

OUTPUT:
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore
        

git commit -m 'added .gitignore and a file'

---------------------------------------

touch e.txt
git add .

NOTE: This will create the file, but it will be highlighted as ignored, and will not allow the file to be added.

---------------------------

git add -f e.txt

OUTPUT:

This will allow you to add the ignored file, and commit it.

$ git commit -m 'add e.txt with -f flag'
[master a99cb22] add e.txt with -f flag
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 e.txt
```

### 5.1 Git ignore file types

Sometimes there are folders or modules that you don't want to push or add to your repository, therefore the best way to do that is to keep them in a file called .**gitignore**. All you need to do is make a list of all the names of files, folders or extensions, each in a new line.

1. To ignore all files in the entire repository, of a certain extension type:  `*.extension`
2. To ignore all files with the same or specific name found anywhere in the project, just type the filename without giving the path: `filename.txt`
3. To ignore a specific file in a specific location, use the full path seen from the *root* of your project folder. Example `/path/new.txt`
4. To ignore all files in a certain folder: `/path/to/*`
5. To ignore a particular folder entirely along with subdirectories: `foldername/`
6. To ignore all Files + Folders, simply use an *asterisk*
7. Run `git status --ignored` command to check if git is tracking any unwanted files.
8. If git is tracking ***unwanted files/folders,*** then use the following command: `git rm -r --cached Data_cleaning_and_visualization/share/`
# 6.0 Topic: Renaming Files

1. `git mv <filename> <newFileName>`
2. `git add .`
3. `git commit -m 'your message'`

The above commands allow you to rename the file name, add them to the **staging area** and then **commit** them.

```
git mv e.txt f.txt

git status

OUTPUT:
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    e.txt -> f.txt

NEXT STEPS:
1. Add the changes to the Staging Area
2. Commit your changes.

```
 
### 6.1 How to un stage a file?

Sometimes you want to **unstage files**, you can use the `git restore --staged file.txt` or `git reset HEAD file.txt`

#### Unstage specific files(gpt answer)

```
git restore --staged file.txt

OR 

git reset HEAD file.txt

OUTPUT
This allows you to restore files, leaving the changes intact, without deleting or discarding the changes.
```

#### Unstage all the files(gpt answer)

```
git restore --staged .

OR

git reset HEAD .

NOTE: This removes all the files from the Staging Area, but PRESERVES the changes.
```

#### Unstage and discard changes(gpt answer)

```
git checkout -- file.txt

OR 

git restore file.txt

NOTE: This will restore a file while discarding the last committed changes.
```

#### 6.2 Why doe we use -- double dash after checkout option?(gpt answer)

1. Git may assume or mistake the file name file.txt as the name of the BRANCH.
2. You may have a branch name called file.txt, therefore it is important to use a double dash -- before the name of the file.
3. Double dash -- is used in git to explicitly separate options from *file names.*
# 7.0 Topic: GitHub and Remotes(simpli learn)

Outline
1. Introduction to github
2. Creating a repository on github
3. Pulling commits from github
4. Collaborating between **Local** and **remote** repositories
5. Managing multiple commits in github.
6. **Merging** file changes in git.
7. **Issue tracking** in git.

### 7.1 Introduction to github

1. Difference between ***master*** and ***origin***?
	a. **Origin**: These include all the commits made in the *github repository*.
	b. **Master:** These include all the commits made in the *local repository.*

2. Github has various subsections:
	a. Personal: *This entails your personal projects that are available from beginner to expert level.*
	b. Open Source Projects: *You can find many opensource projects that are publically available on github.*
	c. Business: You can either choose to use github servers as ***Public cloud repositories*** to manage your business repos, or you can install github locally on your local or private servers as ***Private Cloud Repositories***
	c. Explore: Many projects that are ***hosted on github.***

3. Inside **Explore:** *You can click on various categories to get projects that are relevant to you. Example, you can click on **Text editors**, and you will find all the text editors, click on anyone, and then click on **fork**, if you wish to continue working on or making edits on the most recently pushed or committed project files*

### 7.2 Steps to creating a new Repository using HTTPS and SSH:

1. Login using your credentials
2. Create a new repository
3. Follow **github** instructions: *Create a symbolic link or push from your local repository.*
### 7.3 Creating a repository using HTTPS

1. Move to the repository on your local system that you want to push.
2. Check **git status** to ensure nothing is required to commit or add to the staging area.
3. You can also use the **ls -lrt** command to list down the files you want to push and get a snapshot of what you have in your local repository.
4. **New repository:** Create a new repository on your github account. It will ask you to *name* your repository and also select whether you want to ***initialize*** the repository on github, or you can also choose to leave it.
5. For now, create a repo ***without*** initializing it.
6. Once you have created, it will take you to a page of ***instructions.***
7. It will give you the following details:

### 7.4 HTTPS METHOD

```
### **Quick setup** — if you’ve done this kind of thing before
This will give you an option to use HTTPS or SSH to push, pull or fetch. We will use the HTTPS method.

### …or create a new repository on the command line

echo "# two" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/sohaib-sharih/two.git
git push -u origin main

### …or push an existing repository from the command line

git remote add origin https://github.com/sohaib-sharih/two.git
git branch -M main
git push -u origin main

```

1. **git push -u origin main**: What does `u` entail? *It allows you to instruct git that all your commits will be pushed **master** to **origin**.* You don't need to use the -u option for now.

```
git push origin master

OUTPUT:
If this is the first time you are running the push command, then it will prompt a user id and password, after entering the user id, it will prompt a popup asking for credentials. Then git will compress your LOCAL COMMITS and push them to the github repository.

209. Refresh your github repo page.
210. Your code will be pushed
211. On your vscode CLI, check the Hash of commit by git log --oneline and compare them with the commits on the github repository, they'll be the SAME. To do this, you can click on CODE -> COMMITS tab on top panel.
```

This is the ***END*** of a procedure of pushing your Local Repository using the **HTTPS protocol.**

## 7.5 Using the SSH Key

1. Ensure that the LOCAL repository is ready.
2. Create an **SSH KEY** or **SSH KEYGEN**
3. Configure github with **SSH Public key**

```
ssh-keygen OR ssh-keygen -t rsa -b 4096 -C <your repo user email id>

OUTPUT:

This command Generates 2 KEYS (2 Files)

Example: newTwo (PRIVATE KEY)

-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAACFwAAAAdzc2gtcn
NhAAAAAwEAAQAAAgEAsbZaTPcn/G87yhLZSyu9wTxDPnPsW2pdqtpg6jtdccEZpF3+tdmw
roWW+ZpbXyiDf1gAoUD5NhFDyGBJ5fgwVrfXrL/1aW97TmiQCqYH3r+EmWXSuzl+biDSE7
Q4MgMcQM63P0Pv0bMlpcJNDZsPSH/YGS0ZkDloj8pz6/ubH/bFKY2egFAhHWy6je1TsOCN
gl0S7a688SC2z9GY2/8zZdVJSkXeaPmbdaXtQLMA7pWAk7NurV8s9KLJWraYXSC7CrCrkj
Fw3cr/LSJXoGsAAAEBAMmYwsaJTNF4K/LMtKSZ7zvKw1sg+xC16hnqisoassgX6NCFDzJB
XppGRnfMPNnRld9NOvMt3fANRejKytlmugRTj/fQ6umCtzhyp494nqxiGxFslq2cOWXXev
rX+0YbEiOrTWgnlGqVBAVseik9j25E/VFz6Krran3t7Rhs0NbbFCkDAh1+yDmICSUOtBpm
r3VKQzEjnfipm71TxA2rx+jK0zT7KjjJmPEa5sOoYDUKuGMwQc3hXvJchZ3OB9Q/6j80ZR
0+aSyOQptWrrqIdLoANeDgP3JcTvjZRjxFamAXAx4/MObCUs2BIOoJo0veWviq3Md0TkoT
58fOJlXbqZsAAAAXc29oYWliLnNoYXJpaEBnbWFpbC5jb20BAgME
-----END OPENSSH PRIVATE KEY----

Example: newTwo.pub (PUBLIC KEY)

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCxtlpM9yf8bzvKEtlLK73BPEM+c+xbal2q2mDqO11xwRmkXf612bCuhZb5mltfKIN/WAChQPk2EUPIYEnl+DBWt9esv/Vpb3tOaJAKpgfev4SZZdK7OX5uINITtDgyAxxAzrc/Q+/RsyWlwk0Nmw9If9gZLRmQOWiPynPr+5sf9sUpjZ6AUCEdbLqN7VOw4I2lKBQxzmRAS1fCOsQrWKi38cX4mkqSoOAwkDhEGy2LII/VfuBsGzuEnVzH1yG0/vWiiX+34jKG5RHFR83Tu/ZdeBB51CbCXVE5/aeHr8ZnaCZcAQjEnqEdIh5Czi2GtF5BY9xYtEdP8iUcBrI1eZ1cixLo/r+aNz1IJMSt75D4sQB27Csr40iUQGuu7KaCT3vwe3Pp60iBIKf7qsRPckVqVkqrTK1qifwK9t3A8stJ9UuQd/aXvm9Ts/px8S1qGf0dR6EA284Wm4AEaTqICBjvp9VP4ru8ptqigdM4Kqfj2m8B8J9/BDEZ8ACzjsO64NSfVq2ZN6qZepoYjqGuw4Uw1LCLBzwenamqMmlXST3n30SmRBNvitnlnpl/R0Fh/qAnsmKUgR/0JsyiYu3uaKwyOpEzCGtuCJgZvGThkcbJhurynfPLs3lKW99XuUUCY0fn8OACpe6AUHboYwQ/0cDeAe731cJeYUhwpa8bZn3DyQ== sohaib.sharih@gmail.com


```

1. Create a **github repository**
2. Push from the Local repository to the Github Repository.
3. **NOTE:** The SSH Key allows you to create a repository without using a ***user name or password.***

**Steps to enable and use SSH Key**

1. **git status:** To check and ensure that your ***working tree is clean.***
2. **ls -lrt:** To check the contents of your ***local repository.***
3. **ssh-keygen**: This command on the CLI will allow you to create a SSH key, it will prompt for the **location**, keep the default location, and since there is no ***pass phrase***, hit enter and continue.

## 7.6 SSH METHOD (using Default Location)

```
ssh-keygen

OUTPUT:

Generating public/private ed25519 key pair.
Enter file in which to save the key (/c/Users/USER/.ssh/id_ed25519):

221. This will ask you to enter the path to save the hash key.
222. Press enter to keep the DEFAULT Location.
223. Use the **cat command** followed by the location of the path of the hashkey, to read the Hash value, copy the hash value and Create a hash key on github settings, under SSH and GPG settings.
--------------------

cat key.pub (PUBLIC KEY)

OUTPUT:

SHA256:KsIBcDzjCCr9knKbjFPrJ4wBaU2w5rl404E2WIa170Q USER@DESKTOP-Q92VRIR

-----------------------

1. **Login to github:** Enter your credentials and login, then go to ***settings***
2. **PUBLIC KEY** --> Go to **SSH and GPG keys** and enter the key from the ***key.pub*** file.
3. Once you have setup the HAsh key on github, create a new repository, then select the SSH option.
4. Instructions will appear to push existing local repository files to the github repo.

Example instructions:

... create a new reposirty on the command line:

echo "# three" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:sohaib-sharih/three.git
git push -u origin main

... Push an existing Local repository:

git remote add origin git@github.com:sohaib-sharih/three.git
git branch -M main
git push -u origin main

NOTE: use git push origin master(or main if that is your current branch, you can push code from any branch since you haven't used -u flag.)
```

## 7.7 How to save SSH key in a Custom location?(GPT Answer)

1. Create an SSH key using the **ssh-keygen** command on the CLI, and you will also need to use additional options to create a strong and secure hash as shown below:

```
ssh-keygen -t ed25519 -C 'sohaib.sharih@gmail.com'

OUTPUT:

$ ssh-keygen -t ed25519 -C 'sohaib.sharih@gmail.com'
Generating public/private ed25519 key pair.
Enter file in which to save the key (/c/Users/USER/.ssh/id_ed25519): E:\MISCELLENEOUS\MY PROJECT\LEarning\Blockchain\Node js\My Assignments\Practice\Git\test\threeKey\threeKey
Enter passphrase for "E:\MISCELLENEOUS\MY PROJECT\LEarning\Blockchain\Node js\My Assignments\Practice\Git\test\threeKey\threeKey" (empty for no passphrase):
Enter same passphrase again: 
Your identification has been saved in E:\MISCELLENEOUS\MY PROJECT\LEarning\Blockchain\Node js\My Assignments\Practice\Git\test\threeKey\threeKey
Your public key has been saved in E:\MISCELLENEOUS\MY PROJECT\LEarning\Blockchain\Node js\My Assignments\Practice\Git\test\threeKey\threeKey.pub
The key fingerprint is:
SHA256:U7agW1ZNLxdXsWjxoeEy3aPRHjH9zQq5FwLOQV5JWNs sohaib.sharih@gmail.com
The key's randomart image is:
+--[ED25519 256]--+
|         ..+=+.=*|
|         .++++Oo*|
|        .o==+OEOo|
|       . =o.Bo= *|
|      . S .  = + |
|       + .  . o  |
|      .      .   |
|                 |
|                 |
+----[SHA256]-----+

INTERPRETATION:

229. Run the command.
230. It will prompt you to save it to a location or skip to save it in the DEFAULT location.
231. Copy the path of the folder you want to save it in.
232. Add the name of the file you want it to generate the keys for.
233. Ensure that the file name is NOT created manually.
Example path location: E:\MISCELLENEOUS\MY PROJECT\LEarning\Blockchain\Node js\My Assignments\Practice\Git\test\threeKey\threeKey
234. It will prompt you to keep the DEFAULT Location or to enter a new path location.
235. Select your path, then enter a name for the ssh-keygen to create 2 files automatically, one for the public key and the other for the private key.
236. EXAMPLE: your path is-> E:\Git\test\remote\my_ssh_key will generate 2 files
a) E:\Git\test\remote\my_ssh_key
b) E:\Git\test\remote\my_ssh_key.pub

NOTE:
SSH-KEygEN creates 2 keys
237) PRIVATE KEY
238) PUBLIC KEY, whose file ends with a .pub extension.

```

2. After using the ssh-keygen command, it will create 2 Keys as follows:

	a. PRIVATE KEY (without an extension)
	b. PUBLIC KEY (with .pub extension)


```
cat ../threeKey/threeKey.pub

OUTPUT:
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5sdfsdgdffg46/7hKIxNbQIfQNbRkFsi73x99QehGqnA0n45W1+ sohib.srih@gmail.com

```

3. You need to copy the .pub key and paste it in the GitHub SSH Settings area.
4. Ensure to keep the ***Authentication Key*** option for ***key type*** on github.
5. **SSH Agent**:
	a. It is a background program that stores your ***private key*** securely.
	b. Without it, you will have to enter your ***passphrase*** each time you ***push*** your code.

6. **Command Used to Start SSH-Agent and ADDING the Private Key**

```
eval "$(ssh-agent -s)"
OR
ssh-agent bash

OUTPUT:

1. Either of the commands can be used to START the SSH-Agent program.

Followed by

ssh-add ../threeKey/threeKey (double dot becuase the keys are outside the project folder)

OUTPUT:

./threeKey/threeKey: No such file or directory

1. ssh-add allows you to add the PRIVATE KEY.
2. You need to give the RELATIVE PATH, along with the name of the Private key file.
3. NOTE: The name of the private key file does not end with an extention such as .pub, .pub is for a public key.
```

## 7.8 Difference between *eval "(ssh-agent -s)"* and *ssh-agent bash*(gpt answer)

***eval "(ssh-agent -s)"***

1. This keeps the agent active in the **current shell.**
2. This is a recommended approach.
3. The key is stored temporarily, as long as you don't restart your terminal or computer, otherwise you will have to restart the ssh agent, using this command followed by `ssh-add <path to your private key>`

***ssh-agent bash***

1. This method is also ok, but once you exit it, it will forget the ***private key*** you added, therefore you will have to add the private key again using the `ssh-add <Relative path to private key>`
2. This command starts a new bash shell by loading the *environment variables* needed to run the **ssh-agent**.
3. If you exit the shell, it kills the ***ssh agent***, you will have to run the ssh-agent again then add them again. *You can also check by `ssh-add -l` command.*
4. Restarting or exiting the terminal may still allow github to authenticate without the private key in the ssh-agent because github has saved its memory of temporary authentication tokens generated for a couple of hours.

### Conclusion (difference between eval and ssh-agent bash)

Both methods in principle are the same. They hold the private keys temporarily. However

## 7.9 Update Your Git Remote to Use SSH

1. **git remote set-url origin git@github.com:your-username/your-repository.git**
2. **git remote -v**: Check the new remote connection.
## 7.10 Different types of Cryptographic Methods to generate SSH Key

1. ed25519

	a. More secure with **shorter key lengths** compared to RSA.
	b. Faster **generation** and **signing** speeds.
	c. **Security Level:** **High** (suitable for modern security standards).
	d. **Key Length:** Fixed at **256 bits** (equivalent to ~3000-bit RSA).
	e. **Performance:** **Faster** than RSA in signing and verifying.
	f. **Use Case:** **Recommended for most users** due to its security and performance.
	g. **Command Example:** `ssh-keygen -t ed25519 -C "your_email@example.com"`
2. RSA
	a. Slower than ed25519 in signing and verifying operations.
	b. Requires **longer key lengths** for the same security level as ed25519
	c. **Key Lengths:** Typically **2048** or **4096 bits**
	d. **Security Level:** **Medium to High**, depending on key length.
	e. **Use Case:** Use only if you need compatibility with **legacy systems**.

3. XMSS (eXtended Merkle Signature Scheme)

	a. Designed to be **quantum-resistant** (safe against quantum computing attacks).
	b. **Key Length:** **Variable**, but generally much larger than ed25519 or RSA.
	c. **Slower** than both ed25519 and RSA.
	d. **Use Case:** Ideal for **long-term security** and **post-quantum cryptography** requirements.

#### Recommendation for GitHub:

1. **Use ed25519** unless you have a specific reason to use RSA (e.g., compatibility).
2. Only consider XMSS if you have long-term security concerns and can handle larger key sizes.

## 7.11 Summary of Commands using SSH Method

1. **ssh -T git@github.com**: This is used to check if git is using the correct Hashkey.

```
ssh -T git@github.com

OUTPUT:

Hi sohaib-sharih! You've successfully authenticated, but GitHub does not provide shell access.
```

2. **ssh-agent bash OR eval("ssh-agent -s")**: *This starts the ssh agent program*
3. **ssh-add < relative path to private key >**: *This adds your private key in memory of ssh-agent.*
4. **ssh-add -l**: *This checks if the private key is added*
5. **ssh-keygen:** *Allows you to generate private + public keys in default location*
6. **ssh-keygen -t ed25519 -C 'sohaib.sharih@gmail.com'**: *Allows you to create an ssh-key for custom location. Best practice is to use*
7. **`cat ~/.ssh/*`**:  *This allows you to check all keys present in your system.*
8. `ls ~/.ssh/`: *To check the files created using the ssh-keygen command in your home/default location.*
9. ***Double dash --***: We use double dash to explicitly separate options from file names and branch names, in order to avoid git from misinterpreting the file name as the name of a ***branch name.***
10. **Authentication Key** → Used for pushing, pulling, and accessing repositories via SSH (**✅ Correct choice**).
11. **Signing Key** → Used for **signing commits**, not for authentication.


## 7.12 How to check which SSH Key is being used by local repository?(gpt answer)

There are various methods to find out which SSH Keys are being used for your local repository to authenticate by the Github repository.

1. **Method 1:** This is used to locate ALL SSH Keys in use.
2. **Method 2:** This will list ALL the SSH KEYS on your system.
3. **Method 3:** If you have set up a **specific ssh key** for your repository, this will give you the list of ssh keys, however, if the output is ***empty***, then that means it is using your SSH keys set in the ***default location.***
4. **Method 4:** If you're using `ssh-agent` to manage keys, you can see which keys are currently loaded. `ssh-add -l`
5. **Method 5:** To check which SSH Key is ***actively*** being used by github.


```
Method 1

ssh -vT git@github.com

Interpretation: This will locate all the SSH keys used in use.

1. **`-vT`:** Verbose and Test connection without executing commands.
2. The output will show the **identity file** (the SSH key) that is being used to connect.
3. Look for a line like this --> debug1: Offering public key: /c/Users/USER/.ssh/id_ed25519 ED25519 

OUTPUT:

OpenSSH_9.9p1, OpenSSL 3.2.3 3 Sep 2024
debug1: Reading configuration data /etc/ssh/ssh_config
debug1: Connecting to github.com [20.207.73.82] port 22.
debug1: Connection established.
debug1: identity file /c/Users/USER/.ssh/id_rsa type -1 ---> Cryptography method
debug1: identity file /c/Users/USER/.ssh/id_rsa-cert type -1
debug1: identity file /c/Users/USER/.ssh/id_ecdsa type -1 ---> Cryptography method
debug1: identity file /c/Users/USER/.ssh/id_ecdsa-cert type -1
debug1: identity file /c/Users/USER/.ssh/id_ecdsa_sk type -1
debug1: identity file /c/Users/USER/.ssh/id_ecdsa_sk-cert type -1
debug1: identity file /c/Users/USER/.ssh/id_ed25519 type 3 ---> Cryptography method
debug1: identity file /c/Users/USER/.ssh/id_ed25519-cert type -1
debug1: identity file /c/Users/USER/.ssh/id_ed25519_sk type -1
debug1: identity file /c/Users/USER/.ssh/id_ed25519_sk-cert type -1
debug1: identity file /c/Users/USER/.ssh/id_xmss type -1 ---> Cryptography method
debug1: identity file /c/Users/USER/.ssh/id_xmss-cert type -1
debug1: Local version string SSH-2.0-OpenSSH_9.9
debug1: Remote protocol version 2.0, remote software version b09b5852c
debug1: compat_banner: no match: b09b5852c
debug1: Authenticating to github.com:22 as 'git'
debug1: load_hostkeys: fopen /c/Users/USER/.ssh/known_hosts2: No such file or directory
debug1: load_hostkeys: fopen /etc/ssh/ssh_known_hosts: No such file or directory
debug1: load_hostkeys: fopen /etc/ssh/ssh_known_hosts2: No such file or directory
debug1: SSH2_MSG_KEXINIT sent
debug1: SSH2_MSG_KEXINIT received
debug1: kex: algorithm: curve25519-sha256
debug1: kex: host key algorithm: ssh-ed25519
debug1: kex: server->client cipher: chacha20-poly1305@openssh.com MAC: <implicit> compression: none
debug1: kex: client->server cipher: chacha20-poly1305@openssh.com MAC: <implicit> compression: none
debug1: expecting SSH2_MSG_KEX_ECDH_REPLY
debug1: SSH2_MSG_KEX_ECDH_REPLY received
debug1: Server host key: ssh-ed25519 SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU
debug1: load_hostkeys: fopen /c/Users/USER/.ssh/known_hosts2: No such file or directory
debug1: load_hostkeys: fopen /etc/ssh/ssh_known_hosts: No such file or directory
debug1: load_hostkeys: fopen /etc/ssh/ssh_known_hosts2: No such file or directory
debug1: Host 'github.com' is known and matches the ED25519 host key.
debug1: Found key in /c/Users/USER/.ssh/known_hosts:1
debug1: ssh_packet_send2_wrapped: resetting send seqnr 3
debug1: rekey out after 134217728 blocks
debug1: SSH2_MSG_NEWKEYS sent
debug1: expecting SSH2_MSG_NEWKEYS
debug1: ssh_packet_read_poll2: resetting read seqnr 3
debug1: SSH2_MSG_NEWKEYS received
debug1: rekey in after 134217728 blocks
debug1: SSH2_MSG_EXT_INFO received
debug1: kex_ext_info_client_parse: server-sig-algs=<ssh-ed25519-cert-v01@openssh.com,ecdsa-sha2-nistp521-cert-v01@openssh.com,ecdsa-sha2-nistp384-cert-v01@openssh.com,ecdsa-sha2-nistp256-cert-v01@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256-cert-v01@openssh.com,rsa-sha2-512-cert-v01@openssh.com,rsa-sha2-256-cert-v01@openssh.com,ssh-rsa-cert-v01@openssh.com,sk-ssh-ed25519@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,ssh-ed25519,ecdsa-sha2-nistp521,ecdsa-sha2-nistp384,ecdsa-sha2-nistp256,rsa-sha2-512,rsa-sha2-256,ssh-rsa>
debug1: SSH2_MSG_SERVICE_ACCEPT received
debug1: Authentications that can continue: publickey
debug1: Next authentication method: publickey
debug1: Will attempt key: /c/Users/USER/.ssh/id_rsa
debug1: Will attempt key: /c/Users/USER/.ssh/id_ecdsa
debug1: Will attempt key: /c/Users/USER/.ssh/id_ecdsa_sk
debug1: Will attempt key: /c/Users/USER/.ssh/id_ed25519 ED25519 SHA256:RkZdr9O9nz37pxiFZiZ3rxOoqf6Jtwtt6zDl5BMSa88 -----> (Match the Key on Github)
debug1: Will attempt key: /c/Users/USER/.ssh/id_ed25519_sk
debug1: Will attempt key: /c/Users/USER/.ssh/id_xmss
debug1: Trying private key: /c/Users/USER/.ssh/id_rsa
debug1: Trying private key: /c/Users/USER/.ssh/id_ecdsa
debug1: Trying private key: /c/Users/USER/.ssh/id_ecdsa_sk

->debug1: Offering public key: /c/Users/USER/.ssh/id_ed25519 ED25519 SHA256:RkZdr9O9nz37pxiFZiZ3rxOoqf6Jtwtt6zDl5BMSa88<- --> Path of the SSH Key

debug1: Server accepts key: /c/Users/USER/.ssh/id_ed25519 ED25519 SHA256:RkZdr9O9nz37pxiFZiZ3rxOoqf6Jtwtt6zDl5BMSa88 ----> (Match key on Github)
Authenticated to github.com ([20.207.73.82]:22) using "publickey".
debug1: channel 0: new session [client-session] (inactive timeout: 0)
debug1: Entering interactive session.
debug1: pledge: filesystem
debug1: client_input_global_request: rtype hostkeys-00@openssh.com want_reply 0
debug1: client_input_hostkeys: searching /c/Users/USER/.ssh/known_hosts for github.com / (none)
debug1: client_input_hostkeys: searching /c/Users/USER/.ssh/known_hosts2 for github.com / (none)
debug1: client_input_hostkeys: hostkeys file /c/Users/USER/.ssh/known_hosts2 does not exist
debug1: client_input_hostkeys: no new or deprecated keys from server
debug1: pledge: fork
debug1: client_input_channel_req: channel 0 rtype exit-status reply 0
Hi sohaib-sharih! You've successfully authenticated, but GitHub does not provide shell access.
debug1: channel 0: free: client-session, nchannels 1
Transferred: sent 2168, received 2600 bytes, in 3.2 seconds
Bytes per second: sent 681.5, received 817.3
debug1: Exit status 1

NOTE: There are different types of Cryptography methods:

1. RSA
2. ed25519
3. XMSS

You can select any method, however the fastest and most recure is ed25519 cryptography method.
1. ed25519: It is also recommended to use ed25519 method.
2. RSA: RSA is slower, and may generate longer hash codes. Less secure as compared to ed25519.
3. XMSS: XMSS is the strongest and most secure, and is generally used to protect from attacks from Quantam Computers.

---------------------------------------------------------------------------
Method 2

ls -al ~/.ssh (if your ssh files are located in the DEFAULT Location)
ls -al ./two_key (if your SSH files are located at the CUSTOM location)

Interpretation:

1. To see all the SSH keys you have on your system, use:
2. .pub These are your **public keys**.
3. The corresponding **private keys** are the same names **without `.pub`**.

OUTPUT:

total 27
drwxr-xr-x 1 USER 197121    0 Feb  9 02:23 ./
drwxr-xr-x 1 USER 197121    0 Feb 12 19:25 ../
-rw-r--r-- 1 USER 197121  411 Feb  9 02:22 id_ed25519
-rw-r--r-- 1 USER 197121  102 Feb  9 02:22 id_ed25519.pub
-rw-r--r-- 1 USER 197121 1010 Feb  9 02:23 known_hosts
-rw-r--r-- 1 USER 197121  275 Sep  6 04:49 known_hosts.old
-------------------------------------------------------------------------------
Method 3:

git config --get core.sshCommand

Interpretation:

1. If you have set a **specific SSH key** for the repository, you can find it in the Git config:
2. Then Git is using that **specific key** for this repository. It will return 'ssh -i ./newTwo -o IdentitiesOnly=yes'
3. If it's **empty**, then Git is using the **default SSH key** (usually located in `~/.ssh/id_rsa` or `~/.ssh/id_ed25519`).

OUTPUT:

ssh -i ./newTwo -o IdentitiesOnly=yes

-----------------------------------------------

Method 4:

ssh-add -l

Interpretation: 

1. To check ACTIVE SSH keys made through the SSH Agent.
2. If no keys are listed, you can add them manually: ssh-add /path/to/private_key

OUTPUT:

Add them here.

---------------------------------------------

Method 5:

ssh -T git@github.com

Interpretation: Verify with github

1. To verify which SSH key is **actively** being used with GitHub:
2. If it **fails**, then the key isn't recognized by GitHub.

OUTPUT:

Hi sohaib-sharih! You've successfully authenticated, but GitHub does not provide shell access.


```


### 7.13 How to update/change an SSH connection to your Remote connection?(GPT Answer)

```
git remote -v
git remote --set-url origin git@github.com:sohaib-sharih/newTwo.git

Then try again using
git push origin main/master

NOTE: You can push it once the SSH keys are set. In the previous sections, we learned various different methods of using the SSH Key gen command to generate and save SSH keys.
```

### 7.14 How to create a new Remote Connection/name?

1. git remote -v : provides the current remote connections to your **local directory.**
2. git remote add 'nameOfConnection' 'linkOfGitHubRepo': This will allow you to create a **new name of connection** and also the link is required to connect your **local directory/repo** with the **github repo.**
3. **origin** is a **default** connection name.
4. Note: You should call it MAIN, as its a name used most commonly. The first time you create a new name for connection, **automatically becomes** part of the **default connection name.**
## 8.0 Git Pull

1. Login to your github.
2. Switch to the repository that you want to pull your request from.
3. Add new commits in your remote repository by adding a readme file for example.
4. Add new commits in different branches.
5. Use the `git pull origin master` command to pull the remote repository commits and merge them with your ***local repository.***
6. If there are any changes, it will indicate in your terminal with a + sign.
7. It may also open an ***editor*** on your terminal to add a ***commit message*** for merging into your ***local repository.***

Example

```
BRANCH: mergeBranch
git pull origin mergeBranch

OUTPUT:

remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 961 bytes | 2.00 KiB/s, done.
From github.com:sohaib-sharih/threeKey
 * branch            mergeBranch -> FETCH_HEAD
   d714d6b..6446e3d  mergeBranch -> origin/mergeBranch
Updating d714d6b..6446e3d
Fast-forward
 README.md | 1 +  ---------> This indicates that 1 file with 1 change was made.
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

---------------------------------------------
BRANCH: mergeBranch
git log --oneline(for mergeBranch branch)

OUTPUT:

6446e3d (HEAD -> mergeBranch, origin/mergeBranch) Create README.md
d714d6b Merge commit '89f38b5' into mergeBranch
89f38b5 new Commit
59ad487 7th commit
0b57667 5th commit
79dfec5 (origin/master) fourth
e2de355 third
4d72b37 second commit
Merge branch 'master' of github.com:sohaib-sharih/threeKey
6caa6f3 first commit

-----------------------------------------------
BRANCH: master
git pull origin master

OUTPUT:

remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 989 bytes | 4.00 KiB/s, done.
From github.com:sohaib-sharih/threeKey
 * branch            master     -> FETCH_HEAD
   79dfec5..77e1c68  master     -> origin/master
Merge made by the 'ort' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+) ---> This indicates 1 file + 1 insertion was made.
 create mode 100644 README.md

--------------------------------------------------
BRANCH: master
git log --oneline (for master branch)

OUTPUT:

ce67423 (HEAD -> master) Merge branch 'master' of github.com:sohaib-sharih/threeKey
77e1c68 (origin/master) Create README.md in master branch
dd8bb55 Merge commit 'f21f532' Merge commit after f21f532 commit was made in detached mode
f21f532 detached 406e5c0, added mergeTwo.py file
f89f1fd Merge branch 'newBranch' Merging the newBranch with master
2bc1dfe (newBranch) new merge commit
7944c4f Merge commit '406e5c0'
406e5c0 creating a new file in detached mode, then merging
4cf3817 fourth
59ad487 7th commit
0b57667 5th commit
79dfec5 fourth
e2de355 third
4d72b37 second commit
6caa6f3 first commit


```

#### 8.1 What is the purpose of using GIT PULL and when to use it?

1. You should use git pull command when you want to sync your remote repo with your local repo.
2. Git pull command pulls the following from the remote repo:
	a. git ignore file (*if it was created when creating the remote repo.*)
	b. README.md file (*if it was created.*)
	c. First commit, which is made ONLY if you choose to ADD the README.md file.
3. If you have already created a Project Folder and files in your local directory, and also initialized it, then you don't need to create the README.md file to initialize it separately on the remote repository. *you should skip these options and create an empty repository.*
4. When you run the ***git pull command***, the first time, it creates a folder and copies all the remote repository contents inside that folder on your local directory.
5. If you have accidentally already initialized your remote repository + initialized your local repository separately, then you can run the following command to overwrite your remote repo with your local repo using the following command -> `git push origin main --force`
6. **Delete a branch on your remote repo**: `git push origin --delete new(name of branch on remote repo.)`
7. If ***git pull origin main*** command fails because you have initialized both local and remote repositories separately, accidentally, then it will give you an ERROR like the following:
```
From https://github.com/sohaib-sharih/Python-Memory * branch main -> FETCH_HEAD fatal: refusing to merge unrelated histories

TO RESOLVE THIS ERROR:

OPTION 1
git pull origin main --allow-unrelated-histories

OPTION 2
git push origin main --force
```
### 8.2 Interpretation of the git log --oneline (GPT answer)

The below interpretation is of the git log --oneline log of commits history made after pulling commits from the ***remote repository.***

#### Mergebranch

```
git log --oneline(mergeBranch)

OUTPUT:

6446e3d (HEAD -> mergeBranch, origin/mergeBranch) Create README.md
d714d6b Merge commit '89f38b5' into mergeBranch
89f38b5 new Commit
59ad487 7th commit
0b57667 5th commit
79dfec5 (origin/master) fourth
e2de355 third
4d72b37 second commit
Merge branch 'master' of github.com:sohaib-sharih/threeKey
6caa6f3 first commit
```

#### Interpretation

1. `6446e3d (HEAD -> mergeBranch, origin/mergeBranch) Create README.md`
	a. **6446e3d**: This is the unique hash identifier for this commit.
	b. **HEAD -> mergeBranch**: This shows that your local branch pointer (HEAD) is currently on the `mergeBranch`. You are actively working on this branch.
	c. **origin/mergeBranch**: This indicates that the remote branch (`mergeBranch`) on GitHub is also at this commit. This means your local branch and remote branch are synchronized.
	d. **Create README.md**: This is the commit message. It suggests that a README file was created in this commit.

2. `79dfec5 (origin/master) fourth`

	a. **79dfec5**: Commit hash.
	b. **(origin/master)**: This indicates that the remote `master` branch is at this commit. However, your local `mergeBranch` branch is ahead of this because the latest commits are not on `master` branch.
	c. **fourth**: This was the fourth commit in the repository.
	d. This commit was created on the ***master branch***, that's why it is has **(origin/master)** mentioned in this line.

### Master branch

```
ce67423 (HEAD -> master) Merge branch 'master' of github.com:sohaib-sharih/threeKey
77e1c68 (origin/master) Create README.md in master branch
dd8bb55 Merge commit 'f21f532' Merge commit after f21f532 commit was made in detached mode
f21f532 detached 406e5c0, added mergeTwo.py file
f89f1fd Merge branch 'newBranch' Merging the newBranch with master
2bc1dfe (newBranch) new merge commit
7944c4f Merge commit '406e5c0'
406e5c0 creating a new file in detached mode, then merging
4cf3817 fourth
59ad487 7th commit
0b57667 5th commit
79dfec5 fourth --> This commit is on Master branch, and is mentioned in mergeBranch log
e2de355 third
4d72b37 second commit
6caa6f3 first commit
```
#### Interpretation

1. `ce67423`: This is the commit hash for the most recent commit.
2. HEAD -> master
	a.  `HEAD` indicates your current position in the commit history. It points to the latest commit in the checked-out branch
	b. `master` shows that you're currently on the `master` branch.
3. `Merge branch 'master' of github.com:sohaib-sharih/threeKey`: This message indicates that this is a **merge commit** resulting from a pull from the remote repository. It happened because the remote had new changes that you didn't have locally. By running `git pull origin master`, you merged those remote changes into your local `master` branch.
4. `77e1c68 (origin/master) Create README.md in master branch`
	a. `77e1c68`: This is the commit hash for the change that added the README.md file.
	b. `origin/master`: This indicates the state of the remote repository's `master` branch. It shows that this commit exists on the remote repo but was not on your local `master` branch until you pulled it.
5. `origin/master` vs. `master`
	a. **origin/master** represents the state of the remote repository's `master` branch the last time you interacted with it (e.g., using `git fetch` or `git pull`).
	b. **master** is your local branch. When you pulled the remote changes, Git merged the differences, creating the merge commit (`ce67423`).
## 8.3 How to collaborate between Local and Remote Repositories.

**Scenerio**: *A reviewer is reviewing pushed code from the developer and adding commits on the REMOTE repository for further instructions, where the developer is **pulling** remote commits to apply changes and then pushing the code back to the **remote repository.***

NOTE: This can be done using the 2 commands of ***git push and git pull.***

### 8.4 Managing multiple commits to the same file

1. If you have made changes in your local repo and committed them, and different changes made to the same file in the *remote repository*, then a ***push*** from the ***local repository*** will be reject.
2. ***Solution:*** You have to ***pull*** the new commits from the remote repository, then *push* from your local repository.

```
1. vi four.py
2. Apply a new change.
3. Add it to the staging area.
4. Commit it on local only.
5. Go to your REMOTE repo, switch to the same branch.
6. Edit the same file with changes made to four.py file.
7. Commit changes on REMOTE repo.
8. git push origin master --> It will be rejected

git push origin master

OUTPUT:

$ git push origin master
To github.com:sohaib-sharih/threeKey.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'github.com:sohaib-sharih/threeKey.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

---------------------------

vi four.py (check current changes in LOCAL)

OUTPUT:
print("This is a change made in the LOCAL REPOSITORY")
print("This is a SECOND change made in the LOCAL REPOSITORY")

print("THIRD Change made in LOCAL")

-----------------------------------------

four.py (check current changes in REMOTE)

OUTPUT:

print("This is a change made in the LOCAL REPOSITORY")
print("This is a SECOND change made in the LOCAL REPOSITORY")
print("Change made in the REMOTE")

------------------------------

git push origin master(push before pulling to check rejection message)

OUTPUT:
To github.com:sohaib-sharih/threeKey.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'github.com:sohaib-sharih/threeKey.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

---------------------------------

git pull origin master (pull the changes from the remote first)
vi four.py

OUTPUT:

print("This is a change made in the LOCAL REPOSITORY")
print("This is a SECOND change made in the LOCAL REPOSITORY")
<<<<<<< HEAD

print("THIRD Change made in LOCAL")
=======
print("Change made in the REMOTE")
>>>>>>> 02857c86d3999521ac286eef4d7948b6a01dd5c6
>>>>>

NOTE: You need to add the change in file to the STAGING AREA->COMMIT to add a new commit in your LOCAL REPOSITORY.
----------------------------------

git log --oneline(check current log )

1f19ca1 (HEAD -> master) merged incoming change from REMOTE -> New Commit made on LOCAL
1566a0a new commit on LOCAL
02857c8 (origin/master) 2nd change in REMOTE on four.py
e44059f new commit for change made in LOCAL
d8ba40f change made in LOCAL
ce67423 Merge branch 'master' of github.com:sohaib-sharih/threeKey
77e1c68 Create README.md in master branch
dd8bb55 Merge commit 'f21f532' Merge commit after f21f532 commit was made in detached mode
f21f532 detached 406e5c0, added mergeTwo.py file
f89f1fd Merge branch 'newBranch' Merging the newBranch with master
2bc1dfe (newBranch) new merge commit
7944c4f Merge commit '406e5c0'
406e5c0 creating a new file in detached mode, then merging
4cf3817 fourth
59ad487 7th commit
0b57667 5th commit
79dfec5 fourth
e2de355 third
4d72b37 second commit
6caa6f3 first commit
```


## 8.5 Merging: Resolving Conflict

**Scenerio:** There are 2 developers working on the same file and applying changes in the ***same line***. When you try to ***pull*** the changes from the remote repo, it will indicate a conflict, to resolve this you will need to use the ***merge*** option.

Where there is a change in the same file and same line, GIT will identify the incoming commit and it will not ***automatically merge***, instead you will have to check the changes, fix them and resolve them manually, then save the file.

EXAMPLE
1. Make a change in four.py file on REMOTE repo, line 9.
2. Save a commit on Remote.
3. Make a change in four.py file on LOCAL repo, line 9.
4. Add the change to STAGE-> Commit on Local only.
5. git pull origin master (to pull the commits from REMOTE repo)
6. **Note:** Apply changes on master branch of both *remote and local.*

```
git pull origin master (master branch on remote)

OUTPUT:

remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 972 bytes | 9.00 KiB/s, done.
From github.com:sohaib-sharih/threeKey
 * branch            master     -> FETCH_HEAD
   1f19ca1..3a51600  master     -> origin/master
Auto-merging four.py
CONFLICT (content): Merge conflict in four.py ----> CONFLICT
Automatic merge failed; fix conflicts and then commit the result.

-------------------------------------

Terminal will show -> hree (master|MERGING) inidicating that we need to check, resolve by fixing the incoming change.
----------------------------------

vi four.py (to check incoming changes)

OUTPUT:
print("This is a change made in the LOCAL REPOSITORY")
print("This is a SECOND change made in the LOCAL REPOSITORY")
<<<<<<< HEAD

print("THIRD Change made in LOCAL")
=======
print("Change made in the REMOTE")
>>>>>>> 02857c86d3999521ac286eef4d7948b6a01dd5c6
<<<<<<< HEAD
#New line added on LOCAL, in line 9
=======
# New line of code on REMOTE   ---> Incoming change.
>>>>>>> 3a51600d17cd9ef02fc8a2178872a8346ab6dece ---> incoming commit


NOTE: Apply changes, then ESC, :wq to save and exit.

-------------------------------------------------

327. git add . (add to staging area)
328. git commit -m 'resolve conflict on line 9.'
329. git log --oneline

OUTPUT:

dcde084 (HEAD -> master) resolved conflict on line 9 from incoming commit -> Resolved
76e009d edit made on line 9 on LOCAL
3a51600 (origin/master) line 9 change on REMOTE
1f19ca1 merged incoming change from REMOTE
1566a0a new commit on LOCAL
02857c8 2nd change in REMOTE on four.py
e44059f new commit for change made in LOCAL
d8ba40f change made in LOCAL
ce67423 Merge branch 'master' of github.com:sohaib-sharih/threeKey
77e1c68 Create README.md in master branch
dd8bb55 Merge commit 'f21f532' Merge commit after f21f532 commit was made in detached mode
f21f532 detached 406e5c0, added mergeTwo.py file

```

### NOTE:
1. If you make a change on the ***same file + same line***, then there will be a CONFLICT, and git will not automatically merge the 2 files from an incoming or pull command.
2. If you make changes on the same ***file + different lines***, then it will automatically detect changes, and you will have to apply a ***commit message*** on the terminal for the incoming change.
3. You will then have to push your last commit on ***local***, to ensure both are ***synced***.
4. To check, you can verify by looking at the LAST HASH COMMIT on the file. Or you can use the **git push origin master** command twice, the first time it will sync, the second time it will give the following message on the terminal:

```
$ git push origin master
Everything up-to-date
```

### 8.6 Tracking and raising issues

1. You can **create issues** by going inside your selected repo.
2. You can create **milestones** in order to set project timelines.
3. You can assign **issues** to ***specific developers.***
4. ***Team members*** can respond and reply on issues and mark them as **closed.**
5. You can also add new ***labels***, if you don't want to use from the default presets like *bug, documentation, enhancement, etc.*

# 9.0 Branching, Merging and Rebasing

### Additional Commands to read and analyze the working tree

1. **git log --oneline --decorate --graph:** 
2. **git diff master..main**
3. **git diff main --oneline --decorate --graph**

**Interpretation**
1. **--decorate:** Shows branch names and tags associated with each commit.
2. **--oneline:** A simplified log with one line per commit showing the commit hash and message.
3. **--graph**: Visualizes the branch structure using ASCII characters, showing merge points and branch history.

### git log --oneline --decorate --graph

![[git decorate graph.PNG]]

**Interpretation of line colors:**

RED LINE

1. **Meaning:** Represents the **master branch** and its commit history.
2. **Why Red?** In many terminals, the red color is used to indicate the **active branch** (in this case, master) or the main line of history.

BLUE LINE

1. **Meaning:** Shows the **purple branch** history and how it branched off from master.
2. **Why Blue/Purple?** This color indicates a **separate branch history**, helping you visually distinguish between commits made on master versus those made on purple.
3. **Context:** You switched to the purple branch, made some commits, and then later merged it back into master.

YELLOW LINE

1. **Meaning:** Represents the **final merged state** and the **HEAD** of the master branch.
2. **Why Yellow?** This shows the **fast-forwarded** or **merged commit** that connects the histories of both branches.
3. **Context:** After merging purple back into master, the commit history has converged into a **single line**, showing the complete and unified history on master.

### Deleting branches

1. **Delete a branch from your Local Repository:** `git branch -d nameOfBranch`
2. **Delete a branch from your Remote Repository:** `git push origin --delete branchName`

### Using git gui

1. You can visualize the commits and history of commits of a selected repository through **git gui.**
2. To locate this, go to c drive->program files->git->cmd-> gitgui.exe file.
3. This file is installed when you install **git** in your computer.

## 9.1 Merge Types

There are 2 types of Merge
1. Fast forward
2. Recursive merge

#### Fast forward Merge(Two way merge)

1. This happens only when the branch being merges is **ahead** of the current branch ***without any divergent changes*** detected by git.
2. If there are no changes in both the branches, then git will return a message *already up to date.*

```
EXAMPLE:

git checkout master
git log --oneline

OUTPUT:

9270469 (HEAD -> master) added newFour.py
dec77a5 (orange) made a new.py file
c37c0a8 rm 10.py, git rm --cached 12.py, git rm eight.py
bd83188 deleted 11 and five using git rm command
2e361e9 Merge branch 'orange'
e2022f0 Merge branch 'red'
dc414b2 added 12.py on RED branch
28791b5 added 11.py on orange branch
968a71c added 10.py
51f8021 created 3 files 7, 8, 9 on Orange branch
c907dc6 first commit

----------------------------------

git checkout -b purple 
(this replicates and copies the trails of commits from MASTER branch to the new branch and switches it to the Purple branch)

git log --oneline

OUTPUT:

9270469 (HEAD -> master) added newFour.py
dec77a5 (orange) made a new.py file
c37c0a8 rm 10.py, git rm --cached 12.py, git rm eight.py
bd83188 deleted 11 and five using git rm command
2e361e9 Merge branch 'orange'
e2022f0 Merge branch 'red'
dc414b2 added 12.py on RED branch
28791b5 added 11.py on orange branch
968a71c added 10.py
51f8021 created 3 files 7, 8, 9 on Orange branch
c907dc6 first commit

-----------------------

git checkout master
git merge purple

OUTPUT:
Already up to date.

----------------------

1. Apply changes by creating a new file in Master branch.
2. Add to the Staging area.
3. Commit the change on MASTER branch
4. Switch to Purple branch.
5. Use the git merge master command again

OUTPUT:

Updating 9270469..2cc15b0
Fast-forward
 newile.py | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 newile.py

CONCLUSION: Now both branches are Syncronized.

```

#### Recursive Merge(Three-way merge)

1. This occurs when there are a new commit on both branches and they are different from each other.
2. Git will create a Merge Commit.
3. Git will consolidate the changes.

EXAMPLE

```
1. git checkout purple
2. touch newSix.py
3. git add .
4. git commit -m ''
5. git log --oneline

OUTPUT:

0873fc3 (HEAD -> purple) added empty newSix.py file
2cc15b0 (master) added newile.py
9270469 added newFour.py
dec77a5 (orange) made a new.py file
c37c0a8 rm 10.py, git rm --cached 12.py, git rm eight.py
bd83188 deleted 11 and five using git rm command
2e361e9 Merge branch 'orange'

---------------------------------------

MASTER BRANCH

1. git checkout master
2. touch newSix.py
3. Edit the file, add a print statement.
4. git add .
5. git commit -m ''
6. git log --oneline

OUTPUT:

8a98567 (HEAD -> master) added newSix.py with a print statement
2cc15b0 added newile.py
9270469 added newFour.py
dec77a5 (orange) made a new.py file
c37c0a8 rm 10.py, git rm --cached 12.py, git rm eight.py
bd83188 deleted 11 and five using git rm command
2e361e9 Merge branch 'orange'

-------------------------

git merge purple

OUTPUT:

Auto-merging newSix.py
Merge made by the 'ort' strategy.

git log --oneline(master branch)

OUTPUT:

95dcfcc (HEAD -> master) Merge branch 'purple' ---> This is the merge commit
8a98567 added newSix.py with a print statement
0873fc3 (purple) added empty newSix.py file
2cc15b0 added newile.py
9270469 added newFour.py
dec77a5 (orange) made a new.py file
c37c0a8 rm 10.py, git rm --cached 12.py, git rm eight.py
bd83188 deleted 11 and five using git rm command
2e361e9 Merge branch 'orange'

```


## Summary of Differences:

| **Feature**        | **Fast-Forward Merge**                       | **Recursive Merge**                                |
| ------------------ | -------------------------------------------- | -------------------------------------------------- |
| **When it Occurs** | No new commits on the target branch          | Both branches have new commits                     |
| **New Commit?**    | No new commit, moves HEAD pointer            | Creates a new merge commit (`M`)                   |
| **History Type**   | Linear history                               | Branching history with a merge point               |
| **Use Case**       | When no conflicts or diverging commits exist | When branches have diverged with different changes |

### 9.2 Topic: Conflicts during merge

There are 2 types of Merge Conflicts:

1. Conflict cause by working on the **same file**, but on **different lines.**

If you applied a change on the **same file** but at a **different line**, then **auto merge** will not detect any conflicts, instead it will create a new **merge commit hash** and update the files on your current branch.


EXAMPLE
```
382. git checkout master
383. git merge purple
384. Ensure that both Master + Purple are synchronized (have exact same changes)
385. git checkout purple
386. apply a new change on a new line of newSix.py file.
387. ADD + COMMIT
388. git checkout master
389. git merge purple

git merge purple

OUTPUT:
Updating d354e65..7ed363c
Fast-forward
 newSix.py | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
-------------------------------------------

git log --oneline (master)

OUTPUT:

7ed363c (HEAD -> master, purple) new line in purple ->New merge commit Auto generated.
8d1f466 new change
a4c1e0d added a new line in purple
d354e65 applied change from incoming change in newSix.py



```


2. Conflict caused by working on the **same exact line** of the **same** file.

If you make an edit on the same file and same line, then merging would indicate a conflict, and you would have to write a commit message to save the **merge commit.** And the file that had a merge conflict would indicate the incoming change, so Git would save both lines of code and the change would be marked with **arrows.**

Example (result of a merge conflict)

```
cat newSix.py

OUTPUT:

<<<<<<< HEAD
print("This is a newSix file.")
print("Adding a new line in newSix.py on MASTER Branch")

=======
print('new line')
print('Second line in Purple branch of newSix.py file')
>>>>>>> purple

----------------------------------

1. You need to MANUALLY apply the changes by deciding what to keep and what to be deleted.
2. Make the edit in newSix.py
3. Save the file.
4. Add it to staging area.
5. Commit it. git commit -m 'applied change from incoming change in newSix.py'

git log --oneline(master)

OUTPUT:

d354e65 (HEAD -> master) applied change from incoming change in newSix.py
d41d99c (purple) added 2nd line on newSix.py
7482d4f added 2nd line in newSix.py

```

## 9.3 Git stash topic

**Definition:** Git Stash helps to revert to the last commit without interrupting the current work. *Git Stash allows you to record the Current State of the working directory and the Staging Area, and reverts to a **clean working directory.***

1. If you are in the middle of some changes of branch **master**, and you need to ***switch to another branch,*** without committing any changes in the current branch you can use the following command:

```
1. vi one.py
2. Add 2 lines to the file and save it.
3. Don't commit.
4. File is modified.
5. git status

OUTPUT:

On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   one.py

no changes added to commit (use "git add" and/or "git commit -a")

--------------------------
1. cat one.py
2. Use this command to check the modifications you made WITHOUT commiting any changes.

cat one.py

OUTPUT:

"""
1. Line one
2. Line two
3. Line is WIP.
4. New line added after the 2nd commit.
5. added new line to modify after creating a new branch to check if git checkout red works to switch a branch or not.

"""
------------------------------------------------

git stash save <followed by your stash message>
git stash list (on master branch)

OUTPUT:

stash@{0}: On master: leaving 4th and 5th line modified in one.py to work on branch RED

-------------------------------

git checkout red
git stash list

OUTPUT:

stash@{0}: On master: leaving 4th and 5th line modified in one.py to work on branch RED

NOTE: The stash list was saved on master branch, but it the stash is retained on other branches as well.
```

1. When you initialy made changes to one.py, the file was modified, and when you used **git status** to check the current status, it showed that one.py is modified, *you need to add and commit.*
2. Then you used **git stash save 'stash message'** to save the modification status in stash list.
3. Now check the git status to confirm that current work in progress is stashed out.

```
git status

OUTPUT:

On branch master
nothing to commit, working tree clean
```

4. Check the contents of the modified file: **one.py** using the **cat one.py** command

```
cat one.py

"""
1. Line one
2. Line two
3. Line is WIP.

"""
```


5. Previously, you used **cat one.py** to read the modifications you made ***before stashing.*** And then you used **cat one.py** after stashing out the modifications, which had removed the applied changes from the ***current status*** and working directory as well as Staging Area.

6. Once you have worked on the other branch and want to ***resume*** your work in the master branch, you can switch back to ***master branch*** and then ***restore stash*** by using ***git stash apply*** command.

```
git stash apply

OUTPUT:

On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   one.py

no changes added to commit (use "git add" and/or "git commit -a")

---------------------------

cat one.py

OUTPUT:

"""
1. Line one
2. Line two
3. Line is WIP.
4. New line added after the 2nd commit.
5. added new line to modify after creating a new branch to check if git checkout red works to switch a branch or not.

```

7. Now you can complete your task, followed by ***adding to the staging area and commiting your changes*** in the master branch.

```
1. Complete your work in progress.
2. Just to show for testing/learning purpose add a line stating Finished.
3. vi one.py
4. Add the line Finished.
5. Save it
6. cat one.py

OUTPUT:

"""
1. Line one
2. Line two
3. Line is WIP.
4. New line added after the 2nd commit.
5. added new line to modify after creating a new branch to check if git checkout red works to switch a branch or not.
6. Work is FINSISHED.
"""
-----------------------

1. git add .
2. git commit -m 'third commit to add FINISHED'
3. git log --oneline

OUTPUT:

b3090bd (HEAD -> master) third commit to add FINISHED
902b923 (red) second commit
81648ed first commit
```

8. **git stash list:** Will still show you the Stashed out work in progress, *because we didn't use the pop command yet.*

```
git stash list

OUTPUT:

stash@{0}: On master: leaving 4th and 5th line modified in one.py to work on branch RED
```

### 9.4 Moving forward: Apply the stash on another branch

There are 2 situations that you may encounter:

1. You will either be able to apply **git stash apply** without any ***merge conflicts***, in which case you simply ***add and commit the changes*** in your new branch.
2. You will be prompted of ***merge conflict,*** in which case you will have to **manually resolve the conflicts** followed by *adding + committing.*


### Example to show merge conflict when attempting to switch branch while file is modified.

1. In this example, you have modified a file in a specific branch, but have *not* committed, not have you **stashed out yet.**

```
1. vi one.py
2. add a 6th line
3. Save and exit
4. Attempt to switch branch WITHOUT adding to staging area.

git checkout master (switching from red branch)

OUTPUT:
error: Your local changes to the following files would be overwritten by checkout:
        one.py
Please commit your changes or stash them before you switch branches.
Aborting


```

2. In this case, you have only **two options:** *commit OR stash*

Lets stash

```
1. git stash save 'stashed message'
2. git stash list

OUTPUT

stash@{0}: On red: 2nd stash before Staging modifications on branch RED
stash@{1}: On master: leaving 4th and 5th line modified in one.py to work on branch RED

------------------

REPEAT THE PROCESS.
1. git stash apply
2. git add .
3. git commit -m 'commiting to 2nd stash on RED.'
4. git log --oneline

OUTPUT

608a7bc (HEAD -> red) committing 2nd stash on RED branch
2b20569 third commit to add FINISHED from stashed
902b923 second commit
81648ed first commit

----------------------------------

SWTICH BRANCH TO MASTER
git stash apply

OUTPUT:

Auto-merging one.py
CONFLICT (content): Merge conflict in one.py
On branch master
Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
        both modified:   one.py

no changes added to commit (use "git add" and/or "git commit -a")

-------------------------------------

MANUALLY APPLY INCOMING CHANGES
cat one.py

OUTPUT:
1. Line one
2. Line two
3. Line is WIP.
4. New line added after the 2nd commit.
5. added new line to modify after creating a new branch to check if git checkout red works to switch a branch or not.
<<<<<<< Updated upstream
Work is FINSISHED.
=======
 Adding a new line to STASH
>>>>>>> Stashed changes
"""
-------------------------------

1. Apply changes manually using vi one.py
2. save changes to one.py
3. git add.
4. git commit -m 'commit message'
5. git log --oneline

OUTPUT:

* 8edaa1b (HEAD -> master) adding 2nd stash + resoling merge concflict on MASTER
* b3090bd third commit to add FINISHED
* 902b923 second commit
* 81648ed first commit

-----------------------------------

```

### 9.5 git stash show, git stash clear

1. **git stash show**: Indicates the applied and committed changes on the current branch from ***stashed out*** work in progress.

```
git stash show

OUTPUT:

one.py | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)
-------------------------------------------------

git stash list
OUTPUT:

stash@{0}: On master: leaving 4th and 5th line modified in one.py to work on branch RED

---------------------------------

1. REMOVE the stash, now that the WIP is completed
2. git stash clear
3. git stash list

OUTPUT:

BLANK, because it was deleted and cleared from the history of STASH.

```

**NOTE:** If you want to *apply the stash* and restore it using a specific stash number, then you need to do the following:

1. **git stash list**
2. Select the hash of the stash and run the following command: ***git stash apply stash@{0}***, depending on the number or level of stash you want to restore.

### 9.6 How stash works (applies on the current branch or globally?)

1. `git stash save 'message'` saves changes in a **standalone area**, **not tied to any specific branch**.
2. This means **stashes are global** and can be accessed from **any branch**.
3. **Stashes are global** and can be applied on **any branch**.
4. **Switching branches** does **not** affect the **stash list**.

## 10.0 Rebase

**Scenerio:** *When you are working on a current branch and decide to branch out, the main/master branch may populate other developers commits to it while you have been working on a different branch to complete a specific task. In this case, you can use **git rebase** to get the last commit from the main/master branch in order to synchronize.*

1. **Rebase** allows you to merge conflicts and add a new commit to synchronize the work of 2 developers working on 2 different commits when they branched out.
2. However Rebase allows you to keep the ***commit history*** of the current/master branch clean, and the changes made when you **branched out** are stored inside the Rebase Commit or R, as compared to how its saved in **commit -m**, during **git merge** process.
3. ***Never*** use **rebase** on a public branch.
4. **Rebasing** refers to moving a branch to a different commit.

NOTE: **git rebase master** It helps you to **rebase** the current branch to the latest commit in ***master branch.***

### 10.1 Difference between git merge and git rebase

1. They eventually solve the same problem, but ***differently.***
2. In **git merge**, you merge the differences of your current branch (when branched out) and the changes perhaps made in this **interim period** by another developer on the main branch.
3. In **git rebase**, your last change made on the *branched out* level are saved in the level R commit instead of being saved inside *commit -m* level.
4. **git rebase --abort:** *To abort and get back to the state before "git rebase"*
5. **git rebase --continue:** 

EXAMPLE
1. You have 2 branches called *master* that contains 2 commits and *feature-branch* that contains only 2 commits which are also available in the master branch.
2. You switch to master branch.
3. Add a new commit in master branch.
4. switch to feature-branch that already contains 4 previously made commits.
5. Using **git rebase master** on the feature-branch will allow you to pull and **sync** the latest commit from the **master branch.**
6. How will this be done?
	a. feature-branch will pull the first 2 common commits + the latest commit(3rd commit) in the same sequence that are ***common*** for both branches.
	b. Then it will add the 2 other/additional commits that were made on the feature branch and weren't available on the master branch *on top of the commits pulled from the master branch.*

 EXAMPLE practice

```
1. Add a new file in master branch then commit -m
2. check the **git log** status of bother MASTER + RED branches

git log --oneline (master)

OUTPUT:

40a5210 (HEAD -> master) added new file on MASTER only
8edaa1b adding 2nd stash + resoling merge concflict on MASTER
b3090bd third commit to add FINISHED
902b923 second commit  ---> This is at the same level as RED branch
81648ed first commit

-------------------------------------------

git log --oneline(red branch)

OUTPUT:

608a7bc (HEAD -> red) committing 2nd stash on RED branch
2b20569 third commit to add FINISHED from stashed
902b923 second commit --- This is at the same level as MASTER branch
81648ed first commit

-------------------

1. git checkout master
2. Apply git rebase red

git rebase red

OUTPUT:

Auto-merging one.py
CONFLICT (content): Merge conflict in one.py
error: could not apply b3090bd... third commit to add FINISHED
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config advice.mergeConflict false"
Could not apply b3090bd... third commit to add FINISHED

------------

1. the Shell indicated there were 2 levels of Conflicts on it: ..five (master|REBASE 1/3)
2. You have to resolve each conflict by Manually editing the conflict file, Saving + Commiting.
3. 2 Commits were made this way on MASTER branch.
4. After each commit 1/3, you have to run `git rebase --continue`
5. After all commits were added, resolving conflicts step by step, you need to keep `git rebase --continue`
6. Final output:


git rebase --continue

OUTPUT:
Successfully rebased and updated refs/heads/master.

------------------------------

git log --oneline

OUTPUT:

e281984 (HEAD -> master) added new file on MASTER only
06d66c4 fixed 2nd issue to REBASE in commit level 8edaa1b, previously resolved b3090bd
0062467 resolved conflict on one.py on MASTER 1/3 rebase
608a7bc (red) committing 2nd stash on RED branch
2b20569 third commit to add FINISHED from stashed
902b923 second commit
81648ed first commit

```

### 10.2 When to use git rebase?

1. `git rebase` is used to **move your branch** to the tip of another branch — it's like "replaying" your commits on top of the latest base.
2. Scenario 1: Keeping a feature branch updated
	a. You’re working on `feature-1`, but `main` has new commits.
	b. `git checkout feature-1
		git rebase main`
	c. Now your feature branch is based on the latest `main`.
3. Scenario 2: Cleaning up commit history
	a. Instead of merging (which creates extra merge commits), rebase makes history **linear and cleaner**.
4. What Happens During Rebase? if Git finds conflicts during rebase:
	a. It pauses the rebase.
	b. You **resolve the conflict manually** in the file.
	c. Then run:
```
git add <conflicted-file>
git rebase --continue

```

5. Does `git rebase --continue` ignore conflicts?
	a. **No**, it does **not ignore** conflicts.
	b. It **resumes** rebase **after you’ve fixed** the conflicts.
6. How to ***Resolve Merge*** Conflicts?
	a. Open the conflicted file (you’ll see markers like `<<<<<<< HEAD`).
	b. Edit and choose what to keep.
	c. After fixing:
```
git add <file>
git rebase --continue

If you mess up and want to abort:

git rebase --abort
```

## 11.0 Git clone

Cloning is the process of copy the commit history from another repository to your repository. It can be done in 2 ways:

1. **Copy the working directory**
2. **Cloning the original repository**

Cloning takes 2 arguments

1. URL of the original repository
2. Destination of the directory where cloning is saving / copying files/folders to.

EXAMPLE (Cloning a LOCAL repository)

```
1. cd ..
2. git clone five cloneFive
3. This will clone the 'five' repo to a new folder called 'cloneFive'
4. CD to the cloneFive folder
5. Currently it will only show the current branch where you were last working on in the previous ORIGINAL local repository.
6. Example if you were on master, it will indicate master only, all other branches will be hidden.
7. To show all hidden branches in the cloned repository, use git branch -a

git cone five cloneFive

OUTPUT:

Cloning into 'cloneFive'...
done.

--------------------------

1. cd cloneFive
2. git branch
3. git branch -a

OUTPUT:

git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/red

------------------------------

Git checkout to red, and other branch names and gradually all will become visible one by one.


```

### 11.1 Cloning from git repository

1. copy the URL of the git clone repository
2. Use **git clone URL of git repository** inside the folder you want to clone it to.
3. Files and folders will be copied.
4. Use **ls -lrt** to check the content.
5. Thats all.


---------------


There are generally 6 different types of Git statuses:

1. **Untracked**: Are those files that are not tracked, but were created. You need to **add** them to the git config by running the **git add** command.
2. **Modified**: If we make any changes to **tracked files**, then its marked **Modified.**
3. **Staged**: means that files were staged, ready to be **committed** and **pushed.** A file is ready to be committed.
4. **Unstaged Changes**: Files modified but not yet staged.
5. **Unmodified:** means that the file is being tracked, but no changes were made to it after adding all other files to stage.
6. **Clean State**: Confirm that there are no changes to track.


### 12.0 Forking

1. A **fork** is a copy of a GitHub repository that is created under your GitHub account. It allows you to make changes to a project without affecting the original repository.
2. Steps to Fork a Repository:
	a. **Go to the Repository** → Open the GitHub repository you want to fork.
	b. **Click "Fork"** → Click the "Fork" button at the top right.
	c. **Clone the Forked Repo (Optional)** → If you want to work on it locally, clone it using:

```
git clone https://github.com/your-username/forked-repo.git

```

d. **Make Changes** → Modify the code, commit, and push the changes to your forked repo.
e. **Create a Pull Request (Optional)** → If you want to contribute changes to the original repository, create a pull request.

#### 12.1 What is forking used for?

1. Contributing to open-source projects.
2. Experimenting with changes without affecting the original repo.
3. Keeping a personal copy of a project for customization.


## 13.0 Layout of Github Remote Repository/Dashboard

If you click on **branches** on your working remote repository, it will indicate 3 sections names *Default, Your Branches and Active Branches Section*. Below is an explanation of what each entails:

1. **Default branches**: This is the default branch set by your remote repository, or at the time when you initialized your repo. You can change this by going into **settings** of that specific repository.
2. **Your branches**: These are the branches only shown to you while you are logged in. This indicates the names of branches that you have worked on separately. All the branches that were created or pushed by you. 
3. **Active Branches:** This entails the branches you use in collaboration with team members. Indicates all the branches in the repository that have recent commits or are actively being worked on.

Table 1.1

| Branch Type     | Description                                                                                                  | How It Works                                                                                                   | Particulars                                                                                                |
| --------------- | ------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Default Branch  | The primary branch of the repository. Usually used for production-ready code or the mainline of development. | - Set in the repository settings.  <br>- New pull requests merge into this branch by default.                  | - Typically named `main` or `master`.  <br>- Only one branch can be the default branch at a time.          |
| Your Branches   | All branches that belong to you (created or pushed by you) in the remote repository.                         | - Created using `git branch` locally or directly on GitHub.  <br>- Visible under your profile's contributions. | - May include feature branches, bug fixes, or experimental branches.  <br>- Not necessarily merged yet.    |
| Active Branches | All branches in the repository that have recent commits or are actively being worked on.                     | - Includes branches updated recently (e.g., last push or pull).  <br>- Shown on the GitHub branches page.      | - Not tied to any specific contributor.  <br>- Can include stale branches if they've been pushed recently. |

### 13.1 Git Branches

Git branch commands

1. **git branch** provides the list of branches and indicates which branch you are at.
2. **git branch -M main** _to **rename** an existing branch you are on._
3. **git checkout 'branch name'** _to navigate/switch to another branch._
4. **git checkout -b 'new branch name'**: _to **replace** the name of an existing branch with a **new branch name**, and also **switch simaltaneously.** Its a quick way to replace + switch_ **Note:** this allows to copy all your last commits to the newly created branch.
5. **git branch -d 'branch name'**: This deletes the branch. _You have to switch to another branch in order to delete the branch you are currently on. In other words you cannot delete the branch you are currently on._
6. **Note:** You cannot create a new branch until you have made your first commit.
### Additional Commands

1. **ls** command allows you to list all the files in your current directory.
2. **ls -a** provides all the files and directories including hidden files and directories.
3. **git log:** provides a list of all the commits made in a chronological order with a time stamp and the Author's name.
4. **git branch**: Allows you to check which branch you're currently on, and also shows the list of branches you have created.
5. **git branch -m main master**: This command will change your default or current local branch name from main to master.
6. **git branch -d 'branch name'**: This deletes the branch.  You have to switch to another branch in order to delete the branch you are currently on. In other words you cannot delete the branch you are currently on.
7. **git checkout `branch name`** to navigate/switch to another branch.
8. **git branch < nameOfBranch >**: This helps to create a new branch.

### Git GUI

Once you are familiar with the basic CLI commands, you can better understand and learn the GUI versions. Those are more user friendly and faster with some useful features that help you save time and organize better. Git Tower is a popular example of Git GUI.


-------------------------

## GIT NOTES

Lesson Section

1. creating a git repository
2. git workflow
3. Tracking File Changes
4. Reverting to earlier commits
5. Deleting files in git
6. Ignoring files in git
7. Renaming files in git

## General Knowledge

1. Copy on **gitbash**: Highlight the text on the cli, then press shift + right/left click. Then select copy. To paste it, simply CTRL + V
2. **git checkout -:** This command takes you back to the ***previous branch***, not necessarily the master branch.
3. **Default Branch**: Used as the baseline for new development or deployment. You can change it in repository settings on GitHub.
4. **Your Branches**: Helps you track contributions made under your account. Ideal for managing individual tasks or features.
5. **Active Branches**: Useful for collaboration, as it shows ongoing work. This list may change frequently.
6. **Clean working directory**: This indicates that all changes were added and committed already, therefore the repository status is labelled as **clean.**
7. Use **touch .gitignore** cmd to create the file.
8. **Ignoring a file:** If you want to ignore a specific file, you will have to provide the **full path** of the file location from the **root folder**, along with its extension. Example /test/text.txt OR test/text.txt _can write both ways._
9. To ignore a specific file (e.g., index.html in the root directory):  
    **index.html**
4. Example for files in a specific directory:  
    If the file is in a subdirectory, include the path relative to the repository root:  
    **subdirectory/example.html**
5. To ignore all HTML files in a specific directory, use:  
    **subdirectory/*.html**
6. To ignore all HTML files throughout the repository, add:  
    ***.html**
7. **Remove the File from the Staging Area**. _If the file is already tracked by Git (i.e., has been committed before), you'll need to untrack it before it can be ignored. Use the following command:_  
    **git rm --cached 'file-path'**  
    For example, if you're ignoring index.html:  
    **git rm --cached index.html**  
    **Note:** This command will remove the file from the Git index but keep it in your working directory.
8. **Commit the Changes**. _Commit the updated **.gitignore** and any changes from the **untracked file**:_   **git add .gitignore  
    git commit -m "Add index.html to .gitignore"**
9. **What git push -u Does?**
	a. When you use **git push -u origin 'branch-name'** , you are telling Git to:
    1. Push the specified **local** branch to the **remote** repository (origin).
    2. Set the **upstream branch** for the **local** branch, which means that your local branch will be **linked** to the remote branch on the _specified remote repository (origin)_.
	b. Simplifies Future Pushes and Pulls:
    3. Once the ***upstream*** branch is set, you can simply use git push or git pull without specifying the remote and branch name. Git will remember the remote branch and automatically use it for future pushes and pulls.
    4. **git push** and **git pull**
    5. To track the **status** use **git status**
    6. It helps keep track of changes and ensures that everyone is working on the correct branches, reducing the chance of errors in collaborative environments.
    7. To check which **upstream** is the **local branch** tracking:  
        **git branch -vv**

## 14.0 Scenerios

### 14.1 How to use a local repository for both Github and gitLab?

1. Assuming that you have already pushed a project on ***gitlab***, and you want to push the same project on **github**.
2. **Add github to your remote connection:** *git remote add github `url of github repo`* You will need to create a new remote connection by the name of github or any other name.
3. **Add changes to the staging area:** *git add .*
4. **Commit your changes:** *git commit -m 'new commit'*
5. **Push your code:** *git push github main*
6. **To replace your current remote connection:** *git remote set-url origin `https://github.com/yourusername/kubernetes.git`* But not recommended, otherwise you will lose your remote connection to gitlab.
7. **Note:** Always check which branch you're at in your local system, and the default branch of your github account. Generally the default branch initialized locally is master and github is main.
8. Check the ***remote connection:*** *git remote -v*

```
git remote -v

OUTPUT:

github  https://github.com/s#$%#$%#$%arih/Ku#$%#$%#$%.git (fetch) --> New Connection
github  https://github.com/s#$%#$%#$%arih/Ku#$%#$%#$%.git (push)  --> New Connection
origin  https://gitlab.com/s#$%#$%#$%rih/ku#$%#$%#$%-projects.git (fetch)
origin  https://gitlab.com/s#$%#$%#$%rih/ku#$%#$%#$%-projects.git (pu
```

### 14.2 How do you initialize git one level up after already having pushed the current folder to github & gitlab?

1. Sometimes we end up initializing git inside the project folder itself, that means you can only work with that project folder/repository specifically. What if you wanted to have a ***parent folder*** one level up so you can push new projects inside independent subfolders of the parent folder? You can do that by the method enlisted below.

```
EXAMPLE of your situation:

Kubernetes/         ← This will be your GitHub repo (with its own README.md)
├── README.md       ← Main intro + links to sub-projects
├── project_One/    ← Already initialized with its own README.md
│   └── ...
├── project_Two/    ← Later add more projects here

NOTE:
1. You initially pushed project_One and had initialized that folder, and how after having pushed your content and keeping in mind that the working tree is clean, you can now initialize the parent directory and start using that to push your content from the parent folder.
```

2. Steps to Set It Up:
	a. **Go to your parent folder**:
```
cd path/to/Kubernetes

```
b. **Initialize it as a new Git repo** (if not already):

```
git init

```

c. **Create a new `README.md`** inside the parent `Kubernetes` folder:

```
echo "# Kubernetes Projects" > README.md

```
d. **Add contents like this** in the `README.md`
e. Connect to your GitHub repo (only if not already done):

```
git remote add origin https://github.com/yourusername/Kubernetes.git
```

f. Add and push everything:

```
git add .
git commit -m "Initial commit with parent README"
git push -u origin main

```

g. You can also change the existing remote if you don’t want GitLab anymore:

```
git remote set-url origin https://github.com/yourusername/kubernetes.git

git push origin main
```

2. **Conclusion:**
	a. Now the parent `Kubernetes/` folder is the Git repo.
    b. `project_One/` remains a subfolder with its own `README.md`, no need for a separate Git repo inside it anymore.
    c. Avoid nested `.git` folders — you can delete the `.git/` inside `project_One` if you don't need it to be an independent repo.
3. **Will there be any conflict?** *If you now push from the **parent `Kubernetes/` folder** instead of `project_One/`, this will **replace the structure** in GitHub/GitLab with the full folder layout (parent + subfolders). It won't cause a conflict as long as:*
	a. You're using the **same branch** (`main` or `master`)
	b. You **add/commit/push from the parent folder** now
	c. You’re okay with changing the folder structure in GitHub to show `project_One/` as a subfolder (which you want)
4. Conflict may occur _only_ if:
	a. You had uncommitted changes inside `project_One` that are different
	b. You try to push from both `project_One` and `Kubernetes` separately, and both are initialized Git repos
5. To Avoid Conflicts Going Forward:
	a. Delete the `.git/` folder inside `project_One/` (so only the parent `Kubernetes/` is a Git repo):
```
rm -rf project_One/.git
--------------------------
Always push from the parent folder:

git add .
git commit -m "Updated Project One"
git push
------------------------
This keeps everything clean and conflict-free
```

### 14.3 Modifying an existing git repo with new sub folders and files

1. **Why you see an arrow symbol on your git repo subdirectory?** *What Happened?*
	a. Cloned a repo.
	b. Deleted its `.git` folder.
	c. Initialized a **new Git repo at the parent level** (outside the cloned repo).
	d. Made some changes inside the subfolder (which was originally a Git project).
	e. Committed and **force pushed** to the original GitHub repo.
	f. That arrow symbol (📁 ➡️) you're seeing on GitHub means **a submodule**.
	g. Git treats folders that once were Git repos (even if `.git` is deleted) **and later added in a parent repo** as **submodules**, if not handled carefully.
	h. The folder still had some leftover Git metadata or was treated like a submodule structure when staged/pushed.
	i. You force pushed (`--force`), which ignored GitHub’s expected structure and overwrote the history.

### 14.3.1 How to FIX it? *Option 1*

1. Remove the submodule structure and push cleanly
	a. Delete the submodule folder from the parent repo:
```
git rm --cached your-subfolder-name
rm -rf your-subfolder-name

```
b. Re-add it as a regular folder (not a Git submodule):

```
mkdir your-subfolder-name
# Copy your files back into it if needed
git add your-subfolder-name
git commit -m "Fix: remove submodule and re-add as normal folder"
git push origin main

```

### 14.3.2 How to Fix it? *Option 2*

1. Start fresh (if repo size and history aren’t important)
2. Backup your work.
3. Delete the GitHub repo.
4. Create a new repo on GitHub.
5. Push your parent repo with correct subfolders:

```
git remote set-url origin https://github.com/your-username/new-repo.git
git push -u origin main

```

6. **Notes for Future**

	a. Don’t delete `.git` inside a cloned repo unless you **really know** why you're doing it.
	b. Instead of `--force`, use `git pull --rebase` or resolve conflicts when pushing.
	c. Always commit and push from the root of your actual working project, and keep `.git` only in the root.

### 14.3.3 How to use rebase option(GPT Answer)

1. **The Setup**
	a. You create a **parent folder**, e.g. `GPT-Projects`
	b. Inside it you run:
```
git clone https://github.com/your-username/old-repo.git

```
c. **Rename the cloned folder**, e.g. `nutrition-check` ➜ `nutrition-assistant`
d. **Create new files/folders in the parent folder** (`GPT-Projects`)
e. Want to track and push everything from the **parent folder** as the new structure
f.  But use `git pull --rebase` to avoid forcing changes.

2. **How to Do This (Step-by-Step)**
	a. Create Your Folder Structure
```
mkdir GPT-Projects
cd GPT-Projects
git clone https://github.com/your-username/your-repo.git
mv your-repo nutrition-assistant  # Rename the cloned repo folder
mkdir docs assets                 # Add your new folders in parent
touch README.md index.md         # Add new files in parent

Structure:

GPT-Projects/
├── nutrition-assistant/   ← (was cloned from GitHub)
├── docs/
├── assets/
├── README.md
└── index.md

```
b. Initialize Git at the Parent Level

```
git init
git remote add origin https://github.com/your-username/your-repo.git
git fetch origin main


You now have Git history connected, but not yet pulled.
```

c. Stage and Commit the New Structure

```
git add .
git commit -m "Restructured project layout with renamed folder and new files"

```
d. Pull with Rebase

```
git pull --rebase origin main

This will:

- Bring in remote commits (if any)
- Replay your restructure commit on top of the pulled commits

```

e. **Push to GitHub**

```
You now have:

- A clean history
- No force push
- A renamed subfolder + new folders all pushed from your **parent folder**
```

f. If Git shows any **conflict**, fix them manually and run:

```
git add <filename>
git rebase --continue

This avoids messing up `.git` folders or pushing submodules accidentally.
```

### 14.3.4 How to ignore a tracked file + subfolders

1. Add the following in your **.gitignore file** to ignore a subfolder from your *local parent git repo*. One `.gitignore` at the root is enough for all subfolders.
```
/project_Two/venv/
```
2. If you accidentally ***tracked*** and ***pushed*** files you wanted to ignore, what do you do?
	a. Remove it from tracking -> `git rm --cached project_Two/output.avi`
	b. Commit the changes -> `git commit -m "Stop tracking output.avi"`
	c. Now add the file in your .gitignore file -> `/project_Two/output.avi`
	d. Push your code again, now the output.avi file that was accidentally pushed before will be removed.
### Glossary

1. **git fetch:** The purpose of `git fetch origin main` is to **download the latest changes** from the `main` branch of the remote repository (**without applying them** to your local branch yet). It helps you **see what's new on GitHub** before merging or rebasing.
### Additional research required

1. git switch
2. how to setup upstream on git
3. **History**
4. ****

## License

This project is licensed under the [MIT License](./LICENSE).