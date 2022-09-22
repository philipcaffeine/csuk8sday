# Quickstart examples for Git beginner 

1. Create a git repository, both from a directory and from cloning. Add and commit files.
2. Working with remotes.
3. Branch and merge.

## Download and install Git on your working machine

Download from below link and install Git on your working machine. 
- [Git download win](https://git-scm.com/download/win)

### Preparation 

But first, tell Git who you are with:

```hcl
git config --global user.name "Philip Chen"
git config --global user.email yourname@abc.com
```

## Create files, repo, staged, and commit the files to your repo

If you want to connect local repo to Github, folow the following.

1. Go to [Github](https://github.com/)
2. Log in to your account.
3. Click the new repository button in the top-right. You’ll have an option there to initialize the repository with a README file, just ignore it. 
4. Click the “Create repository” button.

Then, go back to your command line, or terminal in VS Code, do the following: 

```hcl
mkdir testgit
```
```hcl
cd testgit
```
#### create initial file 
```hcl
echo "# Creating testgit" >> README.md  
```
```hcl
git init  
```
#### this is the staged of the file
```hcl
git add README.md   
```
#### commit the file into repo  
```hcl
git commit -m "first commit"   
```
```hcl
git branch -M main   
```
```hcl
git remote add origin https://github.com/philipcaffeine/testgit.git
```
```hcl
git push -u origin main
```

#### View log from current git history

```hcl
git log
```

commit 1d9c8fcc1764540646b4058ce39332fb14a3815c (HEAD -> main, origin/main)
Author: Philip Chen <yec@microsoft.com>
Date:   Thu Sep 22 14:27:48 2022 +0800

## Create a new branch 

### Create a new branch 

#### see, we're in main branch now
```hcl
git branch   
```
```hcl
git checkout -b new-branch
```
#### check current branch
```hcl
git branch      
```
```hcl
echo "Editing by author of [new-branch]" >> share-file.txt
```
```hcl
git commit -a -m "Commit change on a dev new-branch"
```
#### this is the staged of the file
```hcl
git add share-file.txt   
```
#### go back to main
```hcl
git checkout main       
```

### Check out another new branch, Hotfix, and merge to main


#### create and checkout another new hotfix branch
```hcl
git checkout -b hotfix  
```
```hcl
echo "Editing by author of [hotfix]" >> share-file.txt
```
```hcl
git commit -a -m "Commit change by [hotfix]"
```
#### view branch status of all outstanding branches
```hcl
git log --graph --all   
```
#### switch back to main branch
```hcl
git checkout main   
```
#### merge hotfix branch to main
```hcl
git merge hotfix       
```

PS C:\Users\yec\OneDrive\dev_cloud\vs_code\_common_iot\14-kubernetes\testgit> git merge hotfix
Updating 8541726..074b542
Fast-forward
 share-file.txt | Bin 72 -> 134 bytes
 1 file changed, 0 insertions(+), 0 deletions(-)

#### delete hotfix branch 
```hcl
git branch -d hotfix       
```

### Now, let's merge that new-branch into main

#### switch back to main, to merge merge new-branch
```hcl
git branch  
```
#### add another new file before merge 
 ```hcl
echo "test new file" >> test.txt  
```
```hcl
git add test.txt
```
```hcl
git commit -m "add new file"
```
#### merge new-branch
```hcl
git merge new-branch    
```
```
```hcl
git push origin main       
```
```hcl
git branch -d new-branch


## End of this Lab


