# Git

***

# What is Git?

Git is world popular version control system which help us to **Track History** and **Work Together**.

***

# Three states of Git

Git has three main states that your files can reside in : *modified*, *staged*, and *committed*.

- **Modified** : You have changed the file but have not committed it to your database yet.
- **Staged** : You have marked a modified file in its current version to go into your next commit snapshot.
- **Committed** : The data is safely stored in your local database.

This lead us to the three main section of a Git project : *the working tree*, *the staging area*, and *the Git
directory*.

- **Working tree** : Single checkout of one version of the project. Files are pulled out of the compressed database in
  the Git directory.
- **Staging area** : A file, generally contained in your Git directory, that stores information about what will go into
  your next commit. Also known as "index".
- **Git directory** : Where Git stores the metadata and object database for our project.

![](https://git-scm.com/book/en/v2/images/areas.png)

***

# Basic usage of Git

## 1. Getting a Git repository

### 1.1 Initializing a Repository in an existing directory

```
git init
```

### 1.2 Cloning an existing repository

```
git clone https://github.com/tkaenvlcl/TIL.git
```

## 2. Recording changes to the repository

### 2.1 Life cycle of the status of files

![](https://git-scm.com/book/en/v2/images/lifecycle.png)

### 2.2 Checking the status of files

```
git status
```

### 2.3 Tracking new files

```
git add filename
```

### 2.4 Staging modified files

```
git add filename // same as 2.3
```

### 2.5 Short status

```
git status -s
```

**??** : New files that aren't tracked  
**M** : Modified files  
**A** : New files that have been added to the staging area

There are two columns to output  
`Left-hand column`  status of ***the staging area***  
`Right-hand column`  status of ***the working tree***

### 2.6 Ignoring files

Example of .gitignore file

```
# ignore all .a files
*.a

# ignore all .o and .a files
*.[oa]

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in any directory named build
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
```

### 2.7 Viewing staged and unstaged changes

```
# Campare between working directory and staging area
git diff

# Compare between staging area and git directory
git diff --staged
```

### 2.8 Committing changes

```
git commit
```

To type commit message inline

```
git commit -m "commit message"
```

### 2.9 Skipping the staging area

To commit directly from working directory

```
git commit -a
```

### 2.10 Removing files

```
git rm filename

# Remove all files that have the .log in the log/ directory
git rm log/\*.log

# Remove all files whose names end with ~
git rm \*~

the backslash (\) in front of the * is necessary because Git does its own filename
expansion in addition to your shell’s filename expansion
```

To keep the file in working tree but remove it from staging area

```
git rm --cached
```

### 2.11 Renaming(Moving) files

```
git mv file_from file_to
```

### 2.12 Viewing the commit history

```
git log

# Show the differences in each commit
git log -p

# Show only the last two entries
git log -2

# Show how many files were changed and how many lines were added or removed
git log --stat

# Limit log output
git log --after
git log --before
```

### 2.13 Redoing the commit

```
git commit --amend

# Usage
git commit -m 'Inital commit'
git add forgotten_file
git commit --amend
```

### 2.14 Unstaging a staged file

```
git restore --staged filename
```

### 2.15 Unmodifying a modified file

```
git restore filename
```

***

## 3. Remotes

### 3.1 Showing remotes

```
git remote b  

# Show URLs
git remote -v
```

### 3.2 Adding remote repositories

```
git remote add [shortname] [url]
```

If we clone something, shortname shall be 'Origin' automatically.

### 3.3 Fetching and pulling from remotes

```
# Download data to local but no merge
git fetch [remote-name]

# Download data and merge automatically
git pull [remote-name]
```

### 3.4 Pushing to remotes

```
git push [remote-name] [branch-name]
```

### 3.5 Inspecting a remote

```
git remote show [remote-name]
```

### 3.6 Renaming and removing remotes

```
#rename
git remote rename [As-is] [To-be]

#remove
git remote remove [remote-name]
```

***

## 4. Tagging

### 4.1 Listing tags

```
git tag
```

### 4.2 Creating tags

```
# Annoted tags
git tag -a [tag]
git tag -a [tag] -m [message]

# Lightweight tags
git tag -a [tag]
```

### 4.3 Tagging later

```
git tag -a [tag] [All or part of checksum]
```

### 4.4 Sharing tags

```
git push origin [tag-name]

# Push up all tags
git push origin --tags
```

### 4.5 Deleting tags

```
# Delete tag on local repository
git tag -d [tag-name]

# Delete tag from remote server
git push origin --delete [tag-name]
```

***

## 5. Aliases

```
# git ci instead of git commit
git config --global alias.ci commit

# git unstage [filename] instead of git reset HEAD -- [filename]
git config --global alias.unstage 'reset HEAD --'

# git last instead of git log -1 HEAD
git config --global alias.last 'log -1 HEAD'

```

***