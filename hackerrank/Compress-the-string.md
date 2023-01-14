# Compress the String

### Problem:

You are given a string **S**. Suppose a character '**c**' occurs consecutively **x** times in the string. 
Replace these consecutive occurrences of the character '**c**' with **(x, c)** in the string.

### Input Format

A single line of input consisting of the string **S**.

### Output Format

A single line of output consisting of the modified string.

### Constraints

All the characters of **S** denote integers between **0** and **9**.
![image](https://user-images.githubusercontent.com/48019306/212496936-48ccf265-2068-42a5-9688-5f3102ded290.png)

### My answer: 

````python
s = list(input()) + [-1]
x = 1
l = ''
for i in range(len(s) - 1):
    if s[i] == s[i + 1]:
        x += 1
    else:
        l = l + '({}, {}) '.format(x, s[i])
        x = 1
print(l)
````
