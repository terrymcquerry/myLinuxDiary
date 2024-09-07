Directories
==========

`pwd`
`cd`
`ls -ltrh`
`mkdir`
`touch`
`rm`
`cp`
`mv`

Act on terminal
==========

`clear` or press ctrl+l to clear the terminal\
press Q, crtl+c or ctrl+d to exit\
`shutdown`\
`shutdown -P +60` shutdown in an hour\
`shutdown -c` cancel the pending shutdown\
`reboot`\
`sudo su` become root user\

Get info 
==========

`whoami` get username\
`uname -a` get system information\
`history` get a list of previous commands\
`!53` recall and execute the command associated with the history number\
`history -c` delete history\
`uptime`\
`type` get type of command\
`file (fileName)` get file type\
`echo`\
`man`\
`top`/`htop`\
`ping`/`ifconfig`\

Tools
==========

`cat`\
`find`\
`grep`\
`head`\
`tail`\
`nano`/`vim`\
`kill`/`xkill`\
`curl`\
`ssh user@ipaddress`\
`hexedit` edit file in hex mode, f2 to save, ctrl x to exit\
`feh file.jpg` view image files\
`convert file.jpg -resize  30%  file1.jpg` after installing ImageMagick use to convert file size\

`vi`
------------
**vi (name)** *open or edit file*\
**i** *switch to insert mode*\
**ESC** *get back to command mode*\
**:w** *save and get back to writing*\
**ZZ** *save and quit*\
**:q!** *quit without saving*\
**dd** *delete one line*\

`apt`
------------

`apt list --installed`\
`apt purge`\
`apt remove` If you don't want to remove the configuration files\
`apt autoremove`                    remove any unused packages\
`apt clean`                          remove downloaded archive files\
`apt-get update`\
`apt list --upgradable`\
`apt upgrade`\
`apt-get dist-upgrade`

`Git`
--------------

`git config --global init.defaultBranch main`\
`git branch (new-branch)` build a new branch\
`git checkout (branch-name)` change branch (add -b flag to build it at the same time)\
`git branch` list all branches\
`git merge (branch-name)` merges this branch to the current branch\
`git branch -d (branch-name)` delete a branch (mostly after merging)\
`git push origin (branch-name)` push the new branch to the remote repo and afterwards\
