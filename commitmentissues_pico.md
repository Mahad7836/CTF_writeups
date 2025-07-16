Challenge: Commitment Issues

Objective:
The objective of the Commitment Issues picoCTF challenge is to explore a Git repository structure, navigate through its history and content, and recover the flag hidden within the files.

Steps Taken:

Unzipped the Challenge Files:

The challenge starts with a challenge.zip file. After unzipping, I found a directory called drop-in containing a .git directory, a message.txt file, and several other files.

Checked Git Repository:

After confirming that this was indeed a Git repository (based on the .git directory), I used Git commands to explore the repository and its commit history.

Running git log revealed some commit messages, such as "remove sensitive info" and "create flag", which hinted that the flag was hidden in the repository's history.

Explored Commit History:

I examined the commit logs using git log. The key commit to focus on was b562f0b425907789d11d2fe2793e67592dc6be93, which had the message "create flag". This likely contained the flag or a reference to it.

However, running git show b562f0b425907789d11d2fe2793e67592dc6be93 initially resulted in an error because I wasn't inside a Git repository context.

Navigating the File System:

I made sure to be inside the correct repository folder (drop-in/.git) before running any Git commands. Once inside, I ran git show to inspect the changes in the commit b562f0b425907789d11d2fe2793e67592dc6be93.

Discovered the Flag:

In the commit details, I found references to message.txt. I opened this file using the cat command and discovered a hidden message with part of the flag or a clue to the flag's structure.

Extracted the Full Flag:

By exploring more Git logs and checking various file versions, I was able to gather all the parts of the flag, eventually reconstructing it.

Result:
The content of the message.txt file, combined with Git commit history, led me to recover the flag, which was submitted in the format: picoCTF{...}.

What I Learned:

How to interact with and explore Git repositories using basic Git commands (git log, git show, etc.).

How to navigate the file system in a remote environment.

How to extract hidden information and clues from Git commit history.

Basic Linux commands for file manipulation (ls, cat, etc.).