Challenge: binary search

Objective:
The goal of the challenge was to understand how binary search works through a simulated interaction and retrieve the flag by finding a hidden number.

Steps Taken:

Opened the challenge and was given a Python script that simulated a number guessing game using binary search.
The script allows you to input a number guess between a given range, and it tells you if the number is too low, too high, or correct.
Used the logic of binary search to minimize the number of guesses:
Started with a lower bound (e.g., 0) and an upper bound (e.g., 100).
Guessed the middle value and adjusted bounds accordingly:
Continued narrowing the range based on the script’s feedback until the correct number was found.
Upon guessing the correct number, the script revealed the flag.

Result:
The flag was revealed after implementing and completing the binary search correctly. Submitted in picoCTF format: picoCTF{...}.

What I Learned:

Hands-on understanding of how binary search narrows down options efficiently.
Importance of calculating midpoints and updating ranges carefully.
Application of binary search logic in interactive challenges.