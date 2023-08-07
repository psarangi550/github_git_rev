# <ins> Rebasing With Squshing using Git </ins> #

- in large `public large repo` where multiple `colaberator` and many `feature branch` we should have a `rebasing with squashing mechanism` for the `pull request` to `merge the branches`

- a `single commit` having multiple `commit message` will be added to the `squshed message` which will then be merged to the `master or release` branch

- instead of performing the `3 way merging` we can perform the `rebasing with squshing` mechanism to reduce the number of `merge commit` in a `large public repo` which been used 

- this will help in making the `history` of `public repo such as main or release` branch repo clean by `making only single commit` with respect to the merge request 

- we can filter out the `merge commit` by filtering the `git log` with the option as `git log --merges`

- if we want to see the `non merge commit` and those commit which are created in individual feature branch and later got merged using the `fast forward merge or 3 way merge` then we can use the `option`  as the `git log --no-merges`

- **How to perform the rebasing with squshing option**
  
  - we can create a new repo with the `github` account as `public`
  - then we can clone the `repo` using the `repo name`
  - then we can create a `feature` branch and checkout to the branch by using the command as `git checkout -b feature`
  - then we can made `several commit` over the `feature branch`
  - in order to perform the `rebasing with squshing` we need to push the `push the feature branch to github` using the command as `git push -u <remote name> feature`
  - in `github` we can create a `pull request` from the `feature` branch onto the `main` branch by clicking on the `compare and pull request option` and click on `create pull request`
  - when we go to the `pull request` then we can go for the option of
    
    - create a merge commit :- this will be a `3 way merge` or `ff merge` based on the `main branch` to which we are merging 
    - sqush and merge :- all the `commit` will be `squashed into a single commit` in the `main branch` while performing merging , with  this option a `new commit` will be created which will have all the `3 merged commits` which is similar to the `rebase with merge commits`
    - rebase and merge :- 
  
  - now when we fo the `git pull` option and check the `master` branch which will be having a `single commit with multiple commit messages` rather than having `multiple commits`    
  
  - by using the `squashing` i.e `squash and merge` we can `merge` all the commit of the `feature branch` into the `master branch` with a `single commit` with `multiple commit messages` which behave as the `rebasing with merging options`

  - here we have `learned` how to `combine multiple commits` into a single one using the concept of `squshing` but we can do the same using the `options` from the terminal using `interactive rebasing`



