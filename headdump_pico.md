Challenge: Head Dump

Objective:
Extract the hidden flag from a heap dump using common reverse engineering techniques and command-line tools.

Steps Taken:

I started by launching the instance provided in the challenge. The link led me to a web interface, and upon navigating through the documentation, I noticed something unusual about the #api_documentation hash. It seemed a bit different from what I expected.

Clicking on the #api_documentation took me to a Swagger UI interface, which is a tool for testing APIs. It presented various API endpoints.

At the bottom of the Swagger UI page, I saw an option labeled heap-dump. I clicked on it, which allowed me to "Try it out" directly from the UI.

Once I clicked "Try it out," the interface showed me an option to execute the heap dump. I triggered it, and it gave me a set of commands that I could run to interact with the server.

Using the wget command, I downloaded the heap dump file directly to the webshell. The file was named something like heapdump.1.

I used the file command on the heap dump file (file heapdump.1) to check its contents. The result indicated that the file was ASCII text with very long lines (826 characters per line), which suggested it was a text-based file, potentially with embedded data.

To extract meaningful information, I ran the strings command on the file, which pulls out printable strings from binary or text files. I then piped it to grep to search for the keyword picoCTF:

strings heapdump.1 | grep "picoCTF"

This returned the hidden flag embedded in the heap dump file. I immediately noted the flag and used it to complete the challenge.

What I Learned:
Heap Dumps and APIs: I learned how heap dumps can be retrieved via API tools like Swagger UI and how they might contain valuable data that can be extracted using command-line tools.

Using File and Strings Commands: The file command helped identify the type of data, and strings combined with grep were useful for searching through the file's contents to find the hidden flag.

Efficient Flag Extraction: I discovered how simple but effective tools like strings and grep can be used in combination to sift through large files and extract specific data, even when it's embedded in seemingly unrelated information.