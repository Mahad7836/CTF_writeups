Challenge: endianness

Objective:
The objective of the endianness challenge is to understand how data is stored in memory using little-endian or big-endian formats and use this understanding to decode a given value to find the flag.

Steps Taken:

Opened the challenge and reviewed the hexadecimal data provided.

Recognized that the challenge involved endianness (byte order reversal).

Converted the hex value to bytes and manually reversed the byte order (common in little-endian systems).

Used an online hex-to-ASCII converter to transform the corrected hex into readable text.

Located the flag embedded within the output string.

Result:
The flag was extracted after correcting the byte order and decoding the data. Submitted in the picoCTF format:
picoCTF{correctly_decoded_endian_value}

What I Learned:

The difference between little-endian and big-endian byte order.

How to reverse byte sequences for decoding.

How endianness affects interpretation of binary/hexadecimal data in memory.
