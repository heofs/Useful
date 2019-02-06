# Git

## SSH folder setup
git clone git@github.com:UserName/RepoName.git      # Creates a new folder called RepoName

## Branching

git checkout -b branchname      # Starts new branch and open the branch.
OR
git branch branchname           # Start new branch.
git checkout branchname         # Open branch.

git branch                      # List branches.

DO COMMITS TO BRANCH

git checkout master
git merge branchname            # Master is now updated with the new branch.
                                # Master branch now points to same place as branchname.

git branch -d branchname        # Deletes branch.
