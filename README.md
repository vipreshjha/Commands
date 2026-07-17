# Commands
General Commands usefull in daily software development work

Find and Process running on a specific port Unix

    kill -9 `sudo netstat -lnpt | grep -i -n ":3000" | awk -F" " '{print $7}' | awk -F"/" '{print $1}'`


Find Process running on a specific port Windows

    netstat -aon | find /i "listening" | netstat -ano | findstr :4000

Kill process in Windows

    taskkill /PID 26148 /F

Find Process running on a specific port Macbook

    lsof -i tcp:3000
    netstat -vanp tcp | grep 3000
    
Kill process in Macbook
    
    kill -9 <PID>

Start a http server i Python

    python3 -m http.server 8888

Convert between Encodings
    
    iconv -f utf-16le -t utf-8 /mnt/c/Users/20250819120830/data.csv | awk -F',' '$7 ~ /793007/'


# To configure Git SSH keys

On Mac Restart run command to store identity inside ssh agent

Add your specific key

    ssh-add ~/.ssh/id_****** 2>/dev/null

To check if ssh-agent is running or not

    if ! pgrep -u "$USER" ssh-agent > /dev/null; then
        eval $(ssh-agent -s)
    fi

Alternamte method to above

Edit/Create your SSH config file:bash

    nano ~/.ssh/config

Add these lines:

    Host *
    AddKeysToAgent yes
    UseKeychain yes
    IdentityFile ~/.ssh/id_******

Add the key once to the keychain:bash

    ssh-add --apple-use-keychain ~/.ssh/id_******
