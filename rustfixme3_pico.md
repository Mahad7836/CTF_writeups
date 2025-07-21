Challenge: Rust FixMe 3

Objective:
This challenge required fixing a more advanced Rust program designed to decrypt a message using XOR and raw pointers. The goal was to resolve multiple compilation errors, including unsafe memory operations, and produce the correct output (the flag).

Steps Taken:

Opened the Challenge:
On reviewing the provided Rust source code, I saw several compilation errors involving unsafe pointer dereferencing, improper use of Result, and formatting issues. 

The program attempted to decrypt a buffer and print the result.


Problem: A Result was not properly checked before being used, which could lead to a panic.
Solution: I used .is_err() to check if decoding failed and added an early return; if that was the case.

Problem: The code used from_raw_parts without wrapping it in an unsafe block.
Solution: I wrapped the raw pointer conversion in an unsafe block and ensured the pointer math was sound.


Problem: The program attempted to decode a raw buffer but didn’t convert the result into a proper UTF-8 string.
Solution: I used String::from_utf8_lossy(...) to safely handle and convert the byte slice to a human-readable string.


Problem: Similar to FixMe 2, the println! macro didn’t include the {} placeholder.
Solution: I added "{}" to the macro to properly display the flag string.



Result:
The flag was revealed successfully:
picoCTF{n0w_y0uv3_f1x3d_1h3m_411}

What I Learned:

How to safely use raw pointers and wrap unsafe operations in Rust.

Better understanding of handling Result types and avoiding panics using .is_err() and early returns.

Techniques for decoding byte slices using String::from_utf8_lossy.

The importance of correctly formatting output in println!.

Gained more confidence in working with unsafe Rust, memory manipulation, and error handling.

