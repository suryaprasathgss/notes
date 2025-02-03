# git

**Install git:** \
`sudo apt install git`

**Git config:** \
These settings are used to identify you as the author of commits in your Git repository. \
`git config --global user.name "Your Name"` \
`git config --global user.email "your.email@example.co`

**Creating a Git Repository:** \
A Git repository is a folder that git tracks the changes in it. \
To create a new local repository, run the below command in your desired directory. \
`git init` - creates empty local git repository.

**Git Commands** \
`git status` - command is used to check the status of your commits. \
`git add <file>` - command is used to add files to stage. \
`git commit -m "commit message here"` - command is used to commit the staged files. \
`git restore --staged <file>` - can be used to unstage a file. (useful if a file is only staged & later modified) \
`git rm --cached <file>` - used to remove a file from stage. (becomes untracked) \
`git rm -f <file>` - deletes the file from local repo & also from tracking. \
`git remote -v` - shows the remotely connected repository. \
`git remote add <alias> <repo-link>` - adds remote repository with the given alias (usually origin)

**Git Branches** \
Branches are nothing but pointers to a certain commit. \
`git branch` - command is used to check the current branch. \
`git branch -r` - lists all the remote branches. \
`git branch -v` - displays the last commit with the commit message. \
`git branch surya`- will create a new branch called "surya" \
`git branch -d <branch>` -  to delete a branch. \
`git branch <new-branch> #commit` - will create a new branch with that commit changes. \
`git checkout <branch>` - to switch to an existing branch. \
`git checkout -b surya` - will create & immediately switch to "surya" branch. \
`git checkout -b <new-branch> #commit` - will create a new branch with that commit & switch to it immediately. \
**HEAD** always points to the last commit on the currently checked-out branch. If you switch branch, head moves with the branch. 

**Git Log** \
`git log` - command displays date, author, comment of a commit. \
`git log --name-only` - also lists the files changed in that commit. \
`git log --decorate` - shows the commit history along with ref (branches, tags, or remotes) associated with each commit \
`git log --graph --decorate` - to see previous commit history along with the branch they were committed on.

**CLONE PUSH PULL STASH MERGE FETCH FORK** \
`git clone <repo-link>` - To clone a remote repository to your local machine. \
`git push` - pushes the commited changes to the default remote branch (master). \
`git push <alias> <branch>` - To push the changes to remote repo by mentioning the repo(alias) & remote branch. \
`git pull` - is actually two commands in 1 (git fetch & git merge) which updates the local repo with remote changes. \
`git pull <alias> <remote-branch>` - pull from (alias)repo from the mentioned branch. 
