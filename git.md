# git
**What is git?** \
Git is a free open-source distributed version control system (DVCS) used for tracking changes in computer files, especially source code in software development. \
It allows multiple developers to work together on the same project simultaneously, manage different versions of a project, and allows to rollback to previous version if needed.

Git is the core technology & there are many SCM(Source Code Management) like GitHub, GitLab, BitBucket...

Using SCM allows you to:
* Seamlessly collaborate with team and work together on same project.
* Teammates can comment on changes before they're merged, ensuring quality.
* Helps to identify & resolve merge conflicts.
* Tracks every changes made to the codebase, providing clear history.
* Easily revert to a previous version (failover)


**Install git:** \
`sudo apt install git`


**git startup commands**
* Creating empty git repository: \
A git repository is a folder that git tracks the changes in it. \
To create a new local repository, run the below command in your desired directory. \
`git init` - creates empty local git repository.

* Configure git account: \
These settings are used to identify you as the author of commits in your git repository. \
`git config --global user.name "Your Name"` \
`git config --global user.email "your.email@example.com"`

* Track changes on local repo: \
`git status` - check the status of your commits. \
`git add <file>` - add files to stage. \
`git commit -m "commit message here"` - To commit the staged files. \
`git push` - pushes the committed changes to the default remote branch (master). \

* Connecting remote repo: \
`git remote add <alias> <repo-url>` - connects remote repository to the project(local repo) in the given alias(usually origin). \
`git remote set-url <alias> <repo-url>` - sets new remote repo url to the local repo. \
`git remote -v` - shows the remotely connected repository to the current local folder. \
`git push origin <new-branch-name>` - staged changes will be push to remote repo in mentioned branch.


**git unstage** \
`git rm --cached <file>` - used to remove a file from stage. (becomes untracked) \
`git rm -f <file>` - deletes the file from local repo & also from tracking.

**git branch** \
_Branches are nothing but pointers to a certain commit._ \
`git branch` - checks the current branch. \
`git branch -r` - lists all the remote branches. \
`git branch -v` - displays the last commit with the commit message from all branches. \
`git branch surya` - will create a new branch called "surya" \
`git branch -d <branch>` - to delete a branch. \
`git branch <new-branch> #commit` - will create a new branch with that commit changes. \
`git checkout <branch>` - to switch to an existing branch. \
`git checkout -b surya` - will create & immediately switch to "surya" branch. \
`git checkout -b <new-branch> #commit` - will create a new branch with that commit & switch to it immediately. \
`git checkout <file>` - will restore the file to its last committed state in the current branch. \
`git checkout <commit> -- <file>` - checkout a specific version of a file from a particular commit. \
_**HEAD** always points to the last commit on the currently checked-out branch. If you switch branch, head moves with the branch._

**git log** \
`git log` - displays date, author, comment of a commit. \
`git log --name-only` - also lists the files changed in that commit. \
`git log --decorate` - shows the commit history along with ref(branches, tags, or remotes) associated with each commit \
`git log --graph --decorate` - to see previous commit history along with the branch they were committed on.

**CLONE PUSH PULL MERGE FETCH FORK** \
`git clone <repo-link>` - To clone a remote repository to your local machine. \
`git push <alias> <branch>` - To push the changes to remote repo by mentioning the repo(alias) & remote branch. \
`git pull` - is actually two commands in 1 (git fetch & git merge) which updates the local repo with remote changes. \
`git pull <alias> <remote-branch>` - pull from (alias)repo from the mentioned branch. \
`git fetch` - fetches all the changes (origin, branches, tags) from the current repo.

**git stash** \
`git stash <file>` - stash the changes in a dirty working directory for later use. \
`git stash list` - shows the stash list. \
`git stash show <0>` - shows the files stashed in that list. \
`git stash apply <0>` - Restores the changes from the stash but does not remove the stash entry from the list of stashes. \
`git stash drop <0>` - Restores the changes from the stash and removes the stash entry from the list. \
`git stash drop stash@{0}` - Removes a specific stash from the stash list. \
`git stash clear` - Removes all stashes from the stash list.

**git undo** \
`git clean` - removes the untracked changes. check on git status \
`git restore <file>` - when you want to undo the `git checkout <commit> -- <file>` changes. \
`git restore --staged <file>` - can be used to unstage a file. (useful if a file is only staged & later modified) \
`git reset ` - reset is the command we use when we want to move the repository back to a previous commit. \
`git reset <commit>` - 