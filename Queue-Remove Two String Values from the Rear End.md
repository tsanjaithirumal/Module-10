# Queue-Remove Two String Values from the Rear End in Python 🧵

This Python program demonstrates how to manage a list of strings and remove the last two elements (i.e., from the rear of the list).

## 🎯 Aim

To write a Python program to:
- Accept `n` string values from the user
- Remove the last two values (rear end of the list)
- Display the updated list

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` from the user (number of strings).
3. Loop `n` times:
   - Read a string input.
   - Append it to the list `q`.
4. Remove the last element using `pop()`.
5. Remove the next last element using `pop()` again.
6. Display the updated list.

##  Program:
```
q = []
n = int(input())
for _ in range(n):
    s = input()
    q.append(s)

q.pop()  
q.pop() 

print(q)
```
### Output:
<img width="505" height="533" alt="446245032-28a4bb3d-cb2f-4333-bd0a-a23f70ce72c9" src="https://github.com/user-attachments/assets/98bb5c02-289e-40c9-8eb8-608bba7fcba0" />

## Result:
Thus the output is verified
