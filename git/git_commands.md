# Table of contents

1. [create-new-repository](#create-new-repository)
2. [push-an-existing-repository](#push-an-existing-repository)
3. [push-local-branch-to-repository-branch](#push-local-branch-to-repository-branch)
4. [merge-former-version-with-current-version-code](#merge-former-version-with-current-version-code)
5. [delete-a-git-branch-both-locally-and-remotely](#delete-a-git-branch-both-locally-and-remotely)
6. [git-reset](#git-reset)
7. [change-remote-git-repository](#change-remote-git-repository)
8. [switch-to-another-branch/keep-the-changes](#switch-to-another-branch/keep-the-changes)
9. [rename-branch-name](#rename-branch-name)
10. [create a tag](#create-a-tag)
11. [cherry-pick-usage](#cherry-pick-usage)
12. [delete-commit](#delete-commit)
13. [merge develop to master](#merge-branch-develop-to-master-on-gitbhub)
14. [git bug solving](#git-bug-solving)


# create-new-repository
echo "# doc_summary" >> README.md

`$ git init`

`$ git add README.md`

`$ git commit -m "first commit"`

`$ git branch -M main`

`$ git remote add origin https://github.com/<your_username>/<repository_name>.git` 

`$ git push -u origin main`

# push-an-existing-repository

add your files to your repository`$ git add requirements.txt main.py .gitignore`

`$ git commit -m"first commit"`

or open your github, login your profile, and create a new repository called <your repository name-practice>. create an empty repository without a README or license file,once you created the repository, return to the command line and push your local files to github

`$ git remote add origin https://github.com/<your_username>/<repository_name>.git `

rename the default branch main, to match what github expects: 

`$ git branch -M main` (rename branch)

`$ git push -u origin main`(push your main branch to github`s main branch) 

# push-local-branch-to-repository-branch

- before you push you local branch you need to pull the latest code from the repository 

`cd pii_us_api(your project)` 

`git checkout -b dev(branchname) ` 

`git add ./git add filename.py` 

`git status` (check the file status) 

`git reset HEAD <your_file_name>`(to undo a git add eg:git reset HEAD .idea) 

`git commit -m"your comments on this push"` 

`git push origin dev`

# merge-former-version-with-current-version-code

- after git commit use 

`git rebase -i HEAD~2`(# handle twice update currently)

  insert module:replace pick with squash

  then quit with :wq(twice)

`git log`(check the log)

`git push origin branch_name`(if error occurs,you can change to the following code)

`git push origin branch_name -f` (-f means force，please be cautious when handling)
  
- if you do close pull request, and want to push you modify code again, in this situation you must use `git rebase`

# delete-a-git-branch-both-locally-and-remotely

- delete a git branch locally

  `$ git branch -D your_branch_name`(implement this command you need to switch to master)


# git-reset


# change-remote-git-repository

- list your existing remote repositories

  `$ git remote -v`
- Change a remote Git repository

  `$ git remote set-url origin https://github.com/<your_username>/<repository_name>.git `
- remove current remote repositories

  `$ git remote remove origin`

- add a remote repository

  `$ git remote add origin https://github.com/<your username>/<repository name>.git`


- then check the remote repository list


# switch-to-another-branch/keep-the-changes

- `git stash`(remember the stash note)

- `git stash list`(check the list you stashed and pick the right {number} you want to get back)
  
- 'git stash apply stash@{number}'

# rename-branch-name

- git branch -m [oldBranchName] [newBranchName]

# create-a-tag

- git create tag
  
  - The tag should be created in the master branch(very important)
  
   git checkout master
   
  - create the tag
  
  git tag release-jp-fix-v1 -m "The release of the fix for jp"
   
  - push the tag to origin registry
  
  git push origin release-jp-fix-v1

- git checkout tags/[tag_name] -b [branchname]
   
   first git pull(pull the tag code)
  
  `git checkout tags/release-jp-fix-v2 -b release-jp-fix-v2-branch`


# cherry-pick-usage

- git checkout develop

- git pull

- git checkout -b dev/branch_name

- git cherry-pick [hash value]  (corresponding to the commit hash value in Github)

- git add . (if there are conflicts, using below)

- git cherry-pick -- continue

if you want to merge specific branch to master branch

- git checkout master and git pull 

- git branch -b merge-PD-1125

- git cherry-pick commit id(corresponding to the commit which you want to merge to master)

- if it faild, you could use git cherry-pick -m i commit id

- git log 

- git push origin merge-PD-1125

- 


# delete-commit

- git log(get your commit id the former id of your wrong commit)

- git rebase -i commit-id

- substitute pick with drop, then ESC->:wq

- git log (check whether you have deleted the commit)


# merge-branch-develop-to-master-on-gitbhub

- find the branches on home page

- click branches, while bechind the branch there is a 'New pull request' click here

- you could choose which two branches you want to merge

# error: You have not concluded your merge (MERGE_HEAD exists)

- $:git merge --abort
  
- $:git reset --merge
  
- $:git pull

# git-bug-solving
- problem description
  
   remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
   remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
   fatal: unable to access 'https://github.com/<user name>/<repo name>/': The requested URL returned error: 403
  
- solution

  git remote remove origin(remove your current repository)

  git remote add origin git remote add origin https://<personal access token>@github.com/<user name>/<repo name>.git








  

