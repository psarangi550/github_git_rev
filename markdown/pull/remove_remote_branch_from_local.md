
- when we create a branch `remotely` and `pull those remote branch` and then checkout then only corresponding `local branch` will going to be get created
and tracking branch will be created which can be validated by using the command as  `git branch -vv `

- we can remove the `unnecessary tracking branch` which is not linked to the `remote repository` then we can perform the `git remote update <remote name > --prune`

- once the `tracking branch remote part gone` due to the `git remote update <remote name> --prune` then we can delete the branch using `git branch -d <branch name>` if the branch is merged or `git branch -D <branch>` if the branch is not merged


# <ins> How to Remove the Remote Branch from Local Repo </ins> #

- we can use the `--set-upstream` or `-u` for short in order to push the latest branch which created locally but absent in remote 

- when we hover over the `branches` in `remote repo` then we can see that how many commits its been lagging from the `default main branch` on the left ot how many commits its ahead from the `default main branch` on the right hand side

- we can delete the remote branch from the local terminal by using the command as 

    ```
        git push origin -d <remote branch name>
        #this will delete the remote branch from the local branch
    ```

- when we use the command as `git push origin -d <remote branch name>` then it will delete the remote branch which can be seen in terminal using the command `git branch -r` which shoe the remote repo

- we can also perform the `git remote update <remote> --prune` to update the `travcking branch` as well
