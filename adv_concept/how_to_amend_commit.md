# <ins> How to Amend Option for the Git commit command </ins> #

- when we made a mistake while doing the `git commit`  on the `last commit` then this `--amend` option will be very helpful

- when we use the `--amend` option `git` will create a `brand new commit` and the `older commit` will be garbage collected 

- hence this operation can be considered as the `destrutive operation` as it changes the `history` should be done the `private branches` such as `feature-branches` but not on the `public branch such as master or main` branch

- if we want to amend the `commit message` of the `very last commit` then we can use the option as `--amend` as below 

    ```
        git commit --amend -m "<new message that we want to provide>"
        # here the git commit message will be going to get amended 
    
    ```

- this will actually `amend` the `last git commit` and create the `new commit SHA code with New Message` and preveious `commit SHA` will be garbage collected

- when we are using the `!` mark on the `commit message`, as `!` is used for `history expansion` in the `bash` hence it should be either `escaped or inserted betweensingle quote` on them

- the `commit SHA` in the `git` is based on the `content git object` itself , as the `commit message` been changed hence the `content of the git object` been changed hence it will create the `new commit SHA code` rather than using the same old one 

- if we want to amend of the author while doing the `git commit` then we can use the option `--amend` and `--author` for the same by below 

    ```
        git commit --amend --author="User Name <email address>"
        # here the git commit message will be going to get amended 
        #here it will open the VIM prompt with the `preveious commit message` which we can amend or keep it as it is as per the requirement 
        #here in this case as we are changing the author also we care changing the content of the git object hence the `new commit SHA` will be generated and the `old one will be garbage collected`
    
    ```

- we can't use the `--amend` or `--amend and --author` with the `older commit` but it can only be applied on the `last commmit` only


