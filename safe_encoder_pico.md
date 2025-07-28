Challenge :Safe Opener 

Challenge Overview
You are given a Java program (SafeOpener.java) that simulates a safe with a password lock. Your goal is to figure out the correct password to open the safe and get the flag.

Step by step process:
1. Open the java file
2. analyze the code
3. you will find a value "cGwzYXMzX2wzdF9tM18xbnQwX3RoM19zYWYz"
4. code hints at base64
5. open base64 decode and enter value
6. copy the converted value and enclose it between picoCTF{..}
7. voila, flag retrieved


Summary:
The program compares Base64(input) to a Base64 string.
Decode that Base64 string to find the actual password.
Input that password to open the safe and get the flag.