Directories and Files
==========

`pwd` print working directory\
`cd` changes to home directory\
`cd ..` changes to parent directory\
`cd -` changes to previous working directory\
`ls -ltrh` l for long, t to sort the result by the ﬁle’s modiﬁcation time, r to reverse the order of the sort, and h to make it human readable\
`ls -R` list recursively\
`ls -d` view permission for directories.\
`ls -l $(which cp)` get list of a program without knowing it's full pathname\
`mkdir` directory... (as many as you want)(we can use brace expansions too like this: `mkdir {2007..2009}-{01..12}`)\
`mkdir -p dir1/dir2/dir3` make parent directories as needed. option `-v` would print what was done\
`rm -rf or -ir` r for recursively and f for forceful and i for prompting (tip: check what you want to remove, with ls first)\
`cp file1 file1copy` makes a copy of file1 named file1copy\
`cp -r dir1 dir2` makes a copy of dir1 recursively to ensure every file and directory is copied\
`cp -u *.html destination` copy only html ﬁles that do not exist in the destination directory or are newerthan the versions in the destination directory\
-i iption for copying asks before overwriting repetetive file names\
`cp file1 dir1` Copies file1 into directory dir1. The directory dir1 must already exist\
`cp dir1/* dir2` copies every file in dir1 to dir2\
`mv -i file1 file2` Move file1 to file2. If file2 exists, it is overwritten with the contents of file1. If file2 does not exist, it is created. In either case, file1 ceases to exist and prompts you before overwriting if file2 already exists\
`mv file1 .file` hides the file and vice versa.
`mv file... dir` move one or more files to a directory\
`mv dir/file ./newfile` moves the file from dirctory to the current dirctory and changes it's name.\
`mv dir1 dir2` no need for the -r option\
`touch` to make a new file or update the timestamp of it's last modification (`touch new.txt` or in another directory `touch /home/user/project/new.txt`\
`ln file link` create hard link\
`ln -s item link` creat soft link (item is either a file or a directory)\
`diff file1 file1` shows the changes needed in file1 in order for it to match file2\
`diff -r dir1 dir2` compares dirctories contents recursively\

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
`open X` Open X in its default program\


Get info 
==========
`date` displays the current time and date\
`cal` displays a calendar of the current month\
`host` see the host name\
`whoami` get username\
`whatis command` gives short description\
`which`print absolute location of a command\
`whereis`\
`type` see the type of the command\
`file (fileName)` get file type\
`info command` gives info\
`uname -a` get system information (-a for all options)\
`uptime` view system's uptime\
`cat /etc/os-release` view os version info\
`man <command>` print manual for the certain command. search for certain words by pressing forward slash\
`man -k <search term>` search for the words you remember when you are not sure of the command. `apropos` command does the same\
`help <command>` view basic info on built-in commands\
`history` get a list of previous commands\
`!!` get the last command\
`sudo !!` run previous command with privileges\
`!abc:p` print the last command starting with abc\
`!53` recall and execute the command associated with the history number\
`history -c` delete history\
To start incremental search, press CTRL-R followed by the text you are looking for. When you ﬁnd it, you can either press ENTER to execute the command or press CTRL-J to copy the line from the history list to the current command line, or ctrl-O to execute. To ﬁnd the next occurrence of the text (moving “up” the history list), press CTRL-R again. To quit searching, press either CTRL-G or CTRL-C.\
`history n` print n numbers of commands\
`history | grep <command>` pipe it to grep to search for a certain command or phrase.\
`cat .bash_history` this file updates itself with the new commands after ending a session.\
`export HISTSIZE=50` change history size to 50. choose zero to delete history.\
`history > cmds.txt` save history to a cheatsheet\
`echo` (for example echo [[:upper:]]* (it expands and echos list of files starting with uppercase))
Also can be used as a claculator: $((mathematical expression))
Parameter expansion (echo $USER)\
Or command substitution: echo `$(ls)`\
`echo $HISTSIZE` display system variables\
`echo "new line" > textfile.txt` make a text file with this line in it (for adding another line you should use >> or it would rewrite the file instead of appending)\
`echo rm -rf *` can be used to check the commands (in this case a dangerous one) before executing them.\
`echo -e "\e[1;37;41mThis is white text on red background\e[0m"` `echo -e "\e[31mThis \e[32mis \e[33ma \e[34mrainbow \e[35mtext\e[0m"` `echo -e "\e[5mThis is blinking text\e[0m" `format the output.\
`top`/`htop`\
`ping`/`ifconfig`\
`df` displays the current amount of free space on our disk drives\
`free` displays the amount of free memory\
`env` or `printenv` prints a list of available variables. `set` prints almost the same content, but it includes the local variables.\
`set VAR` set a new variable (locally, it will be gone after reboot), `export` it to pass it to child shells and clean it up by `unset` command\


Get info on hardware 
====================
`lspci` Shows all devices currently connected to the PCI (Peripheral Component Interconnect) bus\
`lsusb` Lists USB (Universal Serial Bus) devices currently connected to the machine (specified by id: `lsusb -v -d 1781:0c9f`)\
`lspci -s 04:02.0 -v` shows more details about a specific device (kernel module can be identified)\
`lsmod` shows all currently loaded modules
`modprobe -r` to unload a module\


Tools
==========

`cat` repeats whatever you write and then enter\
`cat file.txt` displays text file\
`cat -n` displays text with number of lines\
`cat > file1.txt` accepts input, by pressing ctrl-D (end program) or ctrl-C (cut the program) saves the text to the file1.txt\
`cat file1.txt > file2.txt` acts like the copy command. if the file already exits, overrides it\
zipped files such as bizp, xz, gzip files can respectively be looked at via bzcat, xzcat, and zcat commands without unzipping.\
`head` prints first 10 line (adjust with -n option) (the -c option is for the number of bytes (characters) shown)\
`tail` opposite of the head command. -f option is very useful for keeping an eye on a file as it gets updated.\
`less` used for pagination.g and shift g to see the beginning and end of the file. write line number then shift g to move to that line. there is also `more` command but not as good\
`od` octal dump files (mostly binary ones). use a or c option to see characters\
`sort` sorts the output alphabetically by default. -b ignores the blank spaces before sorting. -n sorts number based. -r reverses the sorting and -R sorts by random\
`nl` number the lines of a text file\
`uniq` removes duplicate lines. use -d option to see duplicates. it works on adjacents lines so it is recommended to use the sort command before hand. use -c to view the number of times it was repeated. -u to print only the unique lines.\
`wc` displays number of lines, words, and bytes. use -l option displays number of lines (good for counting items in a list)\
`split` split files into multiple ones by size, number of lines, ...\
`cut -f2 -d, file` choose a field (here the second field is chosen) and a deliminator (here is , but by default it's tab). useful for CSV files.\
`sed` use to replace words `sed 's/this/that' file` this changes the word this to that but only the first ocurrance in each line. to do it for all ocurrances use s/this/that/g (global).\
`paste`\
`tr` use to replace charecters. sed command is more common. `cat file | tr 'a' 'A'`. remember tr is a pure filter meaning it doesn't accept file as input.\
`grep pattern filename`\ -i option ignores case sensetivity, -v prints only the lines that do not match the pattern\
`find`\
`tee` read from stdin and output to stdout and files\
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
`chmod [permissions] [path]` change persmission for (ugoa) user (or owner), group, others, all, granting or revoking the permission - indicated with either a plus ( + ) or minus ( - ), Which permission are we setting? - read ( r ), write ( w ) or execute ( x ). example: `chmod u-w file.txt` take away writing permission from user.
You can easily use three numbers from 0-7 to specify permissions for the user, group and others (for example: chmod 751 file.png = -rwxr-x--x)\
`ls -d dir` to see persmissions for a directory. ability to read the contents of the directory (ie do an ls), ability to write into the directory (ie create files and directories), ability to enter that directory (ie cd).
we need to remember is that these permissions are for the directory itself, not the files within.
`yes` output a string repeatedly until stopped.\
`md5sum` and `sha256sum` and `sha512sum` are examples for hashing tools.\

`vi`
------------

`vi newtext.txt` open or edit file\
`i` switch to insert mode\
**push esc** to get back to normal mode. Now in normal mode:\
`:w` save and get back to writing\
`ZZ` or `:wq` save and quit\
`:q!` quit without saving\
`dd` delete one line\
`gg` move the cursor to the beginning of the text\
use h, j, k, and l keys to move the cursor to left, down, up, and right.\
use the `/` to search for words. use `n` to see next occurances.\
`dw` to delete the word your cursor is at.\
`x` to delete a single character.\
`a` to append text at the cursor.\
`d$`  to delete to the end of the line.\




`apt`
------------

`apt list --installed`\
`apt purge`\
`apt remove` If you don't want to remove the configuration files\
`apt autoremove` Remove any unused packages\
`apt clean` Remove downloaded archive files\
`apt update`\
`apt list --upgradable`\
`apt upgrade`\
`apt dist-upgrade`

`Git`
--------------

## *Basics*

`git init` start a git repository on your folder\
`git status`check the status of your repository\
`git add .` prepare files for commit ("." means all files)\
`git restore --staged myfile.py` unstage file\
`git commit -m "message"` commit the staged files\
`git log` view project history\
`echo "*.log" > .gitignore` specify patterns for files you want to keep untracked (in this case files with log extension) in a gitignore file\
`git diff` see changes in a file. (-)shows removed and (+) shows added changes\
`git diff --staged` see staged changes\
`git branch (new-branch)` build a new branch (When you create a new branch, it starts as an exact copy of the branch you were on.) \
`git branch` list all branches (The * shows which branch you're currently in)\
`git branch -a` see all branches. This includes remote branches (when working with colaboraters)\
`git checkout (branch-name)` or `git switch (branch-name)` change branch (add -b (for checkout) or -c flag (for switch) to build it at the same time)\
`git diff branch-name` see changes made in the new branch compared to the branch-name\
`git merge (branch-name)` merges this branch to the current branch ("Fast-forward" means Git was able to simply move the current branch forward to where branch-name was. Since there was no conflict between the branches, this is the simplest form of merging)\
`git branch --merged` see which branches where integrated\
`git branch -d branch-name` delete branch after merging (-d flag is there to ensure deletion of the merged branch only. use -D to force delete)

## *set up*
`git config` configure git on three levels: system level (apply to all machines), global level (apply for all projects on the machine), local level (apply to a particular project)\
`git config --list` display all configured variables (can specify with --global or --local options)\
`git config --global user.name "Your Name"` set your name globally (`git config --global user.name` to verify)\
`git config --global user.email "your.email@example.com"` set your email globally (`git config --global user.email` to verify) (better to use github prvate email)\
`git config --global color.ui auto` turn on color display globally\
`git config --global core.editor nano` set Nano as your default editor\
`git config --global core.autocrlf input` onvert CRLF to LF when you commit but not on checking out\
`git config --global alias.st status` creates an alias st for the status command\
`git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"` sets an alias for the log command and makes the output look better\
`git config --global init.defaultBranch main` for recent changes on github\
`git config --global pull.rebase false` set your default branch reconciliation behavior to merging\


## *build ssh key pairs*

`ssh user@ipaddress`\
`ssh user@server.domain -p portnumber`\

# Shell Scripting
Shebang line: `#!/bin/bash` (as first line in the .sh file)\
change mode of the file to executable via (new files are by default non-executable): `chmod +x file.sh`\
Now to run the file: `./file.sh`\
Define a variable: `myFirstVariable=5` (it's assigned by = and in this case it's an integer)\
Now to print the variable: `echo "My variable is: $myFirstVariable"` (dollar sign calls the content of the variable), (put a backslash behind the dollar sign to print it literally)\
Curly braces {} are used to clearly define the variable name: `${myVariable}`\
In order to preserve white space in a variable use double quotes when using echo, otherwise it would not be printed\



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
- It’s possible to put more than one command on a line by separating each command with a semicolon.
- Using double quotes, we can cope with ﬁlenames containing embedded spaces. In general, word splitting, pathname expansion, tilde expansion, and brace expansion are suppressed; however, parameter expansion, arithmetic expansion, and command substitution are still carried out. While single quotes suppress every kind of expansion. Use backslash (escape character) to selectively prevent an expansion. Escape this by double backslashing.
- pressing Tab completes the pathname. Completion will also work on variables (if the beginning of the word is a $), usernames (if the word begins with ~), commands (if the word is the ﬁrst word on the line), and hostnames (if the beginning of the word is @). Hostname completion works only for hostnames listed in /etc/hosts.
-wild cards: `*` represents zero or more characters. `?` represents a single character. `[]` represents a range of characters\
-difference between " and '. single quotes preserve literal value of all characters. for instance echo "$PATH" prints the content of the variable but echo `$PATH` prints %PATH literally.\
-three ways to execute a command. either it is built-in, exits in the PATH and can be executed from any directory or if not it will be executed only by mentioning the absolute path.\
