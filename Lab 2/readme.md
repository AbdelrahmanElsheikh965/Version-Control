# Lab 2

## Create a new project on your local machine,then push it your remote repo.
	git init
	touch index.html
	git add .
	git commit -m"first commit"
	git remote add origin https://github.com/AbdelrahmanElsheikh965/Version-Control.git
	git remote -v (to be sure)
	git push origin master

## Create two branches (dev & test) then create one file on each branch, and push this changes to the remote repo.
	git checkout -b dev
	touch dev_file
	git add .
	git commit -m"dev_commit"
	git push origin dev
	git checkout -b test
	touch test_file
	git add .
	git commit -m"test_commit"
	git push origin test
	-> If an error happened because of conflicting of commits ordering
	-> And HEAD pointing position between local and remote, run these 2 commands for rebasing HEAD pointer
	-> git pull --rebase origin master
	-> git push origin master
	
## Merge this changes on Master branch and then push it to your remote master branch.
	git checkout master 
	git merge test
	git merge dev

## Tell me how to remove them locally and remotely.
	locally  => git branch -D dev
	remotely => git push origin --delete dev

## Create an annotated tag with tagname (v1.7).
	git tag (to view all avilable tags)
	git tag -a 1.7 -m "First Stable Tag"
## Push it to the remote repository.
	git push origin --tags
	
## Tell me how to list tags.
	git tag
## Tell me how to delete tag locally and remotely.
	locally  => git tag -d v2.5
	remotely => git push origin --delete v2.5
	
	
	
