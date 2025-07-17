Objective:
The objective of the DISKO 1 picoCTF challenge is to analyze a compressed disk image file, investigate its contents using basic Linux forensics tools, and recover a hidden flag stored within the image.

Steps Taken:
Identified the Disk Image File:
The challenge provided a file named disko-1.dd.gz, which appeared to be a gzipped disk image file. Running the file command confirmed that the file was gzip compressed data.

file disko-1.dd.gz

Decompressed the File:
To examine the actual disk image, I decompressed the file using:

gzip -d disko-1.dd.gz

This produced a new file named disko-1.dd.

Checked the Disk Image Format:
Using the file command again on the decompressed 
file disko-1.dd

The output revealed that this was a FAT32 filesystem:


DOS/MBR boot sector ... FAT (32 bit) ...
This confirmed the image could be navigated as a standard filesystem or parsed for strings.

Searched for Readable Strings:
Instead of mounting the image, I used the strings command, which extracts printable character sequences from binary files. Since flags are usually stored in readable form, this is a quick and effective method.

strings disko-1.dd | grep "picoCTF"

Discovered the Flag:
The output of the above command revealed the flag immediately:
picoCTF{1t5_ju5t_4_5tr1n9_be6031da}


Result:
The flag was successfully retrieved using basic forensic string extraction:

picoCTF{1t5_ju5t_4_5tr1n9_be6031da}


What I Learned:
How to inspect and decompress .gz files using gzip -d.
How to identify disk image formats using the file command.
How to use strings to extract readable data from binary files.
That sometimes, challenges can be solved without overcomplicating things—look for the simple solutions first.