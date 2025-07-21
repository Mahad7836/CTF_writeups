Challenge: Rust FixMe 2

Objective:
The challenge involved fixing compilation issues in a Rust program that was meant to decode a hidden message (the flag). The primary goal was to correct minor syntax and formatting issues to get the program to compile and display the correct flag.

Steps Taken:

Opened the Challenge:
I opened the Rust FixMe 2 challenge and was given a short Rust program. On attempting to compile it, the compiler highlighted a few errors related to syntax and return statements.


Problem: The line initializing the key variable was missing a semicolon at the end.
Solution: In Rust, most statements must end with a semicolon. I added ; to the end of the let key = String::from("...") line.


Problem: The code attempted to use ret instead of Rust’s correct return syntax.
Solution: I replaced ret with return; to ensure the function exits properly.


Problem: The println! macro tried to print the result of String::from_utf8_lossy(...) but didn’t include a {} placeholder.
Solution: I added "{}" as the format string to properly include the variable in the output.

After making these fixes, I compiled the code again. The program compiled successfully and printed the decoded flag to the terminal.

Result:
The flag was revealed successfully:
picoCTF{4r3_y0u_h4v1n5_fun_y31?}

What I Learned:

How to recognize and fix basic Rust syntax issues such as missing semicolons.

The importance of using correct return syntax (return) in Rust functions.

Correct usage of the println! macro, including formatting specifiers.

Reinforced the value of compiler error messages in helping identify and fix common mistakes quickly.

