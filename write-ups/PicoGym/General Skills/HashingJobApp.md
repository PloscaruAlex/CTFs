# HashingJobApp (General Skills, 100p)
I had to get the hash of every word sent and I didn't want to do it by hand so I wrote a python script.

I had to parse the actual words between quotes and get the md5 hash and send it back, until I get the flag.
```python
import pwn
import hashlib
io = pwn.remote('saturn.picoctf.net','57689') #connect to the address
while True:
    x = io.recvuntil(b'\n') #Please md5 hash the text between quotes, excluding the quotes:
    print(x)
    if b'pico' in x:
        print(x)
        io.close()
        break
    print(io.recvuntil(b'\n')) #Answer:
    a = x.find(39)
    b = x.find(39, a + 1)
    y = x[a + 1:b] #the actual words between quotes
    io.send(hashlib.md5(y).hexdigest().encode() + b'\n') #sending the md5 hash
    print(io.recvuntil(b'\n')) #md5 hash echoed back
    print(io.recvuntil(b'\n')) #Correct.
```
Flag: `picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}`
