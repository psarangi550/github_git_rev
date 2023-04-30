#### <ins>How to Use Git Pull Command </ins> ####

- in order to do the `git pull` we need the `local tracking branch`
- we also need to know how the `git fetch` command works
- we also need to understand `How the Merge works in git` and in git the `merge` can be happended using the below 2 approaches

    - `fast forward merge`
    - `3 way merge `

- `git pull` :- merge the `remote branch` onto the `local branch`

- when we do the `git pull` we perform the `git fetch` from the remote branch and also perform the `git merge` from the `local repo`

- while performing the `git merge` we perform the `receiving branch` is the `local tracking branch` and the feature branch is the `remote branch`

- `git pull` will update the content of the `currently checked in branch`

- rest of the branch will remain as it is as `git pull` can update the content of the one local branch 

#### <ins>How to perforrm git pull in action </ins>

- before doing the `git pull` we perform the `git checkout` to checkout to a branch  and also we need to make sure that the branch is a `local tracking branch`

- when we do the `git pull` command it will perform the `git fetch under the hood` and update the `FETCH_HEAD` file which is present in the `.git` folder

- under the `FETCH_HEAD` file we can get the details about the `remote branch` and the `SHA 1 hash code of the remote branch`

- Then after updating the `remote branch` and `remote branch SHA code` then git perform the `git merge FETCH_HEAD` which will update the `local working directory and staging Area Files as well`

- git perform the merge as the ` Latest last commit  SHA code reference of remote branch` onto the `local working directory`

- if there were no change in the `local branch` then the merge will happen using the `ff merge`

- if there were changes in the  `local branch` and the `remote branch` then we will  get the `3-way Merge` in the `local branch` and a new `merge commit` will be created 

- 

