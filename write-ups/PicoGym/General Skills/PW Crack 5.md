# PW Crack 5 (General Skills, 100p)
There are thousands of possible passwords so I need to compute the md5 hash of each one to find the correct one.
I made a python script that does that and looks for rhe correct one and spits out the right password:
```python
import hashlib

dict = open('dictionary.txt', 'rb').readlines()
correct_pw_hash = open('level5.hash.bin', 'rb').read()

for i in dict:
    if hashlib.md5(i[:4]).digest() == correct_pw_hash:
        print(i[:4])
```
And I get the correct password: `7e5f`. I ran the challenge script in the same directory with the encrypted file and the hash file and I use the right password and I
obtain the flag.
```
$python3 level5.py 
Please enter correct password for flag: 7e5f
Welcome back... your flag, user:
picoCTF{h45h_sl1ng1ng_40f26f81}
```
Flag: `picoCTF{h45h_sl1ng1ng_40f26f81}`
