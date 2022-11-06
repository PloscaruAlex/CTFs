# PW Crack 3 (General Skills, 100p)
The python script gets the hash of the user input and compares it to the correct hash in the hash file.

To get the correct password I need to get the md5 hash of every possible password:
```python
import hashlib

x = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]

for i in x:
    print(i + ' : ' + hashlib.md5(i.encode()).hexdigest())
```
```
6997 : c9049d2a46feb0ae2de6b0636f32ea0d
3ac8 : 9648ae234bd327d686f9d684342070cd
f0ac : ee7751a05dead01a36378729fd0c204e
4b17 : 03078179ea3e83075620b5ed18f95894
ec27 : f41719388902e51c111a5778b4669fcb
4e66 : cd6925a9d53245b106a97e303f5e2ef7
865e : 1b18e1316f9218cc5b053e1cea28e02e
```
If I try to cat the hash file I can't see anything because it is written in hex, so I read it with xxd:
```
$xxd level3.hash.bin            
00000000: 0307 8179 ea3e 8307 5620 b5ed 18f9 5894  ...y.>..V ....X.
```
That is the correct hash, the one which starts with `03078179...`. And if I run the challenge script in the same directory with the encrypted text file,
with the corresponding password to the correct hash, I get the flag.
```
$python3 level3.py           
Please enter correct password for flag: 4b17
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
```
Flag: `picoCTF{m45h_fl1ng1ng_2b072a90}`
