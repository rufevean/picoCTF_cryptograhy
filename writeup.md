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



