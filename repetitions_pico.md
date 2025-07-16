Challenge: repetitions

Objective:
The objective of the repetitions challenge is to identify and decode a message that contains repeating patterns or characters, usually indicating some form of simple obfuscation or cipher.

Steps Taken:

Opened the challenge and reviewed the given text, which showed a pattern of repeated characters.

Noticed characters were repeated a set number of times (e.g., aaabbbccc...).

Assumed it was encoded using a simple repetition-based encoding like Run-Length Encoding (RLE).

Found a Python script to reduce each character sequence to a single instance (e.g., aaa → a).

After reducing the repetitions, a readable flag emerged in plain text.

Result:
Successfully reduced repeated characters and recovered the flag. Submitted in the picoCTF format:
picoCTF{simple_pattern_obfuscation}

What I Learned:

How to recognize encoding via repetition techniques.

Applied a simple decoding method using pattern reduction.

Pattern recognition is key even for basic CTF challenges.
