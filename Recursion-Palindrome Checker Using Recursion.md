# 🔁 Recursion:nested Recursion in Python

## 🎯 AIM:
To write a Python program to display all the positive numbers in reverse order with a difference 2 from 'N'  using nested recursion

---

## 🧠 ALGORITHM:

1. Start the function fun(n).
2. If n equals 1, return 1.
3. If n equals 0, return 0.
4. Otherwise, print the current value of n without moving to the next line.
5. Call fun(n - 2) and pass its result again into fun().
6. Output the final returned value from the nested recursive calls.
---

## 💻 PROGRAM:
~~~
def fun(n):
    if n==1:
        return 1
    elif n==0:
        return 0
    else:
        print(n,end=" ")
        return(fun(fun(n-2)))
        
n=int(input())
print(fun(n))
~~~

## OUTPUT
<img width="356" height="166" alt="image" src="https://github.com/user-attachments/assets/ef975f79-7672-4d3f-b99f-2364fdcfeb64" />


## RESULT
Thus the Nested recursion is verified.
