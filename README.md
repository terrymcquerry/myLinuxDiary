Directories
==========

`pwd`\
`cd` changes to home directory\
`cd ..` changes to parent directory\
`cd -` changes to previous working directory\
`ls -ltrh` l for long, t to sort the result by the ﬁle’s modiﬁcation time, r to reverse the order of the sort, and h to make it human readable\
`mkdir` directory... (as many as you want)\
`rm -rf or -ir`\ (tip: check what you want to remove, with ls first)
`cp -u *.html destination`\copy only html ﬁles that do not exist in the destination directory or are newerthan the versions in the destination directory
-i iption for copying asks before overwriting repetetive file names
`cp file1 file2 dir1` Copies file1 and file2 into directory dir1. The directory dir1 must already exist
`cp dir1/* dir2` copies every file in dir1 to dir2
`mv -i file1 file2` Move file1 to file2. If file2 exists, it is overwritten with the contents of file1. If file2 does not exist, it is created. In either case, file1 ceases to exist and prompts you before overwriting if file2 already exists
`mv file... dir` move one or more files to a directory
`touch`\
`ln file link` create hard link
`ln -s item link` creat soft link (item is either a file or a directory)

Act on terminal
==========

`clear` or press ctrl+l to clear the terminal\
press Q, crtl+c or ctrl+d to exit\
`shutdown`\
`shutdown -P +60` shutdown in an hour\
`shutdown -c` cancel the pending shutdown\
`reboot`\
`sudo su` become root user\
`sudo passwd [username]` change password for user\

Get info 
==========
`date` displays the current time and date\
`cal` displays a calendar of the current month\
`whoami` get username\
`whatis command` gives short description\
`info command` gives info\
`uname -a` get system information\
`history` get a list of previous commands\
`!!` get the last command\
`sudo !!` repeat command with privileges\
`!53` recall and execute the command associated with the history number\
`history -c` delete history\
`ctrl+R` search history, hit again for previous command, hit ctrl+g to exit\
`export HISTSIZE=50` change history size to 50\
`history > cmds.txt` save history to a cheatsheet\
`uptime`\
`type` get type of command\
`file (fileName)` get file type\
`echo`\
`man`\
`top`/`htop`\
`ping`/`ifconfig`\
`df` displays the current amount of free space on our disk drives\
`free` displays the amount of free memory\

Tools
==========

`cat`\
`less`\
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
`alias name='string'` name shouldn't be taken (check with type)\
`unalias command`\
`alias` list all aliases\


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
`apt update`\
`apt list --upgradable`\
`apt upgrade`\
`apt dist-upgrade`

`Git`
--------------

`git config --global init.defaultBranch main`\
`git branch (new-branch)` build a new branch\
`git checkout (branch-name)` change branch (add -b flag to build it at the same time)\
`git branch` list all branches\
`git merge (branch-name)` merges this branch to the current branch\
`git branch -d (branch-name)` delete a branch (mostly after merging)\
`git push origin (branch-name)` push the new branch to the remote repo and afterwards\

Intersting stuff
==========
- If you highlight some
text by holding down the left mouse button and dragging the
mouse over it (or double-clicking a word), it is copied into a buffer
maintained by X. Pressing the middle mouse button will cause the
text to be pasted at the cursor location.
- We can end a terminal session by closing the terminal emulator window,
by entering the exit command at the shell prompt, or by pressing CTRL-
D.
press CTRL-SHIFT while dragging a file, to make a symbolic link in GUI.
It’s possible to put more than one command on a line by separating each command with a semicolon.
