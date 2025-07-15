Challenge: super ssh

Objective:
Connect to a remote machine over SSH using provided credentials, explore the environment, and find the hidden flag.

Steps Taken:
- Received a username with a password/ private SSH key.
- Used the `ssh` command: using the hint given in the challenge.
- Navigated through directories using `ls`, `cd`, `cat`, and `find` to search for flag-like files.
- Looked in common locations or hidden directories.
- Ensured hidden files (`.filename`) and permissions were checked.
- Upon discovering a file containing the flag, used `cat` to read it.

Result:
Successfully accessed the server and retrieved the flag from a hidden or protected file. Submitted as picoCTF{...}

What I Learned:
- How to securely and correctly connect via SSH.
- Linux navigation and file discovery via CLI tools.
- Practice in thinking like an attacker while exploring unfamiliar file systems.
