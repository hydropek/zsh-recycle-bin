# zsh-recycle-bin

A recycle bin runned in command line

## install

### oh-my-zsh

1. clone the repo
```
git clone https://github.com/ycpedef/zsh-recycle-bin.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-recycle-bin
```

2. activate the plugin in ~/.zshrc:

```
plugins=( [plugins...] zsh-recycle-bin)
```

### zsh
```
git clone https://github.com/ycpedef/zsh-recycle-bin.git
echo "source ${(q-)PWD}/zsh-recycle-bin/zsh-recycle-bin.plugin.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
```

### bash
```
git clone https://github.com/ycpedef/zsh-recycle-bin.git
echo "source $(pwd)/zsh-recycle-bin/zsh-recycle-bin.plugin.zsh" >> $HOME/.bashrc
```

## usage

```bash
$ delete [file]
$ delete -s [file]           # delete in slient mode
$ recover                    # recover latest file
$ recover [file]             # recover specific file

# also can use del as delete, rec as recover

$ trash list                 # display trashname in recycle bin
$ trash clear                # real remove trash which is not created today
$ trash clear [trashname]    # real remove trash [trashname]
$ trash content              # display details of files in recyble bin
$ trash content [trashname]  # display details of [trashname] 
```

**suggested to add in ~/.bashrc or ~/.zshrc:**

```bash
alias rm="delete -s"
```

## demo

![demo.jpg](demo.jpg)
