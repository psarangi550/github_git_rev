# <ins> How to Create the SubModule using the Git Locally </ins> #

- we can add the `git submodule add` command to add the `sub module` onto the `git` but before that we need to make sure to have the `commits` subdirectory `.git` files 

- to make sure it was successful if there is `.gitmodule` in the root of the `repository`

- this `.gitmodule` is helpful for linking the `main .git` to the submodule `that we created later`

- here we can see the `commit` related to the `main module` but the `submodule` commit we are not able to see in this case 

- if the `submodule` get `out of sync` with the `parent module` then we can do that by using it as `git submodule update` command instead

- `We will learn about the delete the submodule` using the `git submodule delete command `

- while cloning as the submodule we can add as the `git submnodule add <git repo url>` which will clone the repo under the `main parent module` in this case 

- this will create the `submodule as .gitmodule` in 

- when we push the `parent` then the `.gitmodule` will going to be get pushed but the commit made on the `submodule` will not going to be pushed

- in the `parent directory` we can get the `reference of the submodule directory` but their also nothing being updated 

- if we want to make a push to the `submodule` then we have to goto the `submodule` folder and `do the push `

# <ins> How to clone the repo which has already submodule and Get all the files from the submodule </ins> #

- when we have the `git repo` with `module and submodule` inside the `git repo` and we want to `clone the parent repo` and `expect to get the submodule repo file` as well then 
when we clone `even  though the submodule info there but we are not able to get the file over there`

- if we want to fetch the `submodule` then we need to use the `git submodule init` and `git submodule update` command which will fetch all the `files in the submodule` onto the `main parent module` by replicating all the `files that are present in there`

- we can also do the `--recurse-submodules` command which will do `clone the parent as well as the submodule file` when we do `git clone --recurse-submodules <github repo>`

- but there is a problem when the `ne commit on the submodule after the parent module` in that case we wil not be getting the `updated folder` because the `parent module` will not be aware about the `submodule commits`

- if we want to get the updated file then we can get the by using the `git submodule update --remote` command over here but when we do the `git submodule update` it will check for the local changes not the remote one that been pushed

- or we can go to the `particular sub directory` and then perform the `git pull` or `git fetch ; git merge` to get the `updated files` as well

# <ins> How to delete the Submodule from the parent module using git </ins>

- if we want to remove the submodule from the parent module there are 3 things to worry about 

    - the `config` inside the `.git` folder
    - the `module` folder inside the `.git` folder
    - the `submodule` folder 

- if we want to remove the `submodule` then we can use the `git rm <submodule name>` but the `modules inside the .git folder` not removed we can delete it manually by using the `rm -rf` command and remove the `additional part from the config file present in the .git folder` and then need to perform `git add . ; git commit -m <msg> ; git push`

- 

- 

