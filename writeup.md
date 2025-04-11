### Name : Mod 26

#### Description :  Cryptography can be easy, do you know what ROT13 is? cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_GYpXOHqX}

Using a simple ROT13 decipher reveals the flag.

**Flag** : picoCTF{next_time_I'll_try_2_rounds_of_rot13_TLcKBUdK}

--- 

### Name  : The Numbers

####  Description : The numbers... what do they mean?

The png has numbers and when you convert those numbers to their respective alphabet positions, you get the flag.

**Flag** : PicoCTF{THENUMBERSMASON}

--- 

### Name : 13

#### Description : Cryptography can be easy, do you know what ROT13 is? cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}

Using a simple ROT13 decipher reveals the flag.

**Flag** : picoCTF{not_too_bad_of_a_problem}

---
### Name : interencdec

#### Description : Can you get the real meaning from this file. Download the file here. 

When you can download the flag, you can see its base64 encoded, so decoding it twice will generate ROT ciphered code.dicphering it using an ROT decipher will reveal the flag.

**Flag** : picoCTF{caesar_d6cr2pt6d_123d5602}

--- 

### Name : hashcrack

#### Description : A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server? Access the server using nc verbal-sleep.picoctf.net 51759

Accessing the server using netcat will reveal three hashes sequential which can be cracked using crackstation hence revealing the flag.

**Flag** : picoCTF{UseStr0nG_h@shEs_&PaSswDs!_ce730f64}

---
### Name : EVEN RSA CAN BE BROKEN???

#### Description : This service provides you an encrypted flag. Can you decrypt it with just N & e? Connect to the program with netcat: $ nc verbal-sleep.picoctf.net 60565 The program's source code can be downloaded here.

Accessing the server using netcat gives the E value, the cipher and the N value. put them in a rsa cipher calculator and you get the flag.

**Flag** : picoCTF{tw0_1$_pr!m3f81fef0a}


---
### Name : Easy1

#### Description :  The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help UFJKXQZQUNB with the key of SOLVECRYPTO. Can you use this table to solve it?

its Vigenere Cipher, using a vigenere cipher decoder online will reveal the flag.

**Flag** : picoCTF{CRYPTOISFUN}

---

### Name : caesar

#### Description : Decrypt this message.

Downloading the file reveals a ceaser ciphered text , run it in the decipher tool reveals the flag at 3 shift.

**Flag**: picoCTF{crossingtherubiconvfhsjkou}

---
### Name : Mind your Ps and Qs

#### Description : In RSA, a small e value can be problematic, but what about N? Can you decrypt this? values

Downloading the file gets the E , N and cipher message, put them in a rsa cipher calculator and you get the flag. 

**Flag** : picoCTF{sma11_N_n0_g0od_73918962}

---
### Name : rotation

#### Description :  You will find the flag after decrypting this file Download the encrypted flag here.

Simple ROT8 cipher, use a rot8 decipher to get the flag.

**Flag** : picoCTF{r2tat3on_d5crypt5d_6c93f7b2}

---

### Name :  Vigenere

#### Description :  Can you decrypt this message? Decrypt this message using this key "CYLAB".

its Vigenere Cipher, using a vigenere cipher decoder online will reveal the flag.

**Flag** : picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}

---
### Name : substitution0

#### Description :  A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher? Download the message here.

when you open the downloaded flag , you can see substituted alphabet order, insert that order into a substitution decipher with the subsituted flag as the code and you get the flag.

**Flag** : picoCTF{5UB5717U710N_3V0LU710N_03055505}


---

### Name : basic-mod1

#### Description :  We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message here. Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. picoCTF{decrypted_message})



```

def decrypt_mod37(filepath):
    # Define the character set
    char_set = [chr(i) for i in range(ord('A'), ord('Z') + 1)] + [str(i) for i in range(10)] + ['_']
    
    # Read the file
    with open(filepath, 'r') as file:
        content = file.read().strip()
        numbers = list(map(int, content.split()))

    # Map each number mod 37 to corresponding character
    decrypted = ''.join(char_set[num % 37] for num in numbers)

    # Wrap with flag format
    flag = f"picoCTF{{{decrypted}}}"
    print(flag)

decrypt_mod37('message.txt')  

```

**Flag** : picoCTF{R0UND_N_R0UND_79C18FB3}


---

### Name : substitution1

#### Description :  A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again. Download the message here.

I used an online substitution cipher decoder for this one. I started with the default guesses and then changed the letter mappings using my intuition. I looked for common patterns and words to figure out the right letters. After a few tweaks, the message made sense and I got the flag.

**Flag** : picoCTF{FR3QU3NCY_4774CK5_4R3_C001_7AA384BC

---
### Name : credstuff

#### Description :  We found a leak of a blackmarket website's login credentials. Can you find the password of the user cultiris and successfully decrypt it? Download the leak here. The first user in usernames.txt corresponds to the first password in passwords.txt. The second user corresponds to the second password, and so on .

identify the password row corresponding to username row to find a cipher. I put that into a caesar cipher brute force tool (therese) to reveal the flag.

**Flag** :  picoCTF{C7r1F_54V35_71M3}

--- 

### Name : rail-fence

#### Description : A type of transposition cipher is the rail fence cipher, which is described here. Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? Download the message here. Put the decoded message in the picoCTF flag format, picoCTF{decoded_message}.


Rail fence cipher, use a decoder with 4 rows and keep the punctations and spaces to reveal the flag.

**Flag** : picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7}

--- 

### Name : Flags

#### Description :  What do the flags mean?

They are maritime signal flags where each flag represents a letter or number . search for the mappings online and align them to dicpher the flag.

**Flag** : picoCTF{f1ag5and5tuff}

--- 
### Name : Mr-Worldwide

#### Description : A musician left us a message. What's it mean?

They resemble coordinates of multiple locations and they are , combinding the first letter of every coordinate reveals the flag.

**Flag** : picoCTF{kodiak_alaska}

--- 

### Name : Tapping

#### Description : Theres tapping coming in from the wires. What's it saying nc jupiter.challenges.picoctf.org 9422.

The server returns a morse code string and using a morse code decoder reveals the flag. 

**Flag** : picoCTF{m0rs3c0d31sfun2683824610}

--- 

### Name : ReadMyCert

#### Description : How about we take you on an adventure on exploring certificate signing requests Take a look at this CSR file here.

A CSR (Certificate Signing Request) is a specially formatted encrypted message sent from a Secure Sockets Layer (SSL) digital certificate applicant to a certificate authority (CA). The CSR validates the information the CA requires to issue a certificate. Use a csr file reader to reveal the flag in its content tab. 

**Flag** : picoCTF{read_mycert_57f58832}

--- 

### Name : la cifra de

#### Description :  I found this cipher in an old book. Can you figure out what it says? Connect with nc jupiter.challenges.picoctf.org 58295.

its Vigenere Cipher, using a vigenere cipher decoder online will reveal the flag.

**Flag** : picoCTF{b311a50_0r_v1gn3r3_c1ph3ra966878a}

--- 
### Name : transposition-trial

#### Description :  Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message. Download the corrupted message here.


With some intiution , we can say that the message is "The flag is picoCTF{...}" . Now, connect the first three letters of the message with the "the" and see in which order they are shuffled , do that shuffle for the rest of the message to get the flag. 

**Flag** : picoCTF{7R4N P051N6_15_3XP3N51V3_109AB02E} 

--- 

### Name :  substitution2

#### Description :  It seems that another encrypted message has been intercepted. The encryptor seems to have learned their lesson though and now there isn't any punctuation! Can you still crack the cipher? Download the message here.

I used an online substitution cipher decoder for this one. I started with the default guesses and then changed the letter mappings using my intuition. I looked for common patterns and words to figure out the right letters. After a few tweaks, the message made sense and I got the flag.

**Flag** : picoCTF{N6R4M_4N41Y515_15_73D10U5_702F03FC}

--- 

### Name : HideToSee

#### Description :  How about some hide and seek heh? Look at this image here.

We can see that the image has atbash cypher in it, the hint says to extract the image. so extracting the image using `steghide` gets a encrypted.txt file, using an atbash decipher tool for the text inside the file reveals the flag. 

**Flag** : picoCTF{atbash_crack_7142fde9}

--- 
### Name : Dachshund Attacks

#### Description : What if d is too small? Connect with nc mercury.picoctf.net 31133.

Accessing the server using netcat gives the E value, the cipher and the N value. put them in a rsa cipher calculator and you get the flag.

**Flag** : picoCTF{proving_wiener_1146084}

--- 

### Name : basic-mod2

#### Description : A new modular challenge! Download the message here. Take each number mod 41 and find the modular inverse for the result. Then map to the following character set: 1-26 are the alphabet, 27-36 are the decimal digits, and 37 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. picoCTF{decrypted_message})

finding modular inverse of 41 for each number results in :

` 28 14 22 30 18 32 30 12 25 37 8 31 18 4 37 35 1 27 32 4 36 30 36`

Using a a1z26 cipher tool with custom alphabet supporting numbers and hyphen reveals the flag.

**Flag** : picoCTF{1nv3r53ly_h4rd_8a05d939}

--- 

### Name : john_pollard

#### Description : Sometimes RSA certificates are breakable

Analyzing the rsa cert using openssl gives a modulos. Inserting that modulos into a factoriser gives p and q.combine them to get the flag.


**Flag** : picoCTF{73176001,67867967}


--- 
### Name : waves over lambda

####  Description :  We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with nc jupiter.challenges.picoctf.org 39894.

`nc jupiter.challenges.picoctf.org 39894. | xsel --clipboard` to get the cipher in clipboard and use a substitution cipher solver to get the flag.its not in the usual format of picoCTF{**FLAG**} .


**Flag** : frequency_is_c_over_lambda_agflcgtyue

---

### New Caesar

#### Description : We found a brand new type of encryption, can you break the secret code? (Wrap with picoCTF{}) dcebcmebecamcmanaedbacdaanafagapdaaoabaaafdbapdpaaapadanandcafaadbdaapdpandcac 

The message was encrypted by turning each character into two letters from 'a' to 'p' using a custom base16 system, then applying a Caesar cipher shift (mod 16) with a single-letter key. To decode it, we tried all 16 possible shifts, then turned each letter pair back into a character by converting them to numbers (0–15), combining them into a byte, and using chr() to get the original text.

**Flag** : picoCTF{et_tu?_07d5c0892c1438d2b32600e83dc2b0e5}

--- 

### Name : morse-code

#### Description : Morse code is well known. Can you decrypt this? Download the file here. Wrap your answer with picoCTF{}, put underscores in place of pauses, and use all lowercase.

Upload the morse code file into a morse code decryper and you get the flag.

**Flag** : picoCTF{WH47_H47H_90D_W20U9H7}

--- 

### Pixelated

#### Description :  I have these 2 images, can you make a flag out of them? scrambled1.png scrambled2.png

Doing a bitwise xor between the images and tuning the final image a bit reveals the flag. 

**Flag** : picoCTF{1b867c3e}

---