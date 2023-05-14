#### <ins>Git Pull Fetch and Push </ins>
- if the changes are made on the `Remote Repository` and we want to reflect those changes in the `local one` then we can use the command as `git fetch` or `git pull`
- `git pull` = `git fetch` + `git merge`

- `git fetch` will not effect the `local working repository or staging Area` after getting the changes from the `remote repository` it just update the working `local git repo` which we push by using the `git commit` command

- all the `branches` were listed in the `.git/refs/heads` folder section

- when we create a `new branch` in the `remote repository` then those branches were not listed in the `local repos` by default

- but when we do the `git fetch` those will be displayed on the `local repository` saving the branches onto the `.git/refs/heads` folder section

- but the `git pull` command changes the `local git repo + staging Area Files and the local working directory `

- `git pull` under the hood uses the `git fetch cmmand` to get the latest update from the `remote repo` and then perform a `git merge` for the `local working directory and staging Area`

#### <ins> How to Local Git Repo Connected to the Remote Repo </ins>

- when  we clone the remote repository to local git repository then `git` create a default remote repo named as `origin`
- when we connect the `local repo` to multiple remote repo then we must have `different remote repo` name 
- when we use the `git pull` then it will pull from the default remote repo which is of `origin`
- by using the command as `git remote` we can see all the `remote repository` connected to our `local git repo`

- when we use the `git push` or `git pull` or `git fetch` then it will be with respect to the `remote repository`

- by using the option as `git remote -v` we can see `origin i.e name of the remote repo` and the `url of the remote repo` but those will be 2 in number one for the `fetch` and other `push`

- when we use the `git branch -a` this will list all the `local` and `remote` branch where the `remote branch` starts with the value as `remotes/<remote repo name>/<remote branch name>`

- we can also that against the `remote repo` name we have the  `HEAD` reference as `remotes/<remote repo>/HEAD ---> <remote repo name>/<remote default branch>` which tells that the `current default remote branch name`

- we can use the command as `git branch -r` which will show the `remote branch` inside the git repo



