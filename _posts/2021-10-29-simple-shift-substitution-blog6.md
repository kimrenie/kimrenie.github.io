---
layout: post
title:  "6. Simple Shift Substitution"
date:   2021-10-29 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 35%}</style></html>

# What is a Cipher

A cipher is a type of encryption technology that replaces original letters with other letters, numbers, and symbols to hide words or text. The words after encryption/decryption are referred to as `encrypted text`. The term `cipher` is a term that refers to encrypted/modified text and is commonly referred to as `ciphertext`. This word came about because it contrasts the regular term `plaintext` which is a message that is readable by any user.

A cipher facilitates *private* communication and an example of its use can be seen in credit card transactions or email interactions. The usage of an encrypted message is beneficial because it cannot be read if accessed by an unauthorized user. 

There are multiple different kinds of ciphers such as:
- Ceasar Cipher
- Monoalphabetic Cipher
- Homophonic Substitution Cipher
- Polygram Substitution Cipher
- Polyalphabetic Substitution Cipher
- Playfair Cipher
- Hill Cipher
- Substitution Cipher

We will be going over the substitution cipher today.

# Simple Substitution Cipher

The most commonly used cipher is the simple substitution cipher because of how simple it is! 

The algorithm that the caesar cipher follows is relatively simple:
1. The first character of our plaintext string is read
2. The alphabetic letter is replaced according to a provided key that is only accessible by the sender and the receiver
3. This process is repeated for every following character in the string
4. The new string is generated and outputted

![cipher-key](/images/cipher-key.jpeg)

The key that is used to move the characters in the substitution algorithm can also be referred  to as the shift. This can be seen visually as a shift of any integer will move our selected character over that many times. For example, if the selected character is the letter 'G' and the algorithm calls for a shift of 6, then the encrypted  letter would produce the alphabetic  character 'M'.

# References

Cipher [https://en.wikipedia.org/wiki/Cipher](https://en.wikipedia.org/wiki/Cipher)