
- when we create a branch `remotely` and `pull those remote branch` and then checkout then only corresponding `local branch` will going to be get created
and tracking branch will be created which can be validated by using the command as  `git branch -vv `

- we can remove the `unnecessary tracking branch` which is not linked to the `remote repository` then we can perform the `git remote update <remote name > --prune`

- once the `tracking branch remote part gone` due to the `git remote update <remote name> --prune` then we can delete the branch using `git branch -d <branch name>` if the branch is merged or `git branch -D <branch>` if the branch is not merged


# <ins> How to Remove the Remote Branch from Local Repo </ins> #

-  