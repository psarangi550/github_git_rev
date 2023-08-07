# <ins> Rebasing with Squashing using the interactive rebasing </ins> #

- if we want to perform `rebaing with squshing in order make multiple feature branch commit into a single commit` then we need to use the concept of `interactive rebasing` using the option as `rebase -i` option from the `git terminal`

- if we want to do that using the below options :---->

  - we need to create a new branch using the option as `git checkout -b feature1` from the `main or master` branch
  
  - we can create `multiple commits` over there using the option as `git add .` and `git commit -m "<msg>"`
  
  - in order to perform the `interactive rebasing` to perform the `rebasing with squshing` we need to do the below steps 
  
  - here we need to rebase the `feature1` branch on top of the `master` branch using the option as `git rebase -i HEAD~3`, which will `sqush last 3 commits` into a `single commit`
  
  - or we can mention the `last commit before we made the feature1 branch i.e last commit of the main branch` branch after creating the `feature branch` as `git rebase -i <last commit of the main branch / last commit before the feature1 branch created>`
  
  - this will open the `vim commit message window` and we need to `edit` in order to make the `multiple commit into a single commit`
  
  - all the `commit messages` will be showned in the `vim interactive terminal`
  
  - then we need to  `squash` `all commit` into a `single commit` then we nee to use the `replace the PICK before the commit into SQUASH/S before the commit message` but we need to `leave first commit of the feature1 branch` except that we can replace the `word PICK with word S` for the options for the `rest of the commits` in order to `sqush the rest commit along with the first commit` into a ` new single commit` with `multiple commit message` based the `commit` we madee to the `feature1` branch 
  
  - when we do the option as `:wq` then we can see that it will show all the `commit message` that need to be added then we can select the options again as `:wq` which will create `new commit id` will going to be get created on based of that having those `3 commit messages`
  
  - then we we do the `git lg` or `git log --oneline` then we can see that `all the commit` been `squashed` into a single commit
  
  - but we can see the `al commit messages` in the `new commit` that has been created

  - then we can do the `feature1` branch into the `master/main` branch using the command as 
    
    - git checkout master/main :- which will checkout to the public master or main branch
    
    - then we can perform the options as `git merge -v feature1` which will merge the `feature1 branch` which currently having a `single commit` into `master branch`
  
  - as we are performing the `rebasing` before `performing merging` with the `git rebase -i` command hence `fast forward` merge going to happen as in case of the `rebasing` we are putting the `feature` branch on top of the `master/main`  branch
  
  - hence an `fast forward` merging will going to happen in that case as the `feature-branch` put on top of the `master branch`

  - `rebasing` will put all the `commit of the  feature branch` on top of the `master/main` branch
  
  - in case of the `interactive rebasing with git rebase -i` option we can see that `all the commit will be merged into single commit` and put on top of the `master or main` branch
  
  - now as the `fast forward merge` happen hence `pointer of the main/master branch` will be now moved to the `last commit` of the `feature branch` but as we have done the `interactive merging` there will be only `one commit` and `branch pointer and head pointer` from the `master or main branch` will move to the `single commit of the feature branch` as the `ff merge been happend`

  - then we can push those changes into the `github` by using the option as `git push`

  - `rebasing with squshing` can be performed with the help of the `github with squash and commit option` or by using the `interactive rebasing from the terminal`

  - we can either pass the `SHA1` hash for the `git rebase -i` or pass the `HEAD` reference for the same 









