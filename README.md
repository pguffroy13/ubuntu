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

## CHROME

```
sudo apt-get -y install xdg-utils
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
sudo rm ./google-chrome-stable_current_amd64.deb
```

## GITHUB 

### SSH-KEY SETUP

- for "ubuntu" repository : 
```shell
ssh -T git@github.com
git remote set-url origin git@github.com:pguffroy13/ubuntu.git
git add -A
git commit -am "Update README.md"
git push
```

### INIT NEW REPOSITORY

```shell
git branch -m main master
git fetch origin
git branch -u origin/master master
git remote set-head origin -a
```

# ALIASES

- Create a file named ``.bash_aliases`` containing :

```shell
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

# ANSIBLE 

``azerty123456``

- Install :

  ```shell
  sudo apt-add-repository ppa:ansible/ansible
  sudo apt update
  sudo apt install ansible 
  ```

- Inventory :

  Example : ``/etc/ansible/hosts``

  ```
  [servers]
  server1 ansible_host=203.0.113.111
  server2 ansible_host=203.0.113.112
  server3 ansible_host=203.0.113.113
  
  [all:vars]
  ansible_python_interpreter=/usr/bin/python3
  ```

- Command :
  
  Examples :

  ```shell
  ansible all -a "df -h" -u root
  ansible servers -a "uptime" -u root
  ansible server1:server2 -m ping -u root
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

