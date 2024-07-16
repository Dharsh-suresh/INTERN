# INTERN
# Caesar Cipher in Python

This project implements a simple Caesar Cipher in Python, which is a type of substitution cipher in which each letter in the plaintext is shifted a certain number of places down the alphabet.

def encrypt_func(txt, s):
    result = ""
    for i in range(len(txt)):
        char = txt[i]
        if char.isupper():
            result += chr((ord(char) + s - 64) % 26 + 65)
        else:
            result += chr((ord(char) + s - 96) % 26 + 97)
    return result
txt = "Internship"
s = 10
print("Plain text:", txt)
print("Shift pattern:", str(s))
print("Cipher:", encrypt_func(txt, s))
