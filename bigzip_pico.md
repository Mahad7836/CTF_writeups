Challenge: big zip

Objective:
The objective of the big zip challenge is to explore a zip archive containing multiple or deeply nested files/folders in order to uncover the flag hidden somewhere within the contents.

Steps Taken:

Opened the challenge and downloaded the provided .zip archive file.

Unzipped the file and noticed it contained either many files / nested directories.

Used webshell to navigate through the folders.

Applied commands like ls, cd, cat, or grep to search for files likely containing the flag.

grep "picoCTF" to automate the flag search.

Result:
Located the flag inside one of the files after exploring/scanning the contents of the zip. Submitted in the picoCTF format:
picoCTF{flag_found_among_nested_files}

What I Learned:

How to handle zip files with many entries or deep directory structures.

Learned to automate file content searching using shell scripting or recursive tools.

Efficient use of Linux CLI (e.g., find, grep, cat) in CTF scenarios.

