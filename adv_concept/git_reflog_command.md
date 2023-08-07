# <ins> How to use reflog in git and github </ins> #

- `git reflog` command show all the ` git operation` done on a `particular repository`

- this command will show `only the changes` made in the `computer` that we have made on the `local git repo`

- it is the `log` of all operation that been performed on the `local git repo`

- if we have reseted to the  speciific commit by using the command as `git reset --option <ommit SHA>` then all the `next commits` will be removed, By uisng the `git reflog command` then we can revert back to the `original state` which was before the `git reset option` been applied

-  when we the command as `git reflog` then we can see the below details 
   
   - we can see the `commit SHA code` and the `HEAD and branch references` and we can see the info `counter of HEAD` command 
   - we can see all the `commit message` at the end while using the `git reflog command`  

- if we want to see the `reflog` for a `particular branch` then we can use the command as `git reflog show <branch name>` but if we are not checked out to the specific branch then we can see that `the head reference been changed to the name of the branch` only when we checked out then we can see the `HEAD` reference

- when we change the `branch` as the `HEAD` reference being changes those will be logged to the `git reflog command`

- All the `log in related to the HEAD` will be show as the output of the `git reflog command` if the `branch been checked out` and we are doing the `giut reflog`

- we can also checkout to a `specific commit` using the `HEAD` referece using the command as `git checkout HEAD@{<number reference>}` then those details will also be showed when we use the command as `git reflog` after checkout to the branch 

- by default the `HEAD` pointer will be `HEAD@{0}` which will be pointing to the last commit

- when we use the `Detached HEAD` command using the option as `git checkout <commit SHA>` as the `HEAD` reference changes hence those etails will also be `recorded` while we are using the `git reflog` command  

- **How to revert back the changes after using the `git reset <commit SHA>` using `git reflog` command**
  
  - when we do a hard reset using the option as `git reset --hard <commit SHA>` then all the `next commit` will be garbage collected after 30 days as thats the defsault timeline for git `garbage collector`

  - when we are also `reseting the commits` then we can see that details in the `git reflog` as we are changing the `HEAD`
  
  - hence after the reset if we want to go back we can use the command as `git reflog` command and go back to the `HEAD@{1}` where its been pointing  to the `HEAD` operation as `git chekout HEAD@{1}`

  - this `git reflog` command can be used to restore the changeswhen we perform any `destrutive operation` such as `rebasing and reset or amending the commit`

  - the `commit message reference` in the `git reflog` command will be stored for the `90 days` hence we can use the same 



  

