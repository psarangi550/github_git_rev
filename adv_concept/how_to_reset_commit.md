# <ins> Git Reset command in Git </ins> #

- these command can `modify` the `git history` , hence its a `destructive command`

- the `git reset` command wiull help in `discard the commited changes` 

- when we made some `commit` but want to `discard the commit` later and bring to the `preveious stage` then that can be done using `git reset` command

- the `git reset` has 3 options

    - git reset --hard
    - git reset --mixed (default)
    - git reset --soft

- based on those option `working dir` or `staging Area` or `git local repo` will get afftected

-  when we want to reset to a specific commit all the commit made after that will be reseted 

- when we usew the command as `git reset <commit short SHA>`  then there will be unstaged changes

- this will by default `send the file commited with the commit SHA back to the working DIR not thew staging Area ` 

- but the `changes` will be there in the `working directory` not to the `staging Area` , here changes were discarded from the `local git repo` and `staging Area` as well 

- when we apply the `git reset` which will by default refer to the `git reset --mixed` mode which will do the below thing

  - Discard the commit
  - Discard the changes from the Staging Area
  - keep the changes in the Working Directory

- In order to commit them again `after changes` we need to stqage them first as they been discarded from the `staging Area`

- when we discard the `changes` then those commit will be `changed compared to the preveious commit that we have`

- when we apply the `git reset --soft <commit SHA code>` then below things will happen

    - Discard the commit from the local git repo
    - Keep the changes in the Staging Area
    - Keep the changes in the Working Dir

- here we don't want to `stage the changes` as its already done and we just need to `commit the changes` in here

- but the `commit SHA` of the new one will be different from the `commit SHA of the old One`

- when we do a `hard reset` using the option as `git reset --hard <commit SHA code>` then 

  - Discard the commit from the local git repo
  - Discard the changes from the staging Area (index)
  - Discard the changes from the Working Directory as well

- as its not `keeping the changes in the working Area or Staging Area` the files changes will be removed after the `git reset --hard option`

- this is the `most desctive operation` out of all `git reset command`

- but when we doing the `git pull` again then we can get back all those changes if the `preveious changes pushed to the remote repo`

- all these `git reset command` should be applied to the `private branch such as ` feature branch not the master branch

- we can also use the `HEAD` reference to do the `reseting` as `git reset HEAD~4` which will `reset` to the `HEAD-4` commit

- here the `~` symbol can be considered as the `-` from the `HEAD` pointer as well

- by default the `reset` applied with the `mixed` option over here

- when we are doing the `git reset --hard` then we can use the `git pull` option freely as there are no changes in the `working Dir or staging Area`


