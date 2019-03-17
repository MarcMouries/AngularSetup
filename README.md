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
ng serve -o                          ## to run on default port and open the app (OR)
ng serve --host 0.0.0.0              ## to allow access outside of localhost
                                     ## to allow  to connect to the ng serve using your ip instead of localhost.
ng serve -h 0.0.0.0 -p 3000 -o       ## (to run on user defined port)
```


### 9. Move the node_modules directory outside the Application
The node_modules directory contains tens of megabytes of tiny files which take forever to sync with tools like Box, Dropbox or OneDrive, 
We'll move it out of the project directory and use a symbolic lync to prevent it from syncing 
The sync tools won’t recognize and sync this symlink, whereas Node.js will work with it as intended
Avoid synchronizing node_modules directories while keeping the projects in OneDrive
```
cd ..
mkdir node_dependencies                 # this will contains all the node_modules directories
mv project-name/node_modules node_dependencies/project-name_node_modules/
cd project-name
## ln -s /path/to/original /path/to/link
ln -s ../node_dependencies/project-name_node_modules node_modules
## run install to reset the paths
npm install
## run the project
ng serve -o 
```



