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

### 5. Install the version of Node needed
```
nvm install v8.15.1
```

### 6. Install the Angular CLI
```
npm install -g @angular/cli
```

### 7. Create New Application
```
ng new project-name
```

### 8. Run the Application
```
cd project-name
ng serve                             ## (OR)
ng serve – – host 0.0.0.0 – – open   ## (OR)
ng serve -h 0.0.0.0 -o               ## (to run on default port)
ng serve -h 0.0.0.0 -p 3000 -o       ## (to run on user defined port)
```



