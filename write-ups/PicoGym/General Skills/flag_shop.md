# flag_shop (General Skills, 300p)
After looking at the source code, I can see that I need to do an integer overflow. I need to have a balance over `100000`, and that balance changes only when 
I buy flags from the first category, `account_balance = account_balance - total_cost`. That means that if `total_cost` is negative, `account_balance` will grow.
To make `total_cost` negative I need to give it a large enough value so it overflows into the sign bit. 

If I give the number `2147383648` it will be stored in `total_cost` as `-100000 * 9`, `-10000` being the 2's complement of that number, and that is what I need. 
Now the `account_balance` is `90001100` and I can access the flag.

Flag: `picoCTF{m0n3y_bag5_68d16363}`
