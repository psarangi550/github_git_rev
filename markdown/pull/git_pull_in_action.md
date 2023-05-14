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

- `git pull -v` which will show the verbose show all the changes done by the `git pull` command

#### <ins> What is FETCH_HEAD in git pull command </ins> ####

- we can also put the verbose option with the `git fetch` command as `git fetch -v`

- in order to see that `FETCH_HEAD` we have to go for the `.git` folder where we can see the folder as `FETCH_HEAD`

- we also have the `HEAD` folder inside the `.git` folder which been pointing to the `current checkout branch`

- when we see the `FETCH_HEAD` file by using the command as `cat FETCH_HEAD` command then we can see the `current checkout branch remote SHA1 code and  branch name and url` and also the `other branch SHA1 code  and other branch and url of that branch `

- when we use the `git pull` command then git usually do 2 things

    - git wrote the `git fetch ` command and get the `SHA1 and branch and url ` into the `FETCH_HEAD` folder 

    - inside the `FETCH_HEAD` file we can see the `current branch (remote) SHA1 code and branch name and url` also other branches which marked as `not  for merge` with `SHA1 code and branch name and url`

    - then git perform the `git merge` command so that `git merge FETCH_HEAD` which will ignore the `not for merge` branch and only perform the `git merge FETCH_HEAD` for the currently checkout branch

    - when we do the `git pull` then git compare the `commit of thr local branch` is in sync with `commit of the Remote branch which can be fetched from the FETCH_HEAD file` and if same then says as `Already up to date`


#### <ins>How to Use the `Git Pull` with Fast Forward Merge </ins> #####

- we can create a `new folder` in the `github` by using the `<foldername>/` with that we can create a new folder 

- before doing the `git pull` we must checked into the `branch` from where we want to do the `git pull`

- when we use the `git pull` where the changes been made in the `remote repo` but not in the `local repo` then `git pull` command will upload the `local branch` onto the `remote branch` and `compare the same`

- then once the `compare` been done and confir that in the `local branch` there were no changes then only `git fetch` command being executed

- it will show the `new commit` of the `checkout branch` based on the `remote changes` that being refered

- we can see the `particular branch contents ` nby using the command as `ls -la <branch name>` which will show the content of the `content of the working directory`

- we can see that `staging Area Content` using the command as 

    ```
        
        git ls-files -s

    ```

- when we do the `ff merge` then it will just change the `pointer of the local commit` to the `remote commit that was extensively made `

#### <ins>How to Perform the `Git Pull` with 3 way Merge Approach </ins> ####

- when we do the `git fetch -v` then the contents of the `remote repository` which been changed will be save to the `.git/objects/<first 2 letter of the remote repo commits>`

- but when we do the `git fetch -v` then it will not `merge` the changes of commit present in `.git/objects/<2 letters od the remote repo>` inside that rest of the `commit details` into the `local branch`

- we can see the `author and commit details` by using the command as `git cat-file -p <few letter of the commits>`

- we can see the type of object by using the command as `git cat-file -t <few letters of the commit id >`

- when we made the `git fetch -v` then it also changes the `FETCH_HEAD` content as well with the latest commit details 

- when merge happended using the `get merge FETCH_HEAD` using the `3 way merge statergy` then it will be displayed as the `Merge made by recursive Statergy`

- when the merge happended using the `3 way merge` then there will be new commit which will point to the `2 parent commits` one for the `local branch` and `one for the remote branch`

- if we have made the changes `locally` then we need to push the changes at the end by using the command as `git push ` command otherwise the `remote branch` will not be aware about the `local changes` even though the `local changes aware about the remote changes`


#### <ins> How to Solve the Merge Confilct when the Same file being changed locally and Remotelly and Trying to pull those changes out </ins> #####

- we can exit the nano editor by executing the `ctrl+O` and `save` and `ctrl+x` to exit

- when we edit the `same content of the same file` then for those `merge conflict` will occure but `git fetch -v` option will pull the latest `code-change` into the same and show the `commits` changed from `older--->New` one

- but while doing the `git merge FETCH_HEAD` git will see theat same file being changed locally hence raise a `merge conflict`

- `visual studio` display that there is merge conflict with the option as `c`

- we have 3 options ion vs code those are 

    - current local changes
    - incoming remote repo changes (it also display the SHA-1 hash code)
    - both changes


- when we have the `merge conflict` in a `file` we can see `3 file version` in the staging area if we are doing the `git ls-files -s` option

    - 1st one the version before changes made to local or remote repo
    - 2nd one the version with the local changes which is the receiving branch for `git pull`
    - 3rd one the version with the remote changes which been coming from the `remote repo` while doing the `git pull`

- if we don't want the changes of both `local and remote repo` then `Delete from <<<<HEAD to the (commit SHA1 hash of the remote repo)`

- once we sorted the `merge conflict` then `commit the changes` then we can see that `conflict been resolved` and `one final version file` exists in the `staging Area`

- A new `commit SHA1 code` will be generated when we resolved the `conflict` and made the commits and which has the parenbt as the `local changes` as well as the `remote changes`

- but the `remote branch` still not pointing to the merge conflict `commit ID` as its not pushed to the `remote repo`

- 









