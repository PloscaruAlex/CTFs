# Magikarp Ground Mission (General Skills, 30p)
I connect to the machine with:
```
$ssh ctf-player@venus.picoctf.net -p 51161
```
Using the password `b60940ca`.

Once I am inside, I list the files and I read them:
```
$ ls
1of3.flag.txt  instructions-to-2of3.txt
$ cat 1of3.flag.txt 
picoCTF{xxsh_
$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
```
I go to /, and I see the second part of the flag and a file which tells me to go to the home directory.
```
$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
```
Then I get the third part of the flag:
```
$ cat 3of3.flag.txt 
c1754242}
```
And I get my flag.

Flag: `picoCTF{xxsh_0ut_0f_\/\/4t3r_c1754242}`
