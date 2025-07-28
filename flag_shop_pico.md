Challenge: flag_shop – Writeup


Analysis of the Source Code
The program simulates a text-based shop where the user starts with $1100 and can:

View their balance
Buy flags
Exit

Available Flags:
Option 1: "Definitely not the flag Flag" — costs $900 each
Option 2: "1337 Flag" — costs $100,000
If you manage to buy it, the program reads and prints the content of flag.txt, which contains the real flag.

But there's a problem:

The starting balance is only $1100, and you can't normally afford the 1337 flag.

Vulnerability
In the flag purchase logic:

int total_cost = 0;
total_cost = 900 * number_flags;
number_flags is user-controlled.

int is a 32-bit signed integer, so the maximum value it can store is 2,147,483,647.

If 900 * number_flags exceeds that, it causes an integer overflow, wrapping the value around into a negative or very low positive number.

Then this check is made:

if(total_cost <= account_balance)
If total_cost is negative (due to overflow), the condition will pass. Then:


account_balance = account_balance - total_cost;
Subtracting a negative value will increase the balance.

Exploit Strategy:
Buy a huge number of cheap flags to overflow the total cost.
Trigger a negative cost, which causes a balance increase.
Use the new balance to buy the 1337 flag and get the real flag.

Exploiting It – Step-by-Step
Run the binary locally or on the remote server if provided.

Step 1: Buy a Huge Quantity
Choose menu option 2 (Buy flags)
Choose sub-option 1 (Knockoff flag)
Enter a large value such as:

number_flags = 2386093
900 * 2386093 = 2,147,483,700 → just above INT_MAX → integer overflow
The total cost becomes negative, allowing the check to pass, and your account balance becomes huge (e.g., $2,146,600 or more).

Step 2: Buy the Real Flag
Choose menu option 2 again
Choose sub-option 2 (1337 flag)

Enter 1 to buy it

You now have enough money to buy it, 
and the program prints your flag

VOILA !



What I learned:
- look at the source code thoroughly and check variables which could be exploited
- int is 32 bit signed !