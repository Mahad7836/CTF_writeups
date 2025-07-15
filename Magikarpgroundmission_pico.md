Challenge: Magikarp Ground Mission

Objective:
The objective of the Magikarp Ground Mission picoCTF challenge is to connect to a remote server via SSH, navigate through the file system, and find three hidden flag parts within the files.

Steps Taken:
- opened the challenge. additional details gave command on how to ssh
- used password to get through and get access
- used 'ls' to see files in directory, found 1/3 of flag
- opened instructions of 2nd part of flag using 'cat'
- used '/' to go to root directory then again did 'ls', found 2/3 flag
- again opened instructions using 'cat'
- used '~' to go to the last directory for 3rd part of flag. found the last part and combined all 3 parts 

Result:
The txt of the 3 files combines to give the flag. Submitted in the picoCTF format: picoCTF{...}

What I Learned:
- how to navigate through directories in linux
- commands such as /, ~, cd, ls, ssh