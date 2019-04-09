# Git

## SSH folder setup
* ```git clone git@github.com:UserName/RepoName.git``` - Clones down the repository to folder.

## Branches

* ```git branch```  - List branches.
* ```git branch -d branchname```  - Deletes branch.
* ```git checkout master``` ```git merge branchname``` - Update master with new branch

### Create a new branch
* ```git checkout -b branchname```  - Starts new branch and open the branch.
OR
* ```git branch branchname``` - Start new branch.
* ```git checkout branchname``` - Open branch.

## GPG Signing
Enabling GPG signing of commits

* `gpg --gen-key` - Generate a new GPG key.
* `gpg --list-secret-keys --keyid-format LONG`- List all gpg keys.
* `gpg --armor --export B251A5023921838` - Exports the public key. Add this to GitHub.
* `git config --global user.signingkey B251A5023921838` - Specifiy which key to use.
* `git config --global commit.gpgsign true`- Enable signing for any local repo on computer.

Signing old commits
1. `git rebase -i master` - Opens up rebase.
2. Add `exec git commit --amend --no-edit -S` on a new line after each commit.
3. `git push -f` - Force a push to the repo.
