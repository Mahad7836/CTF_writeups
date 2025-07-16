Challenge: binhexa

Objective:
The objective of the binhexa challenge is to convert between binary and hexadecimal representations to reveal a hidden flag.

Steps Taken:

Opened the challenge and observed that a string of digits  was provided.

Determined the direction of conversion needed: binary → hex or hex → ASCII.

If binary: grouped the binary into 8-bit segments, converted each to decimal, then to ASCII.

If hex: removed any delimiters (e.g., 0x, spaces), converted the hex to ASCII directly using an online tool or Python script.

Reviewed the output for the flag formatted in picoCTF{...} style.

Result:
Converted the given binary or hex sequence to text, revealing the flag. Submitted in the picoCTF format:
picoCTF{converted_binary_or_hex_to_text}

What I Learned:

How to manually convert binary/hex to ASCII using grouping and conversion.

Tools and techniques to speed up conversion (online converters, Python’s chr(int(),16) or binascii).

How encoding formats can be used to obfuscate flags in CTFs.

