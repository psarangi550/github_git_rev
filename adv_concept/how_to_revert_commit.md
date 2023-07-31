# <ins> How to Revert commit in Git repo </ins> #

- `git revert` is not a `destructive ooperation` and does not modify the `git history`

- As `git revert` can be applied on the `public branch` such as `master or main or dev`

- git revert also `discard specific commit` by creating a `Brand New commit`

- when we use the `git reset` will change the `working Dir and Staging Area` based on the `commit` provided against it and the commits provided after that will be going to get `reverted back`

- git revert will `revert the specific commit` provided against it and create a `Brand New commit` against it 

- we can revert the commit using the command `git revert HEAD` so the commit pointed against the `HEAD` will be modified 

- when we use `git revert option` as `git revert HEAD` then `git` ask for the `commit Message` for the `Brand new commit` which will `inverse the change of the Brand New commit`

- if we are happy with the `commit message` then we can use the command as `:wq`

- it will not `remove the commit we are reverting` but create a `Brand New commit` on top of the `commit` which will `inverse` the changes in the `preveious commits`

- hence `History will not be changed`

- we can verify that using the `git log -p` option where changes been done to each file for the `commit` will be displayed and we can see that `Brand New commit` inverse all the `file changes` for the commit which are being the `reseted`

- when we have a `private repo` and we made the `changes` and push to `remote repo` and later realised that `changes been pulled by some other person` and we want to `discard the changes that we have made` then we can use the command as `git revert HEAD` which will point to the specific commit and then push those changes so that if the other person pull again those changes will be `reverted back`

- with `git revert` we can revert only `single commit` but with the `git reset` we can reset `multiple commit at the same time`

- we can see the changes made with the commit with the option as `git show <commit SHA>` which will show which files were changed as a part of the `specific commit`

- if we have already use the option as `git revert <commit SHA>` and then use the `git revert <another commit SHA>` then if the `Same file been changed` from the `preveious revert i.e git revert <commit SHA>` there will be chances of getting the `Merge conflict` we need to solve that before using the `git reset <another commit SHA>`

- for resolving the `Merge conflict` we can use the `VS code option` which will show where the `Merge conflict` been happening 

- once the `merge conflict` been `solved` then we can use the `git revert --continue` which will revert the changes of the `git revert <another commit SHA>` which was paused due to the `merge conflict`

- but before doing the `git revert --continue` then we need to do add the changes to the staging Area `git add .` then we can continuw with the `git revert --continue` option as well

- 

- `git revert` will do the same thing as `git reset --mixed` been doing i.e for the specific commit
  
  - Discard the commit from the lacla git repo
  - Discard the changes from the Staging Area
  - Keep the changes in the Working DIR
  - Also create a brand new commit which is responsible to inverse the changes
  - keep the `preveious` commit as well for which it does not belong to the `destrutive operations`

- if we want to `recommit` then we need to add that to the `staging Area` first then we can do the `recommit` as its already been discarded from the `Staging Area` by default which is similar to the `git reset --mixed` option but it will also `discard` all the commit happended `after that specific commit`

- 

- 
