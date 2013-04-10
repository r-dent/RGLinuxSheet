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
