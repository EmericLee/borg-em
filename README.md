
Borg-em Script v0.3
-
Automatic backup helper for 'borg backup'.  Support lvm cron snapshot &amp; multiple soure.

Writte by emeric (kometo@gmail.com)

Read more: 基于Borg的Linux 整机备份的单点集群解决方案 http://lee.kometo.com/archives/1253

    Service name:   borg-em.service
    Timer name:     borg-em.timer
    conf file:      /etc/borg-em.conf
    
## Quick install
    
    git clone https://github.com/EmericLee/borg-em.git             #Clone source to some where
    cd borg-em
    chmod 700 borg-em.install && ./borg-em.install                 #Install service and timer
    vim borg-em.conf                                               #Edit the conf file before do anything.
    
    vim borg-em.timer                                              #(optional) edit timer, reinstall atfer edit.
    borg-em                                                        #(optional) Run backup manully first
    borg-em list                                                   #(optional) show list of achive & check repo

## Quick command
    
    systemctl stop|start borg-em.timer        #stop or start timer
    ./borg-em.install                         #reinstall service and timer, update timer conf
    ./borg-em.install uninstall               #undo install 
    borg-em                                   #run backup manully
    borg-em list                              #show list of achive
    vim borg-em.conf                          #edit config anytime
    vim borg-em.timer                         #config timer
    

