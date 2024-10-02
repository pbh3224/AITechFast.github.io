---
layout:     post
title:      Linux命令
date:       2024-10-02
author:     WX
catalog: true
tags:
    - Linux
---
Directory & Files
pwd-print working directory
cd-access directory
	cd ~ = cd
	cd ..   返回上一级
	cd -   go to the last directory you were in
ls-list
	ls -lah = ll -list long format, all, human readable number
	ls Test/  used when Test is not the current working directory
man ls-manual for list command for flag
touch file1.txt-simply create a blank file
nano file2.txt-create and edit a file
cat file2.txt-display file content
mkdir Test-make directory Test
rmdir Test/-only when directory is empty
	rm -rf Test/-remove recursively and forcefully, dangerous command
mv file1.txt Test/
cp file2.txt Test/
rm Test/file2.txt
chmod 755 file1.txt-to change file permissions
nano script.sh-create a shell script(Shell scripting is a text file with a list of commands that instruct an operating system to perform certain tasks.)
./script.sh-print shell script
chmod +x script.sh
you can add alias in the .bashrc, and use source ~/.bashrc to restart bash

Find
which firefox-finding programs
whereis firefox-finding programs and its libraries
sudo apt install mlocate-to give the administrator to install mlocate
sudo apt-get update && sudo apt-get upgrade-update for update library(after installation), upgrade for apps
locate firefox-find anything contains the string “firefox”
	sudo updatedb-update database for locate command
sudo find / -iname linux-find in the root directory linux whether upper case or lower case
grep ‘alias’ .bashrc-find a specific word in the file


Print
echo “Hello world”
printf “1\n2\n3”
printf “1\n2\n3” > file1.txt-write into the file
less .bashrc-better than cat for reading long files, type q to quit
head .bashrc-first ten lines of the file
	head -n 15 .bashrc-first 15 lines
tail .bashrc-last ten lines of the file

history-show bash history
	!84-run the 84th command in the history
	apt update
	sudo !! = sudo apt update-!! for the last command
ping google.com
wget https://somelinux.com/new-release.iso
kill program name or number
kill all
xkill-fps
htop
ls -l | sed “s/[aeio]/u/g” | sort-pipe command | , pipe the result of ls into sed command, and then pipe into sort command
date
cal-calendar
bc-basic caluculator
