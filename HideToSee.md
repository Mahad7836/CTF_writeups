Challenge: HideToSee

Objective:
Cryptography

Steps Taken:
1. Downloaded Image
2. Analyzed it, found 2 circles. One had alphabet in caps going clockwise, other had alphabet in lower going anticlockwise
3. since its a crypto problem, it seems like a stegno problem
4. check the site in the image
5. found nothing there
6. used 'steghide' info atbash.jpg
7. saw a file inside 'encrypted.txt'
8. then saw online how to get to that txt file
9. steghide extract -f atbash.jpg
10. then, cat encrypted.txt
11. youll get the flag in ciphertext
12. copy it and paste it to any atbash decoder
13. flag found

What I Learned:
1. text can be stored inside images
2. the use of stegnography

