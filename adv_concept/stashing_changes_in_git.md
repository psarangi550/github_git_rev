# <ins> Git stashing operation </ins> #

- we can save the `temporary` uncommited changes using the command as `stashing`

- we can `retrieve info from the stash` and apply `agin` using stashing 

- when we made some change and added few changes to the `staging Area` but did not commit them yet , but now if we want to checkout to a `new branch` then `git` will prompt to `commit the changes` before moving to any other `branch` by default

- in that case we can make use the `stashing` in order to save some `temporary` changes and after checking out to the `branch` again we can able to get those changes back again 

- **Perform Stashing In Action**
  
  - lets suppose we are in the `master` branch and perform few commit over here 
  - now we want to switch to the `temp` branch but want to keep the file so that after coming back to the `branch` again we can commit those changes
  -  then we can use `git stash` command in order to stash the changes 
  -  when we `stash` then changes then we can see the below things
     -  Saving the `working directory and index stat` on `temp` and `corresponding commit SHA reference`
     -  after we `stash` the changes using the `git stash` command changes will not be reflected on the `working dir`
     -  those changes will be there in the `.git/refs/stash` folder 
     -  we can see the `commit SHA` will be there on the `/git/refs/stash` folder
     -  we can see its content using the command `git cat-file -p <commit SHA>` we can see the `commit SHA` when we use the command as `git stash` command and also the `commit message` that showed when we use the `git stash` command
     - also we can check what type of object it is by using the command as `git cat-file -t <commit SHA> address` and it is of `type` as `commit` , here the `-t` mans the `type of git object saved in the commit`
     - when we use the `git stash` command `git` create `temporary commit` and save it to the `./.git/refs/stash` file
  
  - now we can switch to the `temp` branch using the command as `git checkout temp` command 
  - if we want to retrieve the changes after checking to the `master` again by using the `git checkout master` command then we have to use it as `git stash pop` , By using this we can retrieve those changes that we have save to the `.git/refs/stash` folder
  - this `git stash pop` command will help in retrieve the `preveious state` where we have the `save the temporary changes`
  - after retrieving the value if we check the `.git/refs/stash` folder then we can see that we are unable to get the `commit SHA` as those are retrieved and we can see that that it will prompt as `no such folder exists` 


- **Perform Stashing Using github Desktop**
  
  - Each `pull request` ben bound to the `specific branch` only 
  - when we switch the branches in the `github desktop` then we can see that `it will prompt` for the `Leave changes on temp` in the `github desktop`
  - now if we want to retrieve the `stash` then we can select the `view stash` after checking back to the `branch`
  - then we `restore or discard` those stash option 




