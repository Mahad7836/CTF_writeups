Challenge: Unminify

Objective:
The objective of the Unminify challenge is to analyze a minified JavaScript file and extract the flag hidden within the code by formatting it for readability.

Steps Taken:

Opened the challenge and downloaded the provided script.js file.

Observed that the code was completely minified (i.e., all code in one line, no formatting).

Copied and pasted the code into https://beautifier.io to make it readable.

Carefully scanned through the formatted code and looked for any suspicious variables or strings.

Found a variable or function call that directly contained the flag as a string.

Result:
Flag found directly in the JavaScript source code after unminifying it. Submitted in the picoCTF format:
picoCTF{..........}

What I Learned:

How to unminify JavaScript code using online beautifiers.

Minified code is often used to hide readable data.

You don’t need to execute JS to find the flag — just formatting and searching is enough.

