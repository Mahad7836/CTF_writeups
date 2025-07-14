Challenge: flaghunters

Objective:
A web page displayed an image, and the goal was to retrieve the hidden flag embedded somewhere within the image or page source.

Steps Taken:
- Opened the provided web page in a browser.
- Right-clicked and selected "View Page Source" to inspect the HTML.
- Found a base64-encoded string hidden in a comment tag within the HTML or possibly as part of a CSS or JS file.
- Copied the base64 string and decoded it using https://www.base64decode.org/ or the `base64` command-line utility.
- The decoded text revealed the picoCTF flag.

Result:
Successfully retrieved and submitted the flag in the format: picoCTF{...}

What I Learned:
- How flags can be hidden in static web content like comments or embedded strings.
- The usefulness of developer tools and view-source inspections in CTFs.
- Practical decoding of base64 to extract hidden information.
