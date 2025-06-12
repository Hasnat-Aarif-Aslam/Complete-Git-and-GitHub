# **What is Git?**


![image](https://github.com/user-attachments/assets/d30b8a16-3164-44f4-9f2b-e11b63b035d1)


# **Git Configuration:**

**Configuring Git involves defining key user settings that Git uses to track who is making changes in a repository. These configurations are stored in Git's config file.**

* git config --global user.name "My Name"
(This sets your global username. Git uses this name to label your commits.)

* git config --global user.email "someone@email.com"
(This sets your global email address. GitHub or other Git servers use this to associate commits with your online account.)

* git config --list
(Displays the current configuration Git is using (including username, email, editor, merge tool, etc.).)


---------------------------------

# **What is origin in Git?**
* **In Git, origin is simply a default alias (nickname) for the remote repository you’re connected to — usually hosted on GitHub, GitLab, Bitbucket, etc.**

---------------------------


# **Commands:**

![image](https://github.com/user-attachments/assets/642e2c0a-c16d-42e7-b247-4d6c6f44383a)

# **The status can be in any 1 of these 4 states:**

![image](https://github.com/user-attachments/assets/1d61522c-1e9b-4423-a4b6-e324b7b0df18)


![image](https://github.com/user-attachments/assets/1e32502b-6ead-4c95-b4de-b6781c3cb833)

git add
* Stages your changes for commit
* Temporary stage
* Moves changes to staging area

git commit
* Saves those staged changes permanently
* Permanent
* Records changes in local repo

-------------------------------------------



**RATHER THAN ADDING EACH FILE ONE BY ONE, WE CAN ALSO ADD ALL THE NEW(UN-TRACKED) OR MODIFIED FILES TO THE STAGED PHASE BY USING THIS COMMAND:**
* git add .


**As we know, when we clone a repo. its one original copy is on github(remote) and the other copy is present locally(our pc), so ``origin means: original copy`` while ``main means: main branch``**
![image](https://github.com/user-attachments/assets/fa1ba52a-2af6-4278-b97b-f6a7d82d0625)

-------------------------------------


# **Lets say we have just started working on a new project, now how do we setup everything?**

git init
* Purpose: Initializes a new Git repository in your local folder.
* Effect: Creates a hidden .git folder to start tracking changes.

git remote add origin paste_link_here
* Purpose: Connects your local repo to a remote GitHub repository.
* origin is the nickname for the remote repo.
* paste_link_here is the HTTPS/SSH URL of your GitHub repo.

git remote -v
* Purpose: Verifies that the remote (like origin) was added successfully.
* Output: Shows both fetch and push URLs for the remote.

git branch
* Purpose: Lists all branches in your repo and highlights the current one with a *.

git branch -M main
* Purpose: Renames the current branch to main. (Actually github has changed the name of main branch from master to main, to thats why we are doing it)

git push origin main
* Purpose: Uploads your local code in the main branch to the remote repo under the origin.

# **Branches:**
**A branch in Git is like a parallel line of development. It allows you to:**

* Work on new features or fixes without affecting the main codebase.
* Safely experiment and isolate changes.
* Merge your changes back into the main project once ready.

# **Commands:**
git branch
* To check current branch

git branch branch_name
* To create a new branch

git checkout branch_name
* To switch to that branch

git checkout -b branch_name
* To create and switch to a new branch in one command

git branch -d branch_name
* To delete a branch

# **After making changes in the branches, if we want to merge the branches with the main branch, we need to use this code:** 
# **1st Way:**
git diff branch_name    (for example: if i am at new branch right now, so i will write: git diff main)
* To compare commits, branches, files and more


git merge branch_name      (for example: if i am at new branch right now, so i will write: git merge main)
* To merge 2 branches


# **Way 2: Using Pull Request (PR) on github**

**A Pull Request (PR) is a GitHub feature used to propose changes from one branch (typically a feature branch) into another (usually main) on the remote repository. When a contributor pushes a new branch to GitHub and wants to merge their work into the main codebase, they create a PR. This allows:**
* Code review by team members

* Discussion of proposed changes

* Approval before merging

**Once the PR is approved and merged on GitHub, other developers can pull the latest changes to their local machines using:**
* git pull origin main

``Note: git pull is a Git command that combines git fetch (download changes) and git merge (apply changes locally). It is different from a Pull Request, which is part of GitHub's collaboration workflow.``


# **Resolving Merge Conflicts:**
A merge conflict happens when Git can’t automatically decide how to combine changes from two branches, because:
* Two people (or branches) changed the same part of the same file.
* Git doesn’t know which version to keep — yours or theirs — so it asks you to resolve it manually.


# **Undoing Changes:**
**CASE 1: Undo Changes in the Working Directory (Before git add)**
* You edited a file but haven't staged it.
* git restore file_name-here

**Undo git add (Unstage File)**
* You added a file to staging (git add) but want to remove it from staging
* git reset file_name-here

**CASE 3: Undo a Commit (Locally)**
* Option 1: Undo the commit, but keep changes staged
* git reset --soft HEAD~1  (HEAD means, the latest commit, and 1 means we only want to reset only 1 commit)
* Option 2: Undo the commit AND unstage files**
* git reset --mixed HEAD~1
* Option 3: Undo the commit and discard all changes (permanent)**
* git reset --hard HEAD~1

**CASE 4: Undo a Specific File to a Previous Commit**
* git checkout paste-commit-id-here -- file-name-here

**CASE 5: Undo a Commit That’s Already Pushed (Use Carefully)**
* git revert paste-commit-id-here
