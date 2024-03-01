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
********************************************************************

# Configure SSH connection with github.

Configure SSH connection to github 

Create a private repository in your github account called "repo-lab"
Copy the SSH URL under 'Quick Setup'

Add origin in your remote repository.

```
git remote add origin <url of your git repo>
```

Verify the Operation with 

```
git remote -v
```

to remove the remote origin 

```
git remote rm origin
```
try to push in the repo but it should fail.

```
git push origin master
```

to fix the issue we need to follow 4 steps.
1. Create and SSH key
2. Add public key to github
3. Add a Private key to your workstation
4. github will use the public key that you uploaded to decrypt the comunication from private key from your workstation authanticating that you are a authorized user.

   it will be done by following 4 steps.
   create SSH directory

   ```
   mkdir  ~/.ssh
   ```

   genrate a new SSH key named "repo-key ". Note that -t represent that type of key as an RSA protocol version 2 key, and -b flag defines the number of ecryption bits as 4k
git clone git@github.com:Kuldeep12378956/DuetWebControl.git /var/www/html/your_subdirectory

   ```
   ssh-keygen -t rsa -b 4096
   ```

   copy the content of the public key &  enter that public key to the github user setting

   got to Setting > SSH & GPG keys > SSH keys

   IN new SSH key, Paste that key

   NOw ADD the Private key to your Workstation keychain.

   ```
   eval $(ssh-agent)
   ssh-add ~/.ssh/repo-key
   




