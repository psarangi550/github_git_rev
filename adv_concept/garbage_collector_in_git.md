# <ins> Garbage collection in Git and How to perform Garbage collection on dediscardpackmand </ins> #

- `garbage collection` is an ativity pperformed by `git` from `time to time`

- by using `garbage collection` git perform all the removal of `unreachable object` and `git reflog` as well 

- we can also run the `garbage collection` git on demand , which will not delete the `obsolete folder` but `pack` the `git object` in the `pack` file 

- `pack` file is the `git object` which will allow us to store the `git object` on the `archieve ` so that ` git repo object` can be less size

- when we download the `git repo` using the `git clone` command from the `remote server` then `packed object in pack file` will be downloaded and on demand `git` will unpack those `packed object in pack file` on demand  

- we can select the `discard changes` option from `VS code or GitHub (By right click and discard changes)` in desktop

- when we go to the `.git/object` folder then we can see the `pack` folder as well 

- when we see the content of the `pack` by using the command as `.git/objects/pack` then we can see the below files 
  
  - one is of `.idx` file and another will be of the `.pack` file 

- when we perform the `garbage collection` then git will `select the unreachable object and relog` from the `.git/objects` folder and save to the `pack` folder

- we can perform the `garbage collection` using the command as `git gc`

- after performming the `garbage collection on demand` using the command as `git gc` then we can see the `folder` that is `.git/objects` folder will be little less as they are save to the `pack` folder and if we see the id of the `.idx` and `.pack`  file is now being changed




