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
git config --global user.email yec@microsoft.com
```

## Create files, repo, staged, and commit the files to your repo

If you want to connect local repo to Github, folow the following.

1. Go to github.
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
```hcl
echo "# Creating testgit" >> README.md  # create initial file 
```
```hcl
git init  
```
```hcl
git add README.md   # this is the staged of the file
```
```hcl
git commit -m "first commit"   # commit the file into repo  
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

View log from current git history

```hcl
git log
```

commit 1d9c8fcc1764540646b4058ce39332fb14a3815c (HEAD -> main, origin/main)
Author: Philip Chen <yec@microsoft.com>
Date:   Thu Sep 22 14:27:48 2022 +0800


## Create a new branch 

### Create a new branch 

```hcl
git branch   # see, we're in main branch now
```
```hcl
git checkout -b new-branch
```
```hcl
git branch      # check current branch
```
```hcl
echo "Editing by author of [new-branch]" >> share-file.txt
```
```hcl
git commit -a -m "Commit change on a dev new-branch"
```
```hcl
git add share-file.txt   # this is the staged of the file
```
```hcl
git checkout main       # go back to main
```

### Check out another new branch, Hotfix, and merge to main


```hcl
git checkout -b hotfix  # create and checkout another new hotfix branch
```
```hcl
echo "Editing by author of [hotfix]" >> share-file.txt
```
```hcl
git commit -a -m "Commit change by [hotfix]"
```
```hcl
git log --graph --all   # view branch status of all outstanding branches
```
```hcl
git checkout main   # switch back to main branch
```
```hcl
git merge hotfix       # merge hotfix branch to main
```
```

PS C:\Users\yec\OneDrive\dev_cloud\vs_code\_common_iot\14-kubernetes\testgit> git merge hotfix
Updating 8541726..074b542
Fast-forward
 share-file.txt | Bin 72 -> 134 bytes
 1 file changed, 0 insertions(+), 0 deletions(-)


```hcl
git branch -d hotfix       # delete hotfix branch 
```

### Now, let's merge that new-branch into main

```hcl
git branch  # switch back to main, to merge merge new-branch
```
```hcl
echo "test new file" >> test.txt   # add another new file before merge 
```
```hcl
git add test.txt
```
```hcl
git commit -m "add new file"
```
```hcl
git merge new-branch       # merge new-branch
```
```
```hcl
git push origin main        # might as well?
```
```hcl
git branch -d new-branch


## End of this Lab


