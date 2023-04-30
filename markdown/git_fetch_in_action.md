#### <ins>Usgae of Git Fetch command </ins> ####

- when we create a `new branch` in the `remote branch ` those branch will not be automatically listed in the `local repository`

- by using the `git fetch` command we can bring the `remote branch that newly created ` into the `local repository`

- we can `git fetch` on any of the branch that was created 

- `git fetch` command uses the `git remote -v` option and find the `fetch url` to associate the newly created `remote branch` onto the `local repository`

- this `git fetch` command will create the `remote branch` only which we can see by using the   command as `git branch -a` or `git branch -r`

- but it will not be added as the `tracking branch ` in the `local git repository`

- we need to checkout to the `remote branch` in the `local git` in order to create the `local tracking branch based on the remote branch`

- we can checkout using the command as `git checkout <remote branch name> `

- we can see the tracking branch using the command as `git branch -vv`

- if we delete the `remote branch` from the `remote repo` which is `locally tracked` then we can see the details by using the command as below 

    ```
        git remote show <remote name>

    ```

- this will show the `deleted remote branch name ` as the stale branch 

- if we want to delete that `stale branch then we can use the command as `

    ```
        git remote prune <remote name>
        #this will remove the stale branch which is being removed from the remote repository

    ```

- when we use the `git remote prune <remote name>` then that will remote the `remote stale branch` but the `local branch will still be there`

- now if we do the `git branch -vv ` then this will display the `local branch` but the corresponding `remote branch` will be gone

- we can also recreate the `remote branch` then we need to push the changes as `git push origin <same name as the local tracking branch which we want to create on the remote repo>`

- if we delete the `local tracking branch` then we can do  that by using the command as `git branch -d <local tracking branch which we want to remove>`

