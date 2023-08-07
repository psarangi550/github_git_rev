# <ins> Usual Development Workflow while working with Public git repo </ins> #

- development workflow while working on the `specific workflow` in `development environment`

- there are `public` and `private` branches where the `public branches` can be of `master/main/dev` which are mostly protected with the owner which can be `merged` with the help of `pull or merge` request

- we have `feature` repo such as `feature1` which will be dedicated for the `specific feature development`

- when we are developing the feature with `feature` branches other collaberator can also work ontheir branch and request the main branch to megrge the changes

- if we want to get those changes i.e the `once feature branch merged to the master branch`then we can use the option as `git pull` option 

- **How to Do pull the changes made to the Public branch in github desktop**
  
  - we can create the `new feature branch` from the `github desktop` by using the `Branches` and putting up the `custom branch name` and `create new branch`
  - we can change the branch `by clicking on the branch of the current`
  - we can do the `local merge to the dev branch using the option as ` below
    
    - we need to checkout to the `master` branch from github desktop by `clicking on the branch` and then click on the `branch to merge` which will do the `local merging` and select the `merge <which branch we want to merge> branch <base> branch`
    
    - now lets suppose we have another branch `feature2` branch which already exists then `merge that we do earlier` will not be reflected on the `feature2 branch` which is already existing
    
    - But if we want to reflect those changes then we need to use the option as `choose a branch to merge into <feature2 branch>` that will help in making the `preveious changes i.e branch merge between the master/main and feature-1` available for the `feature-2` branch 
    
    - when we are using the option as  `merge <merged feature1 and main> branch to feature-2 branch` then git perform the `3 way merge` as there were changes in the `feature2` branch and a `new merge commit SHA` going to be get created

    - we can perform the `rebasing` as well which will put `all commit of the feature2 branch on top of the master or main branch`
    
    - if we are `perform pulling or merging(in case of github desktop)` then there might be chances of getting merged conflict for the same 



