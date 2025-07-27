Challenge: ph4nt0m 1ntrud3r

Tools Used: Wireshark, Online Base64 Decoder
Hint Given: “Time is essential”

Challenge Description:
The challenge provided a .pcap file and a subtle hint: "Time is essential." Our goal was to investigate the captured network traffic to uncover a hidden flag.

Step-by-Step Solution:
1. Opening the PCAP File
First, I downloaded the provided .pcap file and opened it using Wireshark, a powerful network protocol analyzer.

2. Interpreting the Hint - "Time is essential"
The hint pointed towards the importance of time in the analysis. So, in Wireshark:

I clicked on the "Time" column to sort packets chronologically.

This helped spot any anomalies or patterns in the timing or sequence of packets.

3. Identifying Suspicious Packets
Upon scrolling through the sorted packet list, I noticed something interesting:

A set of packets with a length of exactly 12 bytes.

These packets stood out due to their uniform size and consistent spacing.

Curious, I inspected the packet bytes in the lower pane of Wireshark.

4. Recognizing a Pattern: Base64 Encoding
Inside the 12-byte packets:

The ASCII view showed strings ending in ==.

This strongly suggested Base64-encoded data, as == is typical padding in Base64.

5. Extracting the Data
For each suspicious 12-byte packet:

Right-clicked → Copy → Bytes → Hex + ASCII Dump.

Pasted the content into a text editor.

Manually isolated only the Base64-looking characters (usually in the ASCII portion).

Removed all non-relevant hex and formatting.

6. Decoding the Base64
One by one, I pasted the cleaned Base64 strings into an online Base64 decoder.

Each decoded string gave me a fragment of the flag or readable English text.

I continued this process for all 12-byte packets.

7. Reconstructing the Flag
Once all Base64 strings were decoded, I:

Collected the decoded fragments in sequence (according to time).

Combined them carefully to reconstruct the full flag.

And just like that...
we got the flag!

Key Takeaways:
Always pay attention to packet length anomalies.

The "Time is essential" hint was crucial — sorting by time revealed a logical sequence.
Recognizing Base64 patterns in ASCII helped identify hidden data.
Manual analysis can be tedious but effective for small datasets like this.