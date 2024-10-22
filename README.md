Directories
==========

`pwd` print working directory\
`cd` changes to home directory\
`cd ..` changes to parent directory\
`cd -` changes to previous working directory\
`ls -ltrh` l for long, t to sort the result by the ﬁle’s modiﬁcation time, r to reverse the order of the sort, and h to make it human readable\
`ls -l $(which cp)` get list of a program without knowing it's full pathname\
`mkdir` directory... (as many as you want)(we can use brace expansions too like this: `mkdir {2007..2009}-{01..12}`)\
`rm -rf or -ir`\ (tip: check what you want to remove, with ls first)
`cp -u *.html destination` copy only html ﬁles that do not exist in the destination directory or are newerthan the versions in the destination directory\
-i iption for copying asks before overwriting repetetive file names\
`cp file1 file2 dir1` Copies file1 and file2 into directory dir1. The directory dir1 must already exist\
`cp dir1/* dir2` copies every file in dir1 to dir2\
`mv -i file1 file2` Move file1 to file2. If file2 exists, it is overwritten with the contents of file1. If file2 does not exist, it is created. In either case, file1 ceases to exist and prompts you before overwriting if file2 already exists\
`mv file... dir` move one or more files to a directory\
`touch`\
`ln file link` create hard link\
`ln -s item link` creat soft link (item is either a file or a directory)\

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
`cmd1; cmd2` run the first command, then run the second one\
`cmd1 && cmd2` Run cmd2 if cmd1 is successful\
`cmd1 || cmd2` Run cmd2 if cmd1 is not successful\

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
`sudo !!` run previous command with privileges\
`!abc:p` print the last command starting with abc\
`ctrl + R` search easier\
`!53` recall and execute the command associated with the history number\
`history -c` delete history\
To start incremental search, press CTRL-R followed by the text you are looking for. When you ﬁnd it, you can either press ENTER to execute the command or press CTRL-J to copy the line from the history list to the current command line. To ﬁnd the next occurrence of the text (moving “up” the history list), press CTRL-R again. To quit searching, press either CTRL-G or CTRL-C.\
`export HISTSIZE=50` change history size to 50\
`history > cmds.txt` save history to a cheatsheet\
`uptime`\
`type` get type of command\
`file (fileName)` get file type\
`echo`\ (for example echo [[:upper:]]* (it expands and echos list of files starting with uppercase))
Also can be used as a claculator: $((mathematical expression))
Parameter expansion (echo $USER)\
Or command substitution: echo `$(ls)`\
`man`\
`top`/`htop`\
`ping`/`ifconfig`\
`df` displays the current amount of free space on our disk drives\
`free` displays the amount of free memory\
`printenv` prints a list of available variables\

Tools
==========

`cat` displays text file\
`cat movie.mpeg.0* > movie.mpeg` joins files back together\
`cat > file1.txt` accepts input, by pressing ctrl-D saves the text to the file1.txt
`less`\
`|` pipelines (for example you can pipe the output of any command to less to easily examine that)
`sort` sorts the output
`uniq` removes duplicate lines
-d option to see duplicates
`wc` displays number of lines, words, and bytes
-l option displays number of lines (good for counting items in a list)
`find`\
`grep pattern filename`\ -i ignores case sensetivity, -v ptints only the lines that do not match the pattern
`head`\ prints first 10 line (adjust with -n option)
`tail`\ prints last 10 line, -f option to see in real time
`tee` read from stdin and output to stdout and files
`nano`/`vim`\
`open X` Open X in its default program\
`kill`/`xkill`\
`curl`\
`ssh user@ipaddress`\
`hexedit` edit file in hex mode, f2 to save, ctrl x to exit\
`feh file.jpg` view image files\
`convert file.jpg -resize  30%  file1.jpg` after installing ImageMagick use to convert file size\
`alias name='string'` name shouldn't be taken (check with type)\
`unalias command`\
`alias` list all aliases\
`>` redirect standard output (using with no command will truncate existing file or create new empty one)\
`2>`redirects standard error (file descriptor number 2)\
`>>` appends the result to an existing file or just creates one\
`&>` or `&>>` redirects of appends both standard and error outputs to file (also we can use the old version for example: ls -l /bin/usr > ls-output.txt 2>&1 (only in this order))\
`2> /dev/null` dispose of unwanted output\


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
`git clone "ssh link"` make the directory on machine\
`git add .` 
`git commit -m "message"`
`git push origin`git push origin (branch-name)` push the new branch to the remote repo\
`git status`\
`git branch (new-branch)` build a new branch\
`git checkout (branch-name)` change branch (add -b flag to build it at the same time)\
`git branch` list all branches\
`git merge (branch-name)` merges this branch to the current branch\
`git branch -d (branch-name)` delete a branch (mostly after merging)\


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
- press CTRL-SHIFT while dragging a file, to make a symbolic link in GUI.\
It’s possible to put more than one command on a line by separating each command with a semicolon.
- Using double quotes, we can cope with ﬁlenames containing embedded spaces. In general, word splitting, pathname expansion, tilde expansion, and brace expansion are suppressed; however, parameter expansion, arithmetic expansion, and command substitution are still carried out. While single quotes suppress every kind of expansion. Use backslash (escape character) to selectively prevent an expansion. Escape this by double backslashing.
- pressing Tab completes the pathname. Completion will also work on variables (if the beginning of the word is a $), usernames (if the word begins with ~), commands (if the word is the ﬁrst word on the line), and hostnames (if the beginning of the word is @). Hostname completion works only for hostnames listed in /etc/hosts.