
Borg-em Script v0.3
-
Automatic backup helper for 'borg backup'.  Support lvm cron snapshot &amp; multiple soure.
Writte by emeric (kometo@gmail.com)

    Service name:   borg-em.service
    Timer name:     borg-em.timer
    conf file:      /etc/borg-em.conf
    
## Quick install
    
    git clone https://github.com/EmericLee/borg-em.git                  #Clone source to some where
    chmod 700 borg-em.install && ./borg-em.install                      #Install service and timer
    cp borg-em.conf.sample borg-em.conf && vim borg-em.conf             #edit config file as comments
    borg-em list                                                        #show list of achive & check config

## Quick command
    
    sudo systemctl stop|start borg-em.timer   #stop or start timer
    sudo ./borg-em.install uninstall          #undo install 
    borg-em                                   #run backup directly
    borg-em list                              #show list of achive
    vim borg-em.conf                          #edit config anytime
    vim borg-em.timer                         #config timer
    ./borg-em.install                         #reinstall service and timer, update timer conf

