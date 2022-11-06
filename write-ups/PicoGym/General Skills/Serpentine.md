# Serpentine (General Skills, 100p)
When I run the script and I choose option b it says to look in the source code. I found there the function `print_flag()` and I modify the source code so that when
I choose b option the program executes the function.
```python
if choice == 'a':
  print_encouragement()
  
elif choice == 'b':
  print_flag()

elif choice == 'c':
  sys.exit(0)
```
So I run the script again and choose option b and I get the flag.

Flag: `picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}`
