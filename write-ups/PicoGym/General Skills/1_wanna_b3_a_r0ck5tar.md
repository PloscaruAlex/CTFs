# 1_wanna_b3_a_r0ck5tar (General Skills, 350p)
This challenge is a follow-up to mus1c, which means this is a program written in rockstar programming language, but when I try to put the 'lyrics' into the online interpretor
it expects an input so I try to find a way to convert the rockstar code into something else.

I try my luck with python, with a script that converts code fetched from the [rockstar programming language website](https://codewithrockstar.com/code):
```
$python3 /home/kali/.local/bin/rockstar-py -i lyrics.txt -o rock.py
```
I get the next program:
```python
Rocknroll = True
Silence = False
a_guitar = 10
Tommy = 44
Music = 170
the_music = input()
if the_music == a_guitar:
    print("Keep on rocking!")
    the_rhythm = input()
    if the_rhythm - Music == False:
        Tommy = 66
        print(Tommy!)
        Music = 79
        Jamming = 78
        print(Music!)
        print(Jamming!)
        Tommy = 74
        print(Tommy!)
        They are dazzled audiences
        print(it!)
        Rock = 86
        print(it!)
        Tommy = 73
        print(it!)
        break
        print("Bring on the rock!")
        Else print("That ain't it, Chief")
        break
```
And it is not quite correct, but I can see some numbers which I think represent ascii.

There is some nonsense in this program and I ignore it, I focus just on the numbers I am interested in.
I notice there is one line which didn't quite compute well: `They are dazzled audiences`. I looked in the rockstar programming language manual and I try to understand
this line, and I figure it out to be `the_last_variable_used = 79`. 

So when I look at just the numbers in the right range I see:
```
Tommy = 66
Music = 79
Jamming = 78
Tommy = 74
the_last_variable_used = 79
Rock = 86
Tommy = 73
```
And they translate in ascii to: `BONJOVI`. I wrap this in flag format and I get the flag.

Flag: `picoCTF{BONJOVI}`
