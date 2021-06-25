# macos_setup


## Homebrew




### Only M1 chip
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/padawan_e15/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

## Shell

```

```

## Editor
```
brew install --cask visual-studio-code
```

## Useful Apps

```
brew install --cask deepl
brew install --cask shiftit
brew install --cask clipy
```

## Git
```
git --versions
brew install tig
brew install ghq
```

## Useful CLI Tools

```
brew install tree
brew install fzf
```

## Python
```


```


## Rust


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

