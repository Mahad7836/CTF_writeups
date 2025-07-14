Challenge: RED

Objective:
The challenge involved an image with hidden data encoded into the color values or metadata. The goal was to extract the hidden information and find the flag.

Steps Taken:
- Downloaded the image and opened it using an image viewer and then an image analysis tool.
- Observed that the image appeared mostly red — suggesting data may be encoded in color channels (R, G, B).
- Used an online tool to isolate the red, green, and blue layers individually.
- In one of the layers (usually green or blue), found text or binary data representing the flag.

Result:
Extracted the flag embedded in a non-visible color channel or metadata. Submitted as picoCTF{...}

What I Learned:
- How to analyze and manipulate image color channels to detect steganographic data.
- Online tools can reveal data hidden
- Visual simpl
