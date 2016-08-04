# Flows

## Init
* Create develop branch if not exists
* List all current (non master or develop) branches and say that maybe are following git flow
* Ask for feature,hot fix and release prefix
* Ask for tag format and message format
* Ask for remote name???
* Save all in dotfile

## New feature flow
* Move to develop if not there
* Ask if use prefix?
* Ask branch name
* Create branch
* Move to feature branch

### Close feature branch
* Check for un-commited changes and fails
* Move to develop
* Merge feature branch into develop with —no-ff
* Ask to delete feature branch 
* Ask to push to remote


## New release flow
* Move to develop if not there
* Ask version
* Create branch
* Move to release branch

### Close release branch
* Check for un-commited changes and fails
* Ask for branch destination (develop or master)
* Merge release branch with —no-ff
* Tag changes
* If the branch was master
	* Checkout develop
	* Merge release branch with —no-ff
* Ask to delete feature branch 
* Ask to push to remote

## New hot fix flow
* Move to master if not there
* Ask if use prefix?
* Ask branch name
* Create branch
* Move to hot fix branch

### Close hotfix branch
* Check for un-commited changes and fails
* Go to master
* Merge hot fix branch with —no-ff
* Ask version
* Tag changes
* Checkout develop
* Merge release branch with —no-ff
* Ask to delete feature branch 
* Ask to push to remote