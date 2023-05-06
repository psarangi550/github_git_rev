### <ins>Git Push in Action </ins> ###

- in order to perform the `git push` operation we must have the `Write` Access to the `remote repository`
- we can see `How Many commits need to push to the remote repo` with the use of &uarr; in the `vscode`
- we can also use the `-v for verbose` while pushing the changes to the remote repository
- when we do the `git push` operation then `local tracking branch will be in sync with the remote repo`
- tracking of the branch be saved in `refs/remotes/<remote name>/<branch name>`
- we can see the info about the local tracking branch using the command as `git banch -vv`
- we can see the config related changes in the `.git/config` with this file we are able to see those changes

### <ins>How to change the Auther Name While pushing the code into the remote repo </ins> ###

- we can change the `username and email of the config` by using the command as below 
    - git config user.name "&lt; your username &gt; "
    - git config user.email "&lt; your email &gt; "

- but we need to keep in mind that `local changes for the username and email` has more priority than the `global username and password`

-when the changes are in sync then we can see those `sync symbol` in the bottom of the `vscode`

- when we are in sync then we can valiodate that by using the below `cat` command

    - cat '.git/refs/remotes/&lt;remote name&gt;/&lt; branch name &gt;' (for remote)
    - cat '.git/refs/heads/&lt; local branch name &gt;' (to see it for the local)


#### <ins>creating the remote branch based on the local branch ####

- whe  we use the `git push` option `without args` then it will try pushing tio the default branch

- if we are created a new branch and try the `git push` without any args then we will get the error as `fatal error :No upstream branch`

- we can use the command as `git push --set-upstream <remote name> <branch name>`

- we can also use the option as `git push -u <remote name> <branch name>`

- we can also add the verbose by using the command as `git push -v -u <remote name> <branch name>`

- when we push the code with the `--set-upstream or -u` option then we will not be seeing the `local tracking branch as the new branch that we created` by using the command as `git branch -vv`

- as ling as the `branch is a tracking branch` then we don't need to provide the branch name while doing the `git push`



