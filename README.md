Directories and Files
==========

`pwd` print working directory\
`cd` changes to home directory\
`cd ..` changes to parent directory\
`cd -` changes to previous working directory\
`ls -ltrh` l for long, t to sort the result by the ﬁle’s modiﬁcation time, r to reverse the order of the sort, and h to make it human readable\
`ls -R` list recursively\
`ls -d` view permission for directories.\
`ls -F` see file type with characters /, *, and @ which correspond to dir, executable file and link.\
`ls -l $(which cp)` get list of a program without knowing it's full pathname\
`tree` visually output directory structure. -d to view only directories and -C to colorise.\
`mkdir` directory... (as many as you want)(we can use brace expansions too like this: `mkdir {2007..2009}-{01..12}`)\
`mkdir -p dir1/dir2/dir3` make parent directories as needed. option `-v` would print what was done\
`rmdir dir` directory has to be empty.\
`rmdir -p dir1/dir2` has to be empty.\
`rm -rf or -ir` r for recursively and f for forceful and i for prompting (tip: check what you want to remove, with ls first)\
`cp file1 file1copy` makes a copy of file1 named file1copy\
`cp -r dir1 dir2` makes a copy of dir1 recursively to ensure every file and directory is copied\
`cp -u *.html destination` copy only html ﬁles that do not exist in the destination directory or are newerthan the versions in the destination directory\
-i iption for copying asks before overwriting repetetive file names\
`cp file1 dir1` Copies file1 into directory dir1. The directory dir1 must already exist\
`cp dir1/* dir2` copies every file in dir1 to dir2\
`mv -i file1 file2` Move file1 to file2. If file2 exists, it is overwritten with the contents of file1. If file2 does not exist, it is created. In either case, file1 ceases to exist and prompts you before overwriting if file2 already exists\
`mv file1 .file` hides the file and vice versa.\
`mv file... -t dir` move one or more files to a directory\
`mv dir/file ./newfile` moves the file from dirctory to the current dirctory and changes it's name.\
`mv dir1 dir2` no need for the -r option\
`touch` to make a new file or update the timestamp of it's last modification. -a or -m options to update access time or modification time. use -t to specify time. -r to reference a file's timestamp to another\
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
`type` see the type of the command. use -a to see all the instances.\
`compgen -b` to print a list of all builtin commands.\
`file (fileName)` get file type. kinda works like extensions work in windows\
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
`lspci` Shows all devices currently connected to the PCI (Peripheral Component Interconnect) bus. -s to specify hex address of an individual device accompanied by -v to get a verbose response. recommended to use this command with root privilidges. -k option to see the kernel module used for this device.\
`lsusb` Lists USB (Universal Serial Bus) devices currently connected to the machine (specified by id: `lsusb -v -d 1781:0c9f`). -t to map devices as a hierarchical tree\
`lsmod` shows all currently loaded modules\
`rmmod` remove a module\
`insmod` insert a module with exact path\
`modprobe` insert a module by name (more common)\
`modprobe -r` to unload a module. -f to forcefully remove even if it's in use\
`modinfo` shows a description, the file, the author, the license, the identification, the dependencies and the available parameters for the given module. -p for parameters only.\
If a module is causing problems, we can blacklist it. add the line `blacklist module-name` to the /etc/modprobe.d/blacklist conf file. Though the better approach is to create a separate configuration file, /etc/modprobe.d/module_name.conf, that will contain settings specific only to the given kernel module.\
`lsblk` list of block devices\
`lshw` list of hardware\
`/proc` and `/sys` sudo file systems used by kernel. `/proc/cpuinfo` lists detailed info on cpus.

Get info on Boot process
====================

`dmesg`
`systemctl`


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
`less` used for pagination.g and shift g to see the beginning and end of the file. write line number then shift g to move to that line. there is also `more` command but not as good. use G and shift G to get to the top and end of file. use / to search in file and n and Shift n to see upper and lower instances.\
`od` octal dump files (mostly binary ones). use a or c option to see characters\
`sort` sorts the output alphabetically by default. -b ignores the blank spaces before sorting. -n sorts number based. -r reverses the sorting and -R sorts by random\
`nl` number the lines of a text file\
`uniq` removes duplicate lines. use -d option to see duplicates. it works on adjacents lines so it is recommended to use the sort command before hand. use -c to view the number of times it was repeated. -u to print only the unique lines.\
`wc` displays number of lines, words, and bytes. use -l option displays number of lines (good for counting items in a list)\
`split` split files into multiple ones by size, number of lines, ...\
`cut -f2 -d, file` choose a field (here the second field is chosen) and a deliminator (here is , but by default it's tab). useful for CSV files.\
`sed` use to replace words `sed 's/this/that' file` this changes the word this to that but only the first ocurrance in each line. to do it for all ocurrances use s/this/that/g (global).\
`paste`\
`tr` use to replace charecters. sed command is more common. `cat file | tr 'a' 'A'`. remember tr is a pure filter meaning it doesn't accept file as input. as an example you can build a ROT13 encoder like this: cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
. To see a better result of the PATH variable you can: echo $PATH | tr : `\n`.\
`grep pattern filename`\ -i option ignores case sensetivity, -v prints only the lines that do not match the pattern. -o prints only the parts that match. use -A1 to see one line above, -B1 to see one line below, and -C1 to see one line of context. `grep ^pattern` to check the begining of a line and `grep pattern$ to check the ending.\
`find <positon of start> option`\ -name or -iname (to ignore case sensetivity). -type f (file) or d (directory) or l (link). -not. -maxdepth N. -size (exact or + -) c for bytes, k for kilobytes, M for megabytes, G for gigabytes, or -empty. -exec to act on results (ie. `-exec file '{}' \;`) (echo, grep,...). -delete. -print. mention user and group owners by -user and -group switches.\
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
`yes` output a string repeatedly until stopped. for instance pipe `yes` to a program that requires you to give it your consent repeatedly.\
`md5sum` and `sha256sum` and `sha512sum` are examples for hashing tools.\
`tar` to archive files.\
`dd if of` can copy based on blocks and from drives.\
`cpio`\
`tee` read from stdin and output to stdout and files\
`awk '{print $2 " " $1}'` change places.\
`termgraph`\
`xargs` take output and put it in another command.\
`strings` view readable content.\
`base64 file` and -d to decode.\
`sh file` execute as shell script.\
`test or []` evaluates conditional expressions. for example [-n String] checks if the string is non-zero.\
`chsh -s /bin/bash` change shell to bash. list the available options from `cat /etc/shells`. `grep <username> /etc/passwd` to see your current bash. `usermod --shell /bin/bash <username>` is another way to do it. You can also use sudo vim to edit the /etc/passwd file, but it is not recommended.\

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

`Processes`
------------

`jobs` ctrl z stops a process and fg brings it back on. fg %n brings a certain process to life. jobs shows the status.\
`bg %n` backgrounds a process so it runs in the background.\
send a command to background by putting an & at the end of the command.\
`jobs -l` list processes with id.\
`nohup command` process goes on after the shell is closed. (used in sshing servers)\
`kill PID` -9 kill, -15 terminate (default), -1 hup.\
`killall process-name` 
`pkill name` name is not exact. patterns in names count.\



`apt`
------------

`apt list --installed`\
`apt show` see what it is before purging.\
`apt purge`\
`apt remove` If you don't want to remove the configuration files\
`apt autoremove` Remove any unused packages\
`apt clean` Remove downloaded archive files\
`apt update`\
`apt list --upgradable`\
`apt upgrade`\
`apt dist-upgrade`\

`Git`
--------------

## *Basics*

`git init` start a git repository on your folder\
`git remote add origin https//:...`\
`git push -u origin master` -u option saves your preference and from now on git push will do the same.\
`git status`check the status of your repository\
`git add .` or `git add -A` prepare files for commit ("." means all files)\
`git restore --staged myfile.py` unstage file\
`git commit -m "message"` commit the staged files\
`git log` view project history\
`git show "commit number"`view the specified commit.\
`git tag -a v1.0 -m "this is the first version"` tag versions on a current state. to go back to a previous commit to tag specify that commit number. `git show v1.0` to review. `git push v1.0` or `git push origin --tags` to push.\
`git checkout -- file` take back changes to the last commit.\
`git rm file` remove file both from working directory and index.\
`echo "*.log" > .gitignore` specify patterns for files you want to keep untracked (in this case files with log extension) in a gitignore file\
`git diff` see changes in a file. (-)shows removed and (+) shows added changes\
`git diff HEAD` see changes made compared to the last commit.\
`git diff --staged` see staged changes.\
`git branch (new-branch)` build a new branch (When you create a new branch, it starts as an exact copy of the branch you were on.) \
`git branch` list all branches (The * shows which branch you're currently in)\
`git branch -a` see all branches. This includes remote branches (when working with colaboraters)\
`git checkout (branch-name)` or `git switch (branch-name)` change branch (add -b (for checkout) or -c flag (for switch) to build it at the same time)\
`git diff branch-name` see changes made in the new branch compared to the branch-name\
`git merge (branch-name)` merges this branch to the current branch ("Fast-forward" means Git was able to simply move the current branch forward to where branch-name was. Since there was no conflict between the branches, this is the simplest form of merging)\
`git branch --merged` see which branches where integrated\
`git branch -d branch-name` delete branch after merging (-d flag is there to ensure deletion of the merged branch only. use -D to force delete)
`git stash` takes your uncommitted changes (both staged and unstaged), saves them away for later use, and then reverts them from your working copy. use to get a clean working directory. usefull before pull to avoid conflict.\
`git stash list` view your stashed instances.\
`git stash pop` reverse your last stash to working tree.\
`git stash apply stash{n}` pop the specific stash not necessarily the last one.\
`git stash push -m "message"` put your changes in stash with a message.\
`git clean` delete all the uncommited changes. can be done before pulling to make sure the code works fine outside the local machine.\
`git help command`\
`git blame file -Ln (line number)` see who changed a line.\
`git bisect` binary search of commits for the origin of a bug. `git bisect start`, `git bisect bad` ,and `git bisect good t hash"`is the process.\


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
`ssh -i sshkey user@server.domain -p portnumber` sshkey exists in current directory.\
`scp -P portnumber user@server.domain:remoteFile .` download the remoteFile from remote server to the current directory.\

# Bash Scripting

## *Start a new script*
-Shebang line: `#!/bin/bash` (as first line in the .sh file)\
-change mode of the file to executable via (new files are by default non-executable): `chmod +x file`. Execute a file before doing this by `sh file` or `bash file`.\
-Now to run the file: `./file.sh`\
Define a variable: `myFirstVariable=5` (it's assigned by = and in this case it's an integer)\
Now to print the variable: `echo "My variable is: $myFirstVariable"` (dollar sign calls the content of the variable), (put a backslash behind the dollar sign to print it literally)\
Curly braces {} are used to clearly define the variable name: `${myVariable}` (best practice)\
We can add variables in the Command Line outside the Bash script like: ./file.sh Samanth Bobby. here the first word is a variable in $1 and the second in $2 and so on. use echo $@ to print all. $0 is a reference to the script itself. `echo $0` will print the name of the script and `rm -f $0` will self destruct.\
Arrays are like variables that can hold more than one variable under one name. my_array=("value 1" "value 2" "value 3" "value 4"). we access each variable by it's numeric index using curley brackets: ${my_array[1]} is a reference to value 2. ${my_array[-1]} this is value 4. echo ${my_array[@]} will return all arguments. Prepending the array with a hash sign would output the total number of elements in the array, in our case it is 4: echo ${#my_array[@]}.\
Take variable input from user using `read`: read name; echo $name. this will take name from input and print it. print a message
before prompting the user for their input using the -p option and writing the prompt in double quotes. use -r to print what you give as raw. notice that read only reads the first line.\
use `thing=$(uname -a)` syntax to put the result of a command in a variable. the older syntax is like this: `thing=`uname -a``.\
In order to preserve white space in a variable use double quotes when using echo, otherwise it would not be printed\
In many cases, instead of an if syntax its easier to use something like [command] && command, and for the else clause [command] || command. it is possible to group commands like this: command || { command ; exit ; } here we only exit if the first command fails (note that if we had put the commands in paranthesis, they would be executed in a sub-shell and exiting from a sub-shell wouldn't be enough for us)(note that the compound commands must end with a ; and a white space (otherwise it gets confused with the closing brace of shell variable syntax) or a new line before closing it).\
Note: if you want to do nothing after then in an if statement put : there.\
basic looping construct:\ 
for ((i=0; i<10; i++)); do\ 
<command>\
done\
deliberate infinite loop:\ 
for ((;;)); do\
<command>\
done\
There is also: while true; do\ 
A for loop that iterate over the parameters to the script ($1 then $2 and $3 and so on):\ 
for value; do\ 
echo "$value"\
done\
The for loop can be given a list of values to loop over. for instance: for num in 1 2 3 4 5; do... .It can also be a command or pipeline of them. for i in $(seq 1 10) is equal to for ((i=1; i<=10; i++)).\
when declaring a variable in a function use `local` before it to not polute the names, since it becomes global otherwise.\
It is possible to check a command with if. if the command works with no errors, then if is true.\
Use `bash -n script` to perform a syntax check.\
In the case syntax if you close each case with ;;& it will fall through to check the next case.\
If you exapand an array like a variable, it will only expand to the first index ($array. to get certain indexes use ${$array[1]}.\
To loop over all the indexes use @. it's important to put the whole thing in double quotes: for item in "${array[@]}".\
To copy an array correctly: second_array=("${first_array[@]}").\
To push items to an existiong array: second_array+=(item1 item2).\
It's possible to use declare -a command to make new arrays. If you want to see that a variable is actually an array use declare with -p option.\
Get the length of an array: echo "#${array[@]}". put the index number to get the length of the string in that index.\
Use declare -A arr to build associative arrays (kinda like objects). arr[foo]=1 to put value in it. echo "${arr[*]}" to see values and echo "${!arr[*]}" to see the keys.\
put a new value to IFS such as a ',' is very powerfull. you can do this when stringifying the arrays values with '*'. In order not to have to worry about changing IFS, you can do so in a subshell, by putting the code in ().\
Command substitution can be done by backticks. It's better to use $(command) (it will be run in a subshell). A new syntax to avoid subshells: thing=${ myfunc ;}/\
Use let or (()) for arithmetic operations. The curve ball on this one is that (()) returns an exit code and if the arithmetic equalls to 0 the exit code is going to be 1.\
Some reserved exit codes: 1: catchall for general errors. 126: command cannot be executed. 127: command not found. 130: Script terminated by Control-C. Exit codes 1 - 2, 126 - 165, and 255 have special meanings, and should therefore be avoided for user-specified exit parameters. Restricting user-defined exit codes to the range 64 - 113 (in addition to 0, for success) is the c/c++ standard. An exit value greater than 255 returns an exit code modulo 256.\
`Set e` put it at the top of the bash script and it will exit on error. Another thing is that a leading zero in the number you put inside it, makes it treat it as an octal number. One way around this is to declare the base to ten, so if we have a=08, ((10#$a)) will put it in base 10.\
`set x` for debugging.\
Exit the script at the end. just saying exit will return the exit value of the last run command. or exit 0 to indicate success.\
cat /dev/null > to a file to clean it up.\
`Bash -x script` puts bash in debug mode. also we can put `set -x` in the script. and `set +x will turn it off. You can write a message before the outputs by using: PS4='[debug]= ' bash -x script.sh. bash -u looks for undefined variables\


Intersting stuff
==========

- If you highlight some text by holding down the left mouse button and dragging the mouse over it (or double-clicking a word), it is copied into a buffer maintained by X. Pressing the middle mouse button will cause the text to be pasted at the cursor location.\
- We can end a terminal session by closing the terminal emulator window, by entering the exit command at the shell prompt, or by pressing CTRL-D.
- press CTRL-SHIFT while dragging a file, to make a symbolic link in GUI.\
- It’s possible to put more than one command on a line by separating each command with a semicolon. If there is && between the two commands, the second command will only get executed if the first command is successful. || works as an OR conditional, meaning the second command will only get executed if the first one fails.\
- Using double quotes, we can cope with ﬁlenames containing embedded spaces. In general, word splitting, pathname expansion, tilde expansion, and brace expansion are suppressed; however, parameter expansion, arithmetic expansion, and command substitution are still carried out. While single quotes suppress every kind of expansion. Use backslash (escape character) to selectively prevent an expansion. Escape this by double backslashing.\
- pressing Tab completes the pathname. Completion will also work on variables (if the beginning of the word is a $), usernames (if the word begins with ~), commands (if the word is the ﬁrst word on the line), and hostnames (if the beginning of the word is @). Hostname completion works only for hostnames listed in /etc/hosts.\
-wild cards: `*` represents zero or more characters. `?` represents a single character. `[]` represents a range of characters\
-three ways to execute a command. either it is built-in, exits in the PATH and can be executed from any directory or if not it will be executed only by mentioning the absolute path.\
- send stderr to null drive to prevent it from getting printed on output by 2> /dev/null.\
- 

