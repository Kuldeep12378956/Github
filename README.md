# Github

### To check the git installed or not 

```
git --version
```
### configure git in your local workstation 
```
git config --global user.name "kuldeep.kumar"
git config --global user.email "kuldeep@arintech.in"
```

### Verify the setting by 
```
git config --global --list
```

### Set Editory for your Workstation. In my case I want to keep VIM
```
export EDITOR=vim
```

### TO open the Editorgit config --global --edit 

```
git config --global --edit
```
### Create and initialize the local git repo

#### First create a directory, Go inside it, Check if it is git repository or not.
#### to check below is the command
``` git status```    

### To initialize the git in repository.

```
git init
```
### verify the repo has been initialized by 

```
ls -al
```

### Go inside the .git repo and cd .. 
Now if you run the git status command you will be able to see the current branch 

```
git status
```

### Now lets run some important commands.

First make some files inside the repo and add them in the stages by command 

``` git add```

Then make some changes in the file and do commit those changes.

``` git commit```
It will ask you for the message to be added in the commit.

Again check the status after commiting. 
``git status```

### to check the commit history command is 

``` git log ```

### to check the details of perticular commit. you can use git show command but also have to add SHA along with command. below is the proper command.

``` git show dafjafljafhakaoowoihjac ```

### to check the difference between the two commits. 

``` git diff <first SHA> <second SHA> ```

********************************************************************************************

# Git Branches.

# git branch command will show you which branch you are working on with asterrisk sign in front of it.

```
git branch
```  

### create and checkout new branch 

``` git checkout -b testing ```

verify your in the New branch

``` git branch```

switch back to the master branch

``` git checkout master```

### git switch is the command you can use to switch the branches

```
git switch master
```

# Merging

to merge the testing branch into master branch

``` git merge testing ```

#Deleting 

``` git branch -D newbranch ```

#########################



