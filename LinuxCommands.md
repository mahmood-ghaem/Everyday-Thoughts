# Learn Linux commands useful in Docker

`docker pull ubuntu`

`docker run -it ubuntu` interactive

`docker ps` process

`docker ps -a` all process include stoped

Note: `root@41440f4e1e7f:/#` root is loged in user, 41440f4e1e7f is the name of machine that automaticaly generated, `/` represents that where we are in the file system and means root directory highest directory in Linux file system, `#` highest privilages because root user `$` means normal user not root user.

`echo hello` shows hello

`whoami` shows current user

`echo $0` shows the location of the shell program.

Note: `bash` Bash is the shell, or command language interpreter, for the GNU operating system. The name is an acronym for the **' Bourne-Again SHell '**, a pun on Stephen Bourne, the author of the direct ancestor of the current Unix shell sh , which appeared in the Seventh Edition Bell Labs Research version of Unix.

Note: Differents between Windows and Linux: Windows `dir1\dir2` Linux `dir1/dir2`, Linux is case-sensitive.

`history` shows all command used localy

`!2` runs the command number 2 from history

`apt list` list of all application package in database

`apt update` update the list

`apt install nano` install nano text editor

`apt remove nano` remove nano text editor

`ctrl+l` clear console window

`pwd` prints working directory

`ls` list of all files and directories in current location

`ls -1` list each item in one line

`ls -l` long list

`cd ~` do to home directory

`mkdir`, `mv dir1 dir2` change the name, `touch hello.txt`, `touch file1.txt file2.txt file3.txt`, `rm hello.txt`, `rm file1.txt file2.txt file3.txt`, `rm file*`, `rm -r dir/` delete all files and folder inside dir (recursive).

`ctrl+w` delete a word

`nano file1.txt`

`cat file1.txt`, `more file1.txt`, `less file1.txt`, `head -n 5 file1.txt` shows first 5 lines, `tail -n 5 file1.txt` shows last 5 lines

`cat file1.txt > file2.txt` redirection change standard output from screen to a file, `cat file1.txt file2.txt > file3.txt` concatenate

`echo hello > hello.txt`, `ls -l /etc > files.txt`

`grep -i hello file1.txt` stands for global regular expression print, case-insensitive, search hello in file1.txt

`grep -i hello file1*`, `grep -i -r hello .` or `grep -ir hello .` search in current directory

`find` without filter shows all file and directories recursively

`find -type d` shows all directories recursively

`find -type f` shows all files recursively

`find -type f -name "f*"` shows all files start with f

`;` after a command in a line of commands, `;\` go to new line after a command, `command1 | command2` send command1 to command2, `command1 && command2` if command1 works then go to command2 else go out, `command1 || command2` command1 or command2

`printenv` shows environment variables, `printenv PATH` or `echo $PATH`

`export DB_USER=testuser` add key value to current shell environment variable, `printenv DB_USER` or `echo $DB_USER`

`exit`, `docker start -i 2f7` interactive, container ID

`cd ~ ; ls -a ; echo DB_USER=testuser >> .bashrc` append key value to .bashrc, now after restart machine this variable will be alive

`source ~/.bashrc` to reload .bashrc

`ps` shows all running process

`sleep 100 &` start a process in background

`kill 38` stop process number 38

`useradd -m john` create john user with home directory, `cat /etc/passwd` shows created user `john:x:1000:1000::/home/john:/bin/sh`

`adduser bob` create bob user with more interactive steps

`addgroup app && adduser -S -G app app`

`groups app`

`usermod -s /bin/bash john` modify john's starting shell from `sh` to `bash`

`cat /etc/shadow` shows users' passwords in an encrypted format, only accessible for the root user.

`docker exec -it -u john 6af bash` login with john

`groupadd developers` create developers group, `cat /etc/group`

`usermod -G developers john` adding john to developers group and developers for john isn't primary group if use `-g` then developers gonna be as a primary group for john.

`cat /etc/passwd | grep john` or `grep john /etc/passwd` shows only john record with primary group id, `groups john` shows all group for john

`echo echo hello > deploy.sh ; ls -l ; chmod u+x deploy.sh ; ls -l ; ./deploy.sh` create deploy script file and change the execution permission of that.

`chmod o+x deploy.sh` add execution permission to all users, `chmod g+x deploy.sh` add execution permission to group of current user

`userdel john` delete john

[Referense](https://codewithmosh.com/p/the-ultimate-docker-course)
