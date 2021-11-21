# Dotfiles WSL2

## Setup dotfiles in a new computer
- Clone github repo
```shell
git clone --bare git@github.com:OscarAguilarL/dotfiles-wsl2.git $HOME/.dotfiles
```

- Define the alias in the current scope
```shell
alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
```

- checkout the actual content from the git repository to your $HOME
```shell
dotfiles checkout
```
> Note that if you already have some of the files you'll get an error message. You can either (1) delete them or (2) back them up somewhere else. It's up to you.Note that if you already have some of the files you'll get an error message. You can either (1) delete them or (2) back them up somewhere else. It's up to you.


## Installing ZSH

Installing zsh
```bash
# zsh
sudo apt install zsh

# oh my zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Install PowerLevel10k

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
**Skip setup wizard**