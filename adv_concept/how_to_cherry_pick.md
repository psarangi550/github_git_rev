# <ins> cherry picking in git </ins> #

- cherry picking allow us to take `any commit` and `apply/insert` to the `currently checked out branch` as the `last commit`

- it is `not a destrutive operation` but rather create `new commit SHA` while performing this action 

- **senario:-1**

  - lets suppose we are working on the `feature` branch, we have `multiple commit` on the `feature branch` , but we want only one commit as a bug fix `on the master or main` branch then we can use the `cherry pick the commit SHA` and add that to the `master/main` branch

- **Another Senario**

  - if we moved to the `Detached Head` by checking into the `commit SHA` and made few `experimental commit` on top of the `checkout commit SHA` and we don't want to create a `Brand New branch` from the `Last experimental comit`  in order to retain the `experimental commit` then those `experimental commits` can be cherry picked to the `master or main or public ` to keep the changes 

- **senario1 Demo**

    - we can create a `temp` branch and make some `commit` over there
    - we can return to the `master` branch and cherry pick the `commit` and add them to the `master` branch

    - then we can create the branch using the command as `git checkout -b temp`
    - then we can add some commit over there using the command as `git add .` and `git commit -m "msg"`
    - then we can checkout to the `master` branch by using `git checkout master`
    - then we can cheery-pick the commit made in the `temp` branch to master branch using the command as `git cherry-pick <commit>`
    - there might be chances of the `Merge conflict` after solving the `merge conflict`
    - we can use the command as `git cherry-pick --continue` then `it will prompt for the cherry-pick commit message`
    - we can either `amend` or `keep` it as it is then `:wq` to exit and the `cherry-pick` been done
    - here the `commit message` will be same as the `commit we have done in the temp branch` but the `commit SHA` will be different as `content of the object` been changed as the `Date and time of the commit being changed `

    - we can use the option as `--no-commit` option to `cherry-pick` command  which will add the `file` that been changed in the `temp branch with the commit` in the `Staging Area` but will not commit to the `local git repo`
    - we can add and commit it again to make it as tracked and pushj to `local git repo`
    - we can also see the `git status` with `verbose` option as `git status -v` command but this command will only show the changes in the file which are in the `staging Area` no on the `working Directory`

- **Another Senario Demo**
    
    -  

