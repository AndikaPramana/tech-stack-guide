# Git Syntax 

## Config 
1. Set the name of account 
	- `git config --global user.name "{name}"`
2. Set the email of account
	- `git config --global user.email "{email}"`

## Basic
1. Starting git in any directory
	- `git init`
2. Clone a repository 
	- `git clone {link of remote repo}`
3. See git list of all commit 
	- `git log`
4. See any change, committed or modified files
	- `git status`
5. Discard all local change 
	- `git reset --hard`
6. Discard all local change but still preserving the change
	- `git reset`

## Pull, commit and push
1. fetch changes in remote branch
	- `git fetch`
2. pull all changes from remote branch
	- `git pull origin {branch_name}`
	or
	- `git pull`
3. Add files to commit
	- `git add .`	==> to add all files 
	- `git add {file_name}` ==> to add specific files
4. Commit in Git
	- `git commit -m "name of your commit"`
5. Commit all tracked files automatically
	- `git commit -a -m "name of commit"` ==> no need to use `git add` anymore
6. Pushing a commit to remote branch
	- `git push origin {branch_name}`

## Git tag
1. Create a tag
	- `git tag {tag_name}`
2. push all tags to origin 
	- `git push --tags`
3. push specific tag to origin 
	- `git push origin {tag_name}`

## Git Branch
1. Show all remote and local branch
	- `git branch -a`
2. Show remote branch only 
	- `git branch`
	or
	- `git branch -r`
3. Checkout local branch 
	- `git checkout {branch_name}`
4. Checkout branch which not yet in local but exist in remote
	- `git checkout origin {branch_name}`
5. Create new branch localy and checkout to that branch
	- `git checkout -b {branch_name}`
6. Delete a branch
	- `git branch -d {branch name}`

## Merging a branch
1. 	Merge branch a to branch b
	- `git checkout {name of branch a}`
	- `git merge {name of branch b}`
	
	- OR
	- `git merge {a}/{b} `
	- Note: Merging branch a to b is different than merging branch b to a

## Setting Remote URL
1. see which remote branch this git refer to
	- `git remote -v`
2. Link git repository to different remote branch
	- `git remote set-url origin {new_remote_url}`

## Git Stash 
1. Store modified files temporarily
	- `git stash`
2. Restore modified files
	- `git stash pop`
3. List all stash
	- `git stash list`

## Advanced Git Command
1. Clone all remote branch to local
	- `touch getallbranch.sh`
	- `vim getallbranch.sh`
	- paste the following command
	
	```
	for branch in `git branch -a | grep remotes | grep -v HEAD | grep -v master `; do
   	git branch --track ${branch#remotes/origin/} $branch
	done
	```
	- `chmod +x getAllBranches.sh`    
	- `sh getAllBranches.sh`

