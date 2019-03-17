# Setup Angular on MacOS

A step by step guide to get an Angular development env running

### 1. Install HomeBrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### 2. Install NVM
```
brew install nvm
```
### 3. Create NVM directory
```
mkdir ~/.nvm
```

### 4. Add NVM directory to bash_profile
```
~/.bash_profile 
export NVM_DIR=”$HOME/.nvm”
```
