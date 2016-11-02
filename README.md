RGLinuxSheet
============

Here i will list my most recent used Ubuntu commands. This is whether what i use most or have to google very often.

Find all IP´s in current local network

    ping *.*.*.255
    arp -a

Find a folder

    find / -name 'httpdocs' -type d
    
Get the size of a folder

    du -ch the/path | grep total

Shutdown system

    sudo shutdown -h now
    #or
    sudo halt

Git - Discard any changes

    git checkout -f
    
Git - Submodule add

    git submodule add https://path.to/submodule.git folder/to/clone/to
    
Git - Update Submodules

    git submodule update --recursive
    git pull --recurse-submodules

Resume screen

    screen -r

Leave screen in background

    Ctrl+a Ctrl+d
    
Fetch submodules if the folders are missing
 
    git submodule update --init
    
Install LATEST version of node

    sudo apt-get install python-software-properties
    sudo add-apt-repository ppa:chris-lea/node.js
    sudo apt-get update
    sudo apt-get install nodejs
    
Compress a folder with tar and extract it

    tar czf compressed.tar.gz a/folder/
    tar xvf compressed.tar.gz

Copy public ssh key to server

    ssh-copy-id user@server.tld
    # or
    cat ~/.ssh/id_rsa.pub | ssh user@server.tld "cat >> ~/.ssh/authorized_keys"
    
Count lines in a file
    
    wc -l file.txt
    
Find lines containing string

    less file.txt | grep "string"
    
Find Path of running process (macOS)

    ps aux | grep Xcode 
