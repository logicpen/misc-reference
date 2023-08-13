### Contents
* [Branch Operations](#branch-operations)
* [Logging Operations](#logging)
* [Stashing Changes Temporarily](#stashing-changes-temporarily)
* [Submodules](#submodules)
* [Reverting Changes](#reverting-changes)

----------------------------------------

#### Branch Operations
* To create new branch and checkouts the branch :- `git checkout -b <branch-name>`.
* To push branch to the remote and sets the tracking information :- `git push -u origin <branch-name>`.
* To list all remote branches :- `git branch -r`.
* To copy remote branch locally :- `git fetch origin <branch_name>` then `git switch <branch_name>`.
#### Logging
* To list one commit per line :- `git log --oneline`.
#### Stashing changes temporarily
* If one has made changes in a branch then he can't checkout other branches or take pull from the remote. To do so he has commit the changes.
* Stashing is a concept in git in which we can store changes temporarily and the changes those are saved away with `git stash` command would be reverted from the working branch. After this point one can switch branch, take pull from remote and perform other git operations.
* Stash changes in a directory or a file :- `git stash push -- path/to/folder_or_file`.
* To apply the changes but keeps the changes in stash list :- `git stash apply`.
* To apply the changes and delete the changes from the stash list :- `git stash pop`.
#### Submodules
* Submodules allow you to keep a Git repository as a subdirectory of another Git repository. This lets you clone another repository into your project and keep your commits separate.
* To pull a repository with which has submodules use `git pull --recurse-submodules`
#### Reverting Changes
* To revert changes done in a file or directory use `git checkout -- path/to/file_or_directory`(doesn't remove untracked files only changes in tracked files)
* To remove all untracked files use `git clean -f`