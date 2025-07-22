Challenge: Secret of the Polyglot

Objective:
Understand how polyglot files can be interpreted differently by different interpreters/parsers and extract the hidden flag.

Steps Taken:

Opened the challenge and downloaded the provided file.

Ran the file command on the terminal to determine the file type. It showed multiple formats, suggesting it’s a polyglot (e.g., both PNG and PDF).

Tried opening the file in an image viewer—it displayed an image and one part of the flag.

Resaved the image as .png

Tried to open it again

Found other part of flag(the first half)

Combined the 2 parts and got the main flag


What I Learned:

What polyglot files are and how they work.
How to use file and to analyze file structures.
How some programs read only part of a file based on their expected headers.
How to extract embedded files from within seemingly unrelated formats.