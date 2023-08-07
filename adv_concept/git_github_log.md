# <ins> Advance Git Section </ins> #

- How to `revert commits`
- How to `Reset commit`
- How to `Amend commit`
- How to `cherry pick commits`
- - How to perform `stashing`
- How to perform `rebasing with squashing` which will e helpful in merging multiple commits into single commits and then perform rebasing
- Advance filtering option with `git log` option


- while cloneing we can see the no of git object as `<downloaded git object>/<total git object>`
- we can add the `git lg` command which is `by default not available` by using the command as 

    ```
        git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%C(bold blue)<%an>%Creset' --abbrev-commit"

    ```

- **Advanced Git Log Option Available**
  
  - Advance `git log` options are of 
    
    - `--oneline` 
    - `--graph`
    - `-p`
    - `--stat`

  - `git log` command actually show the `extended logs` with `complete SHA code` , `branch pointer` and `HEAD pointer` and `current local branch` and `remote branch` and `remote HEAD pointer` as well 
  
  - `git log` also show the `Author Name` and `Date of the commit` and `commit messages` as well
  
  - if we want to see the shorter version where `1 line per commit` then we can use the command as `git log --oneline` command 
  
  - this will show the `short commit SHA number`  and `short commit messages` also able top see the info such as `current checkout branch`,`branch pointer`,`local head pointer`,`remote head pointer`,`Remote Branch` as well
  
  -  we have the option of `git lg` which will show the same info as the `--oneline` option but also `show the date` when the `commit was made` and `commit author name` which is missing in `--oneline` option alson show the `graph` option over here
  
  - `--graph` option will show the `git log` with the `graph` view but the view is similar to the `git log` which is the extended version of it 
  
  - we can also merge the `--oneline` and `--graph` option which will show the view as the `oneline view` alongside the `graph view`

  - `--stat` option with the `git log` command  along with the `git log` outputed `extended info` we can see the `info` about the `number of changes` that been made to `each file` based on the `commit`
  
  - `-p` option will show all the `git log + git stat` output but also display the `changes` made to each file where `green` show the added info and `red` show the deleted info

  - `-<no of commit that we want to see>` git will only log only those many commits ex: `git log -4` show only last 4 commit over there with the `git log extended view`


**How to use the git shortlog option in git**

  - `git shortloig` command will show us the `summary of all commit made in the repo` 
  - we can see `which author make which commits` over there
  - here the `commit` will be sorted by the `AuthorName` in ascending order
  - we can see the `quantity of commit made by the specific user` by using this
  - if we want to sort by the `number of commit` that been made by the `author` then we can use the option as `git shortlog -n` option 
  - we can also see the info about the `number of author and their number of commit` by usingn the option as `-s` as `git shortlog -n -s` which will show the info such as `only author name and  their correspondsing commit number`
  - if we want to see the `author name , author email and author commit in number` then we can use the command as `git shortlog -n -s -e` or `git shortlog -nse`

**How to filter from git log command**

  - if we want to filter the `all commit` made by `particular author` by using the command as `git log --author='<name of the author>'` which will show all the `commit` made by the `specific author` also we can use the `git log --author='<name of the author>' --oneline` which will show the all the `commit` made by the `particular author` in a `shortedn view`
  
  - we can provide the `regex` expression for the `author name` which should be `in quotes` which can able to detect the `all commit` made by the `specific` user
  
  - if we want filter based on the `commit message or description` then we can use the command as `git log --grep='<sentence or messaqge>'` which can filter only those commit which have the `specific commit message thats been asked`  


**Formatting the Git Log command**

  - we have to use the option as `--pretty` in order to `pretty format` the code out in here 
  - we can use the command as `git log --pretty=format:"%H"` will show the `complete commit SHA messages` over here 
  - we have to use the command as `git log --pretty=format:"%cn:%H"` which will show the `commit author Name` and `complete commit SHA code reference` over to the terminal
  - here the `%H` refer to the `complete commit SHA reference`
  - the `%cn` refered to the `complete commit Author Name` which stands for `commiter name`
  - the `%s` stands for the `commit subject`
  - the `%h` stands for the `short commit SHA code`
  - the `%P` stands for the `parent hash`
  - the `%p` stands for abbr `parent hash`
  - the `%f` stands forn the `file name or commit subject`
  - the `%b` stands for the `commit body`
  - ther`%o` stands for the `encoding`


  - the `%an` stands for the `author name`
  - the `%ae` stands for the `author email`
  - the `%ce` stands for the `commiter email`
  - the `%cD` stands for the `commiter date or commit Date`
  - the `%cr` stands for the `commiter date relative`
  - the `%ci` stands for `commiter date iun ISO format`
  - the `%ct` stands for the `commiter epoche timestamp`
  - the `%aD` stands for the `author Date`
  - the `%ar` stands for the `relative author Date`
  - the `%at` stands for `author date in unix timestamp`
  - the `%ai` stands for the `author timestamp in ISO format`


  - we can also provide `Humnan Readable String along with the above format as below` such as 
    
    ```
        git log --pretty=format:"Author Name:%an::Short commit SHA:%h:: commit Date: %cD"

    ```

**How to Fetch Only Merge commit from the git log**

  - iin order to fetch the `Merge commit` which is auto created by the `3 way merge` or any specific `Merge commit` then we can use the command as `git log --merges` which will only show the merged commit over here we can also use the command as `git log --merges --oneline` command over here as well
  
  - if we want fetch those commit which are not merged then we can use the command as `git log --no-merges --oneline` option as well which will show the commits which are not yet merged by using the command as `git log --no-merges` command where `--oneline` is optional to collapse the result 



