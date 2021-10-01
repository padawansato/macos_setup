# macos_setup

## Rosetta2

```
softwareupdate --install-rosetta
```

## Check arm64(m1) or x86_64(intel)

```
uname -m

```

## Homebrew

### Homebrew (arm)
Do not check the "Turn on rosetta2" checkbox of "iTerm2" in Finder application.


```iterm
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/padawan_e15/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

### Homebrew (Intel)
"Terminal.app" , turn on rosetta2 chechbox on finder.app




## Shell (Fish shell)
https://github.com/jorgebucaran/awsm.fish

```
brew install fish
echo "/usr/local/bin/fish" >> /etc/shells
chsh -s /usr/local/bin/fish 
```


### Fishshel plugin manager(fisher)
```
curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher
```

### fish shell plugin
```
fisher install jethrokuan/z
fisher install PatrickF1/fzf.fish
fisher install decors/fish-ghq
fisher install jorgebucaran/replay.fish
fisher install IlanCosman/tide@v5
fisher install franciscolourenco/done

```


### Show which one uesed in prompot 

`~/.config/fish/functions/fish_prompt.fish`
```
echo -n "("(uname -m|sed "s/\r//")")"
```


## Terminal

```
brew install --cask iterm2
```


## Editor
```
brew install --cask visual-studio-code
brew install --cask google-japanese-ime
```

## Docker

[Docker Desktop for Apple silicon](https://matsuand.github.io/docs.docker.jp.onthefly/docker-for-mac/apple-silicon/)


### window manager
to use desktop app in docker container

```
brew install --cask xquartz
```


## Useful Apps

```
brew install --cask karabiner-elements
brew install --cask alfred
brew install --cask deepl
brew install --cask grammarly
brew install --cask shiftit
brew install --cask clipy
brew install --cask appcleaner
brew install --cask cheatsheet
brew install --cask keyboardcleantool
```

## Cloud Storage

```
brew install --cask dropbox
```

## Web Browser

```
brew install --cask vivaldi
```

## Git

```
git config --global user.name "First-name Family-name"
git config --global user.email "username@example.com"
```

```
git --versions
brew install tig
brew install ghq
```
### Git CLI

```
brew install gh
gh auth login
gh config set editor vim
```
create remote repository with local CLI

```
git init 
gh repo create --private[or --public]
```




### gitignore
global
```
touch ~/.config/git/ignore
touch ~/.config/git/[some].gitignore
git config --global --add core.excludesfile ~/.config/git/[some].gitignore
```

[official gitignore samples](https://github.com/github/gitignore/tree/master/Global)



## Useful CLI Tools

```
brew install z
brew install tree
brew install fzf fd bat ripgrep
brew install tmux
```


## Useful apps for Productivity

```
https://todoist.com/ja/downloads/mac
```



## Finder settings

```
defaults write com.apple.finder _FXShowPosixPathInTitle -boolean true
defaults write com.apple.finder AppleShowAllFiles -bool true
killall Finder
```

## Boot sounds

```
sudo nvram SystemAudioVolume=%00
```

## Python

brew install is not working.

```
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```

> For Fish shell:
> Execute this interactively:

```
set -Ux PYENV_ROOT $HOME/.pyenv
set -U fish_user_paths $PYENV_ROOT/bin $fish_user_paths
```

> And add this to ~/.config/fish/config.fish:

```
status is-interactive; and pyenv init --path | source
```

### venv
```
pyenv install [version]
pyenv global [version]
python -m venv "venv_py[version]"
alias venv-up "fish -C 'source venv_py*/bin/activate.fish'"
```


## Rust
https://blog.rust-lang.org/2020/11/27/Rustup-1.23.0.html
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
set -U fish_user_paths $fish_user_paths $HOME/.cargo/bin
```


