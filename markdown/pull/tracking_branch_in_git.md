### <ins> Trcking Branch in Git </ins>

- traking branch is the `local branch` which is connected to the `remote branch`
- the `default local branch` while clone will same as the `remote default branch`
- checking out the `remote branch` which is not present in the `local branch` will create the `tracking branch` which is a branch is present in both `local branch` and `remote branch` but refer to the `local remote branch`
- `git branch -vv` will show the `tracking branch` present in the `tracking branch`

#### <ins> How to create the tracking branch in the local git repo Based on Remote Branch </ins>

- by using the git checkout `git checkout <remote branch which not yet track but we want to track it>`

- we can now see the tracking the branch as `git branch -vv ` which will show all the tracking branch

- git `allow` us to `delete the branch` if its `not checked out` and `not merged to the remote branch`

#### <ins>Alternate Way to See the Tracking Branch </ins>

- `git remote show <remote repo name>` which will show the `urls for fetch and push` but we will also be see the info about the `tracking branch as well`

