# dice-roll.sh
Dice rolling sh script with colorized output

This is  a simple shell script. `/dev/urandom` is used for randomness. No bashism, so I expect it to run in most environment

## Usage

This script mostly understand the standard die rolling notation with a twist to add support for coloring. For instance:

```
roll 2d6+1d8g+5
```

will output the result of rolling two 6-sided dice, then the result of rolling one 8-sided die colored green and then add 5 and finally display the final sum


```
roll 3d4r+3d4y
```
Will output the result of rolling three 4-sided dice colored red and then the result of rolling three 4-sided dice again, but colored yellow and finally the final sum


The `+` in the notation can be surrounded by spaces or omitted entirely (They are just treated as argument separator). Otherwise, no white space is allowed before or after the `d` or before the color modifier

The different color modifiers supported are:

modifier|color
--------|-----
r | red
g | green
b | blue
c | cyan
m | purple(magenta)
y | yellow
