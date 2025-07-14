Challenge: hashcrack

Objective:
Given a hash value, identify the hashing algorithm used and find the original input that produces that hash. No cracking tool was pre-installed; online tools like CrackStation were allowed.

Steps Taken:
- Opened the challenge and found a single hash value.
- Observed the length and format of the hash to determine likely algorithm (e.g., MD5 = 32 hex characters).
- Used https://crackstation.net/ to paste the hash and retrieve the plaintext.
- Cross-verified the output with the flag format expected by picoCTF.

Result:
The cracked hash revealed the original string. Submitted in the picoCTF format: picoCTF{...}

What I Learned:
- How to visually recognize hash types based on length and structure.
- Practical use of online rainbow tables and hash databases.
- Reinforced the importance of not storing passwords as unsalted hashes in real-world systems.
