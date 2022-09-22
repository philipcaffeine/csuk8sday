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
mkdir testgitrepo
```
```hcl
cd testgitrepo
```
```hcl
echo "# testgitrepo" >> README.md  # create initial file 
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
git remote add origin https://github.com/philipcaffeine/testgitrepo.git
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

```hcl
git branch # see, we're in master now

git checkout -b new-branch

git branch

echo "Editing by author of [new-branch]" >> share-file.txt

git commit -a -m "Commit change on a dev new-branch"

git checkout master # go back to master


git checkout -b hotfix

echo "Editing by author of [hotfix]" >> share-file.txt

git commit -a -m "Commit change by [hotfix]"


git log --graph --all

git checkout master

git merge hotfix

Updating f42c576..3a0874c
Fast-forward
 index.html | 2 ++
 1 file changed, 2 insertions(+)


```

Now, let's merge that new-branch into master:

git branch # make sure you're in the branch you want to merge the other into. git merge new-branch

cat test.txt

git add test.txt

git commit -m "merge conflict resolved"

git push origin master # might as well?


## Cloud quickstart

- 6GB unused RAM
- [**Microsoft Azure Cloud** (`azure`)](./rancher/azure)
1. Clone or download this repository to a local folder
