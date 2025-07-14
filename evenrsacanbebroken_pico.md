Challenge: even rsa can be broken????

Objective:
Given an RSA public key (N, e) and a ciphertext, the goal was to decrypt the message and recover the plaintext flag, possibly due to weak or small key parameters.

Steps Taken:
- Noticed that N was small enough to factor in a reasonable time.
- Used online factorization tool to factor N into its prime components p and q.
- Calculated φ(N) = (p - 1)(q - 1).
- Computed the private key exponent d = inverse of e mod φ(N).
- Used the RSA decryption formula: plaintext = ciphertext^d mod N.
- The decrypted result was converted to a readable string or directly matched picoCTF format.

Result:
Successfully decrypted the ciphertext and retrieved the plaintext flag. Submitted as picoCTF{...}

What I Learned:
- RSA with small key sizes can be broken by direct factorization.
- Understanding modular arithmetic and RSA structure is crucial for crypto-based CTFs.
- How to implement simple RSA decryption in Python or using online tools.
