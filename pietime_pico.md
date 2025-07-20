Challenge : PIE TIME

Objective
Capture the flag by exploiting a function-pointer-based jump in a PIE (Position Independent Executable) binary. The program prints main()'s runtime address, reads a user-supplied hex address, casts it as a function pointer, and jumps there. You need to redirect execution to the win() function to reveal the flag—even though PIE randomizes addresses on each run.

Key Ideas
PIE + ASLR ensures the binary loads at different addresses each time, but relative offsets between functions remain constant 
The program leaks the runtime address of main(), which serves as our anchor point.
Since win() is located at a fixed offset from main() in the binary, we can compute its current address as:

win_addr = main_addr - OFFSET
The offset was determined to be 0x96 (150 decimal) 

Step-by-Step

1. Inspect Source/Binary
The binary prints &main, then prompts:

scanf("%lx", &val);
((void (*)())val)()

No overflow or format string—simple address jump 


2. Find the Offset

gdb ./vuln
disassemble main
disassemble win
Typical results:

main: 0x133d
win:  0x12a7

Offset = 0x133d - 0x12a7 = 0x96 


3. Attack the Remote Binary

nc rescued-float.picoctf.net PORT
# The server prints: Address of main: 0xAAAABBBBCCCC
win_addr = main_addr - 0x96
# Input hex(win_addr) when prompted
The program jumps to win(), prints “You won!” and outputs the flag 


✅ Result
By dynamically calculating win()’s address from the leaked main() address and the constant offset, execution is redirected to win(), allowing the flag to be retrieved reliably.

What I Learned
-PIE & ASLR randomize load addresses but preserve relative function offsets
-Leaking a single address enables full control via computed offsets
-Simple function-pointer jumps can become powerful when combined with dynamic address leaks