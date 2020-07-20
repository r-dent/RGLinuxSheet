# RGLinuxSheet

Here i will list my most recent used Linux commands. This is whether what i use most or have to google very often.

Find all IP´s in current local network

    ping *.*.*.255
    arp -a

Shutdown system

    sudo shutdown -h now
    #or
    sudo halt

Resume screen

    screen -r

Leave screen in background

    Ctrl+a Ctrl+d
    
Install LATEST version of node

    sudo apt-get install python-software-properties
    sudo add-apt-repository ppa:chris-lea/node.js
    sudo apt-get update
    sudo apt-get install nodejs

Copy public ssh key to server

    ssh-copy-id user@server.tld
    # or
    cat ~/.ssh/id_rsa.pub | ssh user@server.tld "cat >> ~/.ssh/authorized_keys"
    
Find Path of running process (macOS)

    ps aux | grep Xcode 
    
## Filesystem

Find a folder

    find / -name 'httpdocs' -type d
    
Get the size of a folder

    du -chs the/path | grep total // Size of folder
    du -chd 1 the/path // Sizes of subfolders
    
Compress a folder with tar and extract it

    tar czf compressed.tar.gz a/folder/
    tar xvf compressed.tar.gz
    
Serve a Folder via HTTP

    python -m SimpleHTTPServer 8080
    
## Text in files
    
Count lines in a file
    
    wc -l file.txt
    
Find lines containing string (-o for "only matching part of the line)

    less file.txt | grep "string" -o
    
Find occurrences of string in files

    grep -r "string" .
    
Truncate all lines to a length of 80 (using [cut](https://www.geeksforgeeks.org/cut-command-linux-examples/))

    cut -c -80 some-file.txt
    
## GIT

Git - Discard any changes

    git checkout -f
    
Git - Submodule add

    git submodule add https://path.to/submodule.git folder/to/clone/to
    
Git - Update Submodules

    git submodule update --recursive
    git pull --recurse-submodules
    
Fetch submodules if the folders are missing
 
    git submodule update --init
    
Setup custom diff tool
I´m using `ksdiff` which is the CLI interface for [Kaleidoscope](https://www.kaleidoscopeapp.com/).

    git config diff.tool ksdiff
    git config difftool.ksdiff.cmd 'ksdiff $LOCAL $REMOTE'
    git config difftool.prompt false
    
Diff files between `some_branch` and HEAD.

    git difftool some_branch.. -- Filename.ext
    
Set global `.gitignore` file

    git config --global core.excludesfile '~/.gitignore'
