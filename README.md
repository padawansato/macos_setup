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
"iTerm2.app" , turn off rosetta2 chechbox on finder.app

```iterm
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/padawan_e15/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

### Homebrew (Intel)
"Terminal.app" , turn on rosetta2 chechbox on finder.app




## Shell (Fish shell)

```
brew install fish
echo "/usr/local/bin/fish" >> /etc/shells
chsh -s /usr/local/bin/fish 
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


## Useful Apps

```
brew install --cask karabiner-elements
brew install --cask alfred
brew install --cask deepl
brew install --cask shiftit
brew install --cask clipy
```

## Cloud Storage

```
brew install --cask dropbox
```


## Git

```
git --versions
brew install tig
brew install ghq
```

## Useful CLI Tools

```
brew install z
brew install tree
brew install fzf
brew install tmux
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

```
pip3 install pyenv
```

## Rust

