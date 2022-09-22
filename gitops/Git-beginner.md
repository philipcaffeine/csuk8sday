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
cd testgitrepo
echo "My first repository." > README.md
git init
git add README.md       # this is the "staging"
git commit -m "initial"      # this commits all staged files only, with a commit message
cd .. # get to where we were

```


### Cloud quickstart

- 6GB unused RAM
- [**Microsoft Azure Cloud** (`azure`)](./rancher/azure)
1. Clone or download this repository to a local folder
