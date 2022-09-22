# Quickstart examples for Git beginner 

Quick sample for beginners of Git for version control.

1. Create a git repository, both from a directory and from cloning. Add and commit files.
2. Working with remotes.
3. Branch and merge.

Intended for experimentation/evaluation ONLY.

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

In your command line, or terminal in VS Code, do the following: 

```hcl
mkdir testgitrepo
```
```hcl
cd testgitrepo
```
```hcl
echo "# testgitrepo" >> README.md
```
```hcl
git init
```
```hcl
git add README.md
```
```hcl
git commit -m "first commit"
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

## Connect to GitHub

Connect it to github

git remote add origin philipcaffeine@github.com:philipcaffeine/testgitrepo
git push -u origin master

## Clone existing repo 


```hcl
git clone https://
git log
```

## Cloud quickstart

- 6GB unused RAM
- [**Microsoft Azure Cloud** (`azure`)](./rancher/azure)
1. Clone or download this repository to a local folder
