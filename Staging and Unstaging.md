## Git Initialization

`git init`

>Initializes a new Git repository in the current directory. This creates a `.git` directory to start tracking changes in the project.

## Check the Status

`git status`

> Shows the current state of the working directory and staging area. It indicates which files are staged, modified, or untracked.

## Git Staging

`git add file_name`

>Stages a specific file for commit (replace file_name with the actual file name).

`git add -A`

>Stages all changes (added, modified, and deleted files) in the working directory for commit.

`git add .`

>Stages all changes (except untracked files) in the current directory and its subdirectories.

`git *.js`

>Stages all `.js` files in the current directory.

`git add **/*.js`

>Stages all `.js` files in the current directory and any subdirectories, recursively.

## Git Modified Data Restore

`git restore file_name`

>Discards changes in a modified file, restoring it to the last committed version (useful when you want to undo local changes).

<b>After restoring a file, you need to add it again (`git add`) and commit (`git commit`) if you want to save further changes.</b>

## Unstaging Data

`git rm --cached file_name`

>Removes a file from the staging area without deleting it from the working directory. This is used when you want to unstage a file after adding it with git add.

## Check Changes

`git diff`

>Shows the differences between the working directory and the staging area (i.e., changes that are not yet staged). You can also use git `diff --staged` to see the differences between the staging area and the last commit.
