# Configuring user information

#### `git config --global user.name "Your Name"`:-> _Sets the name you want attached to your commit transactions_

#### `git config --global user.email "your.email@example.com"`:-> _Sets the email you want attached to your commit transactions_

# Basic Git Commands

#### `git init`:-> _Initializes a new Git repository_

#### `git clone <repository>`:-> _Clones a repository into a new directory_

# Making Changes

#### `git status`:-> _Shows the working directory status_

#### `git add <file>`:-> _Adds a file to the staging area_

#### `git add .`:-> _Adds all files in the current directory to the staging area_

#### `git commit -m "Commit message"`:-> _Records changes to the repository with a message_

# Viewing History

#### `git log`:-> _Shows commit logs_

#### `git log --oneline`:-> _Shows commit logs in a simplified form_

# Branching

#### `git branch`:-> _Lists all local branches_

#### `git branch <branch-name>`:-> _Creates a new branch_

#### `git checkout <branch-name>`:-> _Switches to the specified branch_

#### `git checkout -b <branch-name>`:-> _Creates and switches to a new branch_

#### `git merge <branch-name>`:-> _Merges the specified branch into the current branch_

# Remote Repositories

#### `git remote add <name> <url>`:-> _Adds a remote repository_

#### `git remote -v`:-> _Lists all configured remote repositories_

#### `git fetch <remote>`:-> _Fetches changes from the remote repository_

#### `git pull <remote> <branch>`:-> _Fetches and merges changes from the remote branch_

#### `git push <remote> <branch>`:-> _Pushes changes to the remote branch_

# Undoing Changes

#### `git reset <file>`:-> _Unstages a file_

#### `git reset --hard`:-> _Resets the working directory to the last commit_

#### `git reset --hard <commit>`:-> _Resets the working directory and index to the specified commit_

#### `git revert <commit>`:-> _Creates a new commit that undoes the changes from a previous commit_

# Stashing

#### `git stash`:-> _Stashes changes in a dirty working directory_

#### `git stash list`:-> _Lists all stashes_

#### `git stash apply`:-> _Applies the latest stash_

#### `git stash apply stash@{n}`:-> _Applies the nth stash_

#### `git stash drop`:-> _Deletes the latest stash_

#### `git stash drop stash@{n}`:-> _Deletes the nth stash_

# Tagging

#### `git tag`:-> _Lists tags_

#### `git tag <tag-name>`:-> _Creates a new tag_

#### `git tag -a <tag-name> -m "Tag message"`:-> _Creates an annotated tag with a message_

#### `git push <remote> <tag-name>`:-> _Pushes a tag to the remote repository_

# Viewing Differences

#### `git diff`:-> _Shows changes between working directory and index_

#### `git diff <commit>`:-> _Shows changes between working directory and specified commit_

#### `git diff <commit1> <commit2>`:-> _Shows changes between two commits_

# Rebase

#### `git rebase <branch>`:-> _Reapplies commits on top of another base tip_

#### `git rebase --continue`:-> _Continues rebase after resolving conflicts_

#### `git rebase --abort`:-> _Aborts the rebase and returns to the original branch_

# Cleaning

#### `git clean -f`:-> _Removes untracked files from the working directory_

#### `git clean -fd`:-> _Removes untracked files and directories_

# Working with Submodules

#### `git submodule add <repository> <path>`:-> _Adds a new submodule_

#### `git submodule update`:-> _Initializes, fetches, and checks out the submodule_

#### `git submodule init`:-> _Initializes the submodule_

#### `git submodule deinit <path>`:-> _Deinitializes the submodule_

# Gitignore

#### `echo "pattern" >> .gitignore`:-> _Adds a pattern to the .gitignore file_

#### `git rm -r --cached .`:-> _Removes all files from the index and stages them for a commit_

# Useful Aliases

#### `git config --global alias.st "status"`:-> _Creates a shortcut for 'status'_

#### `git config --global alias.co "checkout"`:-> _Creates a shortcut for 'checkout'_

#### `git config --global alias.br "branch"`:-> _Creates a shortcut for 'branch'_

#### `git config --global alias.ci "commit"`:-> _Creates a shortcut for 'commit'_

# Git Help

#### `git help <command>`:-> _Shows help for a specific Git command_

# For more detailed information, refer to the official Git documentation at https://git-scm.com/doc
