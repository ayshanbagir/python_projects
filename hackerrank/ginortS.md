# ginortS

### Problem: 

You are given a string **S** containing alphanumeric characters only.

Your task is to sort the string **S** in the following manner:
- All sorted lowercase letters are ahead of uppercase letters.
- All sorted uppercase letters are ahead of digits.
- All sorted odd digits are ahead of sorted even digits.

### Input Format

A single line of input contains the string **S**.

### Constraints

0 < len(S) < 1000

### Output Format

Output the sorted string **S**.

### My answer: 

````python 
l = list(input())
low = []
up = []
odd = []
even = []
for i in l:
    if i.islower():
        low.append(i)
    elif i.isupper():
        up.append(i)
    elif i.isdigit() and int(i) % 2 == 1:
        odd.append(i)
    elif i.isdigit() and int(i) % 2 == 0:
        even.append(i)
print(''.join(sorted(low) + sorted(up) + sorted(odd) + sorted(even)))
```` 
