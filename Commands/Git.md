# Git

## Basic commands

- `git clone git@github.com:UserName/RepoName.git` - Clones down the repository to current folder.
- `git pull` - Pulls remote repo down to working directory.
- `git fetch` - Fetches remote repo down to local repo.

## Branches

- `git branch` - List branches.
- `git branch -d branchname` - Deletes branch.
- `git checkout master` `git merge branchname` - Update master with new branch
- `git checkout -` - Switch to the last used branch.
- `git checkout -- .` - Switch to master and delete current changes.

### Create a new branch

- `git checkout -b branchname` - Starts new branch and open the branch.
  OR
- `git branch branchname` - Start new branch.
- `git checkout branchname` - Open branch.

## Rebasing

- `git checkout master`
- `git pull`
- `git rebase master` - Merges your current branch with master.

## Stashing

- `git stash` - Stashes changes.
- `git stash pop` - Brings back the changes.

## Extras

### Add SSH Key

- `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
- `eval "$(ssh-agent -s)"`
- `ssh-add ~/.ssh/id_rsa`
- `cat ~/.ssh/id_rsa.pub` copy to clipboard.
- Add key to SSH in <https://github.com/settings/keys>.


### GPG Signing

Enabling GPG signing of commits

- `gpg --full-generate-key` - Generate a new GPG key.
- `gpg --list-secret-keys --keyid-format LONG`- List all gpg keys, use the top sec key.
- `gpg --armor --export B251A5023921838` - Exports the public key. Add this to GitHub.
- `git config --global user.signingkey B251A5023921838` - Specifiy which key to use.
- `git config --global commit.gpgsign true`- Enable signing for any local repo on computer.

### Signing old commits

1. `git rebase -i master` - Opens up rebase.
2. Add `exec git commit --amend --no-edit -S` on a new line after each commit.
3. `git push -f` - Force a push to the repo.

### Change default git editor to VS Code

1. Open gitconfig using `vim ~/.gitconfig`
2. Add the following at the end:

```
[core]
    # Use custom `.gitignore` and `.gitattributes`
    excludesfile = ~/.gitignore
    attributesfile = ~/.gitattributes
    editor = code --wait
```

3. Open VS Code command palette (`CMD + Shift + P`) and run `Shell Command: Install 'code' command in PATH`
