Challenge : BLAME GAME

Objective:
Recover a hidden flag from a set of files by exploring version control history. The challenge hints toward using git, suggesting the flag might be found in previous commits or changes tracked by Git.

Step-by-Step
1. wget 'link address' to download the file
2. unzip challenge.zip
3. cd drop-in
4. ls

You’ll see multiple files here, including a Python file (message.py) and a hidden .git directory. This indicates it's a Git repository.

5. git log message.py

6. voila - there's your flag!

What I Learned
-How to explore Git history using git log
-The importance of .git metadata and how it can expose sensitive info
-That flags (or secrets) can be hidden in version control—even after being "deleted"
-To always check commit history when presented with Git-based challenges