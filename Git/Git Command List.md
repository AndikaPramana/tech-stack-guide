# Github Syntax 

## basic
1. Starting git in any directory
	- `git init`
2. Checkout local branch 
	- `git checkout {branch_name}`
3. Checkout branch which not yet in local but exist in remote
	- `git checkout origin {branch_name}`
4. Create new branch localy and checkout to that branch
	- `git checkout -b {branch_name}`
5. see which remote branch this git refer to
	- `git remote -v`
6. Link git repository to different remote branch
	- `git remote set-url origin {new_remote_url}`
7. See git list of all commit 
	- `git log`
8. Show all remote and local branch
	- `git branch -a`
9. Show remote only in local
	- `git branch`
10. Discard all local change 
	- `git reset --hard`
11. fetch changes in remote branch
	- `git fetch`
12. pull all changes from remote branch
	- `git pull origin {branch_name}`
13. Commit in Git
	- `git commit -m "name of your commit"`
14. Add files to commit
	- `git add .`	==> to add all files 
	- `git add {file_name}` ==> to add specific files
15. Clone all remote branch to local
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
16. Store modified files temporarily
	- `git stash`
17. Restore modified files
	- `git stash pop`
18. List all stash
	- `git stash list`
