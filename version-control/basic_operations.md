#### Create New Branch And Push :-
* `git checkout -b <branch-name>` :- Creates new branch and checkouts the branch.
* `git push -u origin <branch-name>` :- Pushes branch to the remote and sets the tracking inforamtion.
#### Get Short Hash :- 
* `git log --oneline` :- 
#### Stashing changes temporarily :-
* If one has made changes in a branch then he can't checkout other branches or take pull from the remote. To do so he has commit the changes.
* Stashing is a concept in git in which we can store changes temporarily and the changes those are saved away with `git stash` command would be reverted from the working branch. After this point one can switch branch, take pull from remote and perform other git operations.
* `git stash push -- path/to/folder_or_file` :- stash changes in a directory or a file
* `git stash apply` :- to apply the changes
#### Submodules :-
* Submodules allow you to keep a Git repository as a subdirectory of another Git repository. This lets you clone another repository into your project and keep your commits separate.
* To pull a repository with which has submodules use `git pull --recurse-submodules`
#### Revert Changes To a Specefic Commit :-
* To revert changes done in a single file use `git checkout -- path/to/file`