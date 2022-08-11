# 02. Install Node.JS

## 3 ways to install node

1. directly on your machine
2. on a vm
3. in docker

Since 95%+ of servers (which are needed by web apps to deliever HTML pages) run on linux, it would be wise to develop node apps on linux, a linux vm, or docker to avoid compatibility issues, especially concerning the file system.

## installing modules globally

NPM allows you to install modules globally but it isn't safe to allow someone else's code to have free reign on your system.

To mitigate potential security problems is create a new directory to store global modules and configure npm

```
mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
```

Now when npm installs a module globally, send them to this new directory by editing bashrc

```
nano ~/.bashrc
```

now that it is open, add these two lines at the end of the file

```
export NPM_GLOBAL="$HOME/.npm-global"
export PATH="$NPM_GLOBAL/bin:$PATH"
```

Restart the bash terminal with `source ~/.bashrc`

Now you can install global modules safely without sudo starting with npm itself for auto updates

`npm install npm --global`
