### Squash and Rebase workflow
* In this workflow we first squash our commits in our feature branch to a single commit then we rebase our feature branch from the up to date main or master branch. Following are the steps:
1. First we squash all the commits in our feature branch to a single commit, so first checkout to the feature branch and use any of the following commands,
    * `git rebase -i HEAD~[number_of_commits]`(number of latest commits we want to squash)
    * `git rebase -i [commit-hash]`(let's say we want to squash latest 3 commits then we have to chose the hash of the 4th commit)
2. Push to the remote branch by `git push` but if we already pushed our code to the remote then we have to force push the squashed commit by `git push -f`.
3. Checkout to the master and pull the latest code from remote to the local master branch then again checkout to the feature branch and rebase from the latest master branch by using command:
    * `git rebase master`(also it's safe to keep a copy of the feature branch before rebase).
    * Resolve conflicts if any, run builds and tests etc.
    * Force push to the remote branch by running `git push -f`.
4. Crate merge/pull request in the remote repo. We can also merge feature branch to the master branch locally by running following commands:
    * `git checkout master`
    * `git merge feature-branch`
    * `git push origin master`