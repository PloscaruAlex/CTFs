# Magikarp Ground Mission (General Skills, 30p)
I connect to the machine with:
```bash
$ssh ctf-player@venus.picoctf.net -p 51161
```
Using the password `b60940ca`.
Then 
```bash
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ pwd
/home/ctf-player/drop-in
ctf-player@pico-chall$ cd ../../../
ctf-player@pico-chall$ pwd
/
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
c1754242}
ctf-player@pico-chall$ exit
```
And I get my flag.

Flag: `picoCTF{xxsh_0ut_0f_\/\/4t3r_c1754242}`
