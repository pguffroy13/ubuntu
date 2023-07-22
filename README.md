# INSTALLATION 
- sudo apt install gnome-text-editor -y
- sudo apt install gimp -y
  ```
  gimp
  ```
- sudo apt install nautilus -y
  ```
  nautilus
  ```
- sudo apt install x11-apps -y

# ALIASES

- Create a file named ``.bash_aliases`` containing :
```
export PS1="\[\e[31m\][\[\e[m\]\[\e[38;5;172m\]\u\[\e[m\]@\[\e[38;5;153m\]\h\[\e[m\] \[\e[38;5;214m\]\W\[\e[m\]\[\e[31m\]]\[\e[m\]\\$ "

cat<<'EOF'
           _..._
         .'     '.
        /  _   _  \
        | (o)_(o) |
         \(     ) /
         //'._.'\ \
        //   .   \ \
       ||   .     \ \
       |\   :     / |
       \ `) '   (`  /_
     _)``".____,.'"` (_
     )     )'--'(     (
      '---`      `---`
EOF

alias update='sudo -- sh -c "apt update && apt -y upgrade && apt -y --purge autoremove && sudo apt -y clean"'
alias dev='cd dev'
```


# HOWTO WEB-SERVER

- sudo apt-get install nodejs
- sudo apt-get install npm
- npm install

- vi package.json
  ```json
  {
    "name": "Demo",
    "version": "1.0.0",
    "description": "demo project.",
    "scripts": {
      "lite": "lite-server --port 10001",
      "start": "npm run lite"
      },
    "author": "",
    "license": "ISC",
    "devDependencies": {
      "lite-server": "^1.3.1"
      }
  }
  ```

- npm start 

