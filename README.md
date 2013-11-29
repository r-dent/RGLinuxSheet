RGLinuxSheet
============

Here i will list my most recent used Ubuntu commands. This is whether what i use most or have to google very often.

Find all IP´s in current local network

    ping *.*.*.255
    arp -a

Find a folder

    find / -name 'httpdocs' -type d

Shutdown system

    sudo shutdown -h now

GIT Discard any changes

    git checkout -f

Resume screen

    screen -r

Leave screen in background

    Ctrl+a Ctrl+d
    
Clear DNS Cache [MAC OS]

    dscacheutil -flushcache
    
Git Submodule add

    git submodule add https://path.to/submodule.git folder/to/clone/to
    
Fetch submodules if the folders are missing

    git submodule init 
    git submodule update
    
Install LATEST version of node

    sudo apt-get install python-software-properties
    sudo add-apt-repository ppa:chris-lea/node.js
    sudo apt-get update
    sudo apt-get install nodejs
    
Compress a folder with tar and extract it

    tar czf compressed.tar.gz a/folder/
    tar xvf compressed.tar.gz

Copy public ssh key to server

    cat ~/.ssh/id_rsa.pub | ssh user@server.tld "cat >> ~/.ssh/authorized_keys"
