# PW Crack 2 (General Skills, 100p)
When I looked in the script, the user input for the password was compared to `chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)` so I opened up the python interpretor
to see what that means:
```
$python3
>>> chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)
'39ce'
```
And that is my password for the flag. I ran the script in the same directory with the encrypted flag and there it is.
```
$python3 level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```
Flag: `picoCTF{tr45h_51ng1ng_502ec42e}`
