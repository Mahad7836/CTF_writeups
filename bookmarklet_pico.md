Challenge: bookmarklet

Objective:
The objective of the bookmarklet challenge is to understand and decode a piece of JavaScript code embedded in a browser bookmark (called a bookmarklet) to extract the hidden flag.

Steps Taken:

Opened the challenge and received a JavaScript "bookmarklet" starting with javascript:.

Copied the entire bookmarklet code and pasted it into a text editor for better visibility.

Unescaped the URL-encoded characters (like %20, %3D, etc.) using an online decoder.

After decoding, formatted the JavaScript code using an online beautifier.

Carefully read through the logic and found the part of the script where the flag was either displayed, generated, logged.

Executed the script in the browser’s dev console if required to reveal the flag.

Result:
Decoded / executed the bookmarklet to extract the flag. Submitted in the picoCTF format:
picoCTF{bookmarklets_can_be_sneaky}

What I Learned:

What bookmarklets are and how they work in browsers.

How to decode URL-encoded JavaScript.

How to safely analyze small scripts to extract useful content like flags.

