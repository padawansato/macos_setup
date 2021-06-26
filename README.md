# macos_setup


## Homebrew
Only M1 chip

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/padawan_e15/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```


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



## Useful Apps

```

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
brew install jq
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

