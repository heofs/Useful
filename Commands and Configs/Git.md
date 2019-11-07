# Git

## Configurations

### Configure User
- `git config --global user.name "yourname"`
- `git config --global user.email "youremail"`

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

### Rebase on pull

`git config --global pull.rebase true`

### Git branch name on Terminal

Open `~/.bash_profile` and add the following to the end of the file.

```
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

export PS1="\[\e[1;31m\]-------------------------- \w\[\033[32m\]\$(parse_git_branch)\[\e[1;31m\]\n\u -> \[\e[0m\] "
export PS2="| => "
```

## Commands

### Branches

- `git branch -d branchname` - Deletes branch.
- `git checkout master` -> `git merge branchname` - Update master with new branch.
- `git checkout -` - Switch to the previous branch.
- `git checkout -- .` - Switch to master and delete current changes.  

Creating a new branch
- `git checkout -b branchname` - Starts new branch and open the branch.
- `git branch branchname` - Start new branch.

### Rebasing

- `git checkout master`
- `git pull`
- `git checkout yourbranch`
- `git rebase master -i` - Merges your current branch with master.

### Stashing

- `git stash` - Stashes changes.
- `git stash pop` - Brings back the changes.
- `git stash apply` - Brings back changes and keeps stash.

### Ignoring files locally only

Add file to `.git/info/exclude`

then do

`git update-index --skip-worktree ./your-file.yaml`
