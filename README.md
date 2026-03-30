# EX 7 (A) Types of Recursion: Head Recursion in Python

## AIM:
To write a Python program to demonstrate **Head Recursion** by finding and printing the sequence based on the sum of all digits (even or odd adjusted input).

## ALGORITHM:

1. **Start**
2. Define a recursive function `fun(n)`
3. In the function:
   - Create a recursive call at the **beginning** (Head Recursion)
   - Print the result after the recursive call
4. Take input from the user
5. If input is odd, convert it to the next even number
6. Call the recursive function
7. **Stop**

## PROGRAM:
```
def fun(n):
    if n == 0:
        return
    fun(n - 2)
    print(n, end=' ')
num = int(input())
if num % 2 != 0:
    num -= 1
print()
fun(num)

```

## OUTPUT
<img width="809" height="210" alt="image" src="https://github.com/user-attachments/assets/18ae3082-8e28-4b45-a29c-6982eb511608" />

## RESULT
  Thus, the Python program to demonstrate **Head Recursion** is executed successfully.

# EX 7 (B) Recursion:Palindrome Checker Using Recursion in Python

## AIM:
To write a Python program to check whether a given string is a **palindrome** using **recursion**.

---

## ALGORITHM:

1. **Start**
2. Define a recursive function `is_palindrome(word)`
   - **Base Case:** If the string length is less than 1, return `True`
   - **Recursive Case:** If the first and last characters match, call the function recursively on the substring without first and last characters
   - Else, return `False`
3. Get input from the user
4. Call the recursive function
5. Print whether the string is a palindrome
6. **Stop**

---

## PROGRAM:
```
def is_palindrome(word):
    if len(word) < 1:
        return True
    else:
        if word[0] == word[-1]:
            return is_palindrome(word[1:-1])
        else:
            return False

word = input()

if is_palindrome(word):
    print("String is a palindrome")
else:
    print("String is not a palindrome")
```
## OUTPUT
<img width="626" height="261" alt="image" src="https://github.com/user-attachments/assets/53b70d7b-acc4-40d1-8b09-15ebeaf64132" />

## RESULT
  Thus, the Python program to check whether a given string is a **palindrome** using **recursion** has been executed successfully.

## EX 7(C) Recursion:Sum of Digits using Recursion in Python

## AIM:
To write a Python program to calculate the **sum of all digits** in a number using **recursion**.

## ALGORITHM:

1. **Start**
2. Define a recursive function `sum_digit(n)` that:
   - Returns 0 if `n <= 0` (Base Case)
   - Else, returns `n % 10 + sum_digit(n // 10)` (Recursive Case)
3. Take integer input from the user.
4. Call the recursive function and store the result.
5. Print the result.
6. **Stop**

## PROGRAM:
```
def sum_digit(n):
    if n <= 0:
        return 0
    return (n % 10) + sum_digit(n // 10)

num = int(input())
result = sum_digit(num)
print(result)

```
## OUTPUT
<img width="1172" height="212" alt="image" src="https://github.com/user-attachments/assets/46569ecf-80e0-4c44-ae5c-7cb8ca180350" />

## RESULT
  Thus, the Python program to calculate the **sum of all digits** in a number using **recursion** is executed successfully.

# EX 7 (D) Taylor Series Using Recursion in Python

## AIM:
To write a Python program to evaluate a **Taylor Series** using **recursion**, where values of `x` and `n` are taken from the user.

## ALGORITHM:

1. **Start**
2. Create variables `x` and `n`
3. Get values for `x` and `n` from the user
4. Define a recursive function `series(x, n)`
   - **Base case:** If `n == 0`, return 1
   - **Recursive case:** Return `x**n / n + series(x, n-1)`
5. Print the result
6. **Stop**

## PROGRAM:
```
def series(x, n):
    if n == 0:
        return 1
    else:
        return (x**n / n) + series(x, n - 1)
x = int(input())
n = int(input())
print(series(x, n))
```
## OUTPUT
<img width="434" height="179" alt="image" src="https://github.com/user-attachments/assets/599b630f-f928-4319-89fb-ca1553e6ea1f" />

## RESULT
  Thus, the Python program to evaluate a **Taylor Series** using **recursion** is executed successfully.

# EX 7 (E) Taylor Series:sinh(x) Evaluation using Recursion in Python

## AIM:
To write a Python program to evaluate the value of **sinh(x)** for **n terms** using recursion.

---

## ALGORITHM:

1. **Start**
2. Read input for variable `x` (angle or number)
3. Read input for variable `n` (number of terms)
4. Define a function `fact(n)`:
   - If `n <= 1`, return 1
   - Else, return `n * fact(n - 1)` (recursive factorial)
5. Define a function `sinh(x, n)`:
   - If `n == 0`, return `x`
   - Else, return `(pow(x, 2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)`
6. Call the `sinh(x, n)` function and print the result
7. **Stop**

---

## PROGRAM:
```
def fact(n):
    if n <= 1:
        return 1
    else:
        return n * fact(n - 1)
def sinh(x, n):
    if n == 0:
        return x
    else:
        return (pow(x, 2 * n + 1) / fact(2 * n + 1)) + sinh(x, n - 1)
x = float(input())
n = int(input())
print("sinh(", x, ") =", sinh(x, n))
```

## OUTPUT
<img width="398" height="157" alt="image" src="https://github.com/user-attachments/assets/da8224c3-f245-4dfb-be18-80cab0ad5246" />

## RESULT
  Thus, the Python program to evaluate the value of **sinh(x)** for **n terms** using recursion is executed successfully.
