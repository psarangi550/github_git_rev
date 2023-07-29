# <ins> Rebasing Internal Work </ins> #

- when we rebase then git moves the `HEAD` to the `last commit` of the `base or master` branch

- Then git perform `rebaseing` the `feature` branch ontop of the `last commit` of the `master` branch , here in this process `multiple duplicated commits` will be created based on the `commit` on the `feature` branch and the `old commit` of the `feature` branch will be garbage collected

- then we will `Merge` the `new last commit` of the `feature` branch ontop of the last commit of the `master` branch by using the `fast forward merge` so that there will be non need of a `New Merge commit`

- we can see the `git log` with the `graph` option as `git log --graph`

- every commit after the `rebasing` should have only `one parent`

- in case of the `rebasing` the `feature and master` branch point to the `same commit` after the `rebasing been completed`

- in case of the `normal merging using the 3 way merge` the merge commit created `after all commit` in branches `which are going being merged` 

- when we are using the `rebasing` then the `all the commit` of the `feature branch` will be shown after the `master brqanch last commit` which is not actually correct

- when we check the `log` using the `git log --graph` option then we can see the `even though for the feature branch new duplicated commit are created` but their `time` showing `preveious` to the `last commit on the master branch` which is actually not correct , because in `git` all commit should be performed after the `preveious commit` , but that does not happen in case of `rebasing`

- if we want to see the `commit object details` then we can use the command as `git cat-file -p <commit SHA ID>` which will show the `info` such as 

    - whats the type of ` git object` that be a `tree or blob` object 
    - parent `commit SHA ID` for the `specific commit ID` that we are seeing 
    - author name which will show when the `original commit SHA created time will show`
    - commiter name `which will show the time when branch got rebased and new commit ID generated`

- we can remove the `feature` branch after the rebasing been done and the `branch goit merged`

- we can delete the branch using the command as `git branch -d/-D <branch name>` , if the branch not merged then we casn use the command as `git nbranch -D <branch name>` and when branch been merged then we can use the command as `git branch -d <branch name>`

- when we push the `changes` on to the remote repo from remote repo also the `corresponding remnote branch of the deleted branch` also goit deleted

-
