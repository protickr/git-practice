# Staging, committing and pushing changes  

## Tracking and Staging


**show modified flies and newly created files or directory**

> `$ git status`  
> 
> or short status by,  
> `$ git status -s`  


**add files to staging area**
> `$ git add -A`  
or  
> `$ git add --all`  
>
>adds file/folder to staging area from everywhere inside git initialized directory
>
> `$ git add -p`  
> Add to staging area part by part. 


>_add files to staging area from current directory and its subdirectories_ 
> `$ git add .`

>_add modified files only_  
> `$ git add -u`  
or  
> `$ git add --update`  

**improper way to stage**  
> `$ git add *`  
"*" is a shell command, so whatever returned by shell is added to staging area,
it is imprecise and inconsistent across multiple operating system and environments  
so avoid using it.  
> While  
> `$ git add *.txt`  
> adds all files with txt extension to staging area.

**List of files in staging area**  
> `$ git ls-files`

**show changes made**
>`$ git diff`  
> Difference between working directory vs staging.  
> Shows changes that are not staged. Will not show newly added files or untracked files.   
> 
> `$ git diff --staged`  
> Difference between Staged vs last_commit   
> Review staged changes.  
>
>`$ git diff HEAD`  
Shows incoming changes to parent, in this case HEAD, both staged and untracked changes.  
>
> `$ git diff branch_name`  
Changes made to a branch
>
>`$ git diff <file_name>`  
Show changes made to file since previous commit  
> 
>`$ git diff commit_hash_1 commit_hash_2`  
Shows change between commit_1 and commit_2

## Committing to local branch

**Commit staged changes**  
>`$ git commit -m "commit message"`  

**show git commit log**
> `$ git log`  
> `$ git log --stat`    
> `$ git log --graph`  
> `$ git log --all --oneline --decorate --graph`  
> as a tree  

**View a commit**
> `$ git show <commit_hash>`  
> `$ git show <commit_hash:directory/file>`  

## Push commit to remote repo
>first take a pull then push  
>`$ git pull origin branch`  
>`$ git push origin branch`  
>or  
> `$ git pull`  
> `$ git push`  
> if remote upstream branch is already set or set upstream branch first.

[Index][index]

[index]: ../index.md
