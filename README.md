# Automorphic-number-using-Python
Check Whether or Not the Number is an Automorphic Number in Python
Given an integer input for a number, the objective is to check whether or not the number is Automorphic or not. Therefore we’ll write a program to Check Whether or Not the Number is an Automorphic Number in Python Language.

Example
Input : 5
Output : It's an Automorphic Number.
automorphic number or not in python
Check Whether or Not the Number is an Automorphic Number in Python Language
Given an integer input as the number the objective is to check whether or not the number is an Automorphic number. To do we’ll first square the number and check if the number has been repeated in the same order of digits at the end of it’s square. For a Number to be Automorphic, it must pass the below mentioned condition

Automorphic Number
A number whose square ends with the same number is known as an Automorphic number.
Let's try and understand it even better using an example ,

Example
Input : number = 5
Output : It's an Automorphic number.
Explanation : Number = 5
Square of number = 25
as the square of the number ends with the number itself, It's an Automorphic number.
Therefore, for a number to be Automorphic it number have a square that ends with the number itself.
Automorphic NumberIn Python
Therefore, to Check Whether or Not a Number is an Automorphic Number, we write a Python Code using the following methods –

Method 1: Using Modulo Operators
Method 2: Short cut
Method 3: Using endswith() method
We’ll discuss the above-mentioned methods in detail in the upcoming sections.


Method 1: Using Modulo Operators
Working
In this method we’ll use the modulo operator to extract the last number of digits based on the length of the number input. We’ll reverse the number to match with the original numeric order of the digits.

Given an integer input as the number, we perform the following operations,

Find the square of the given integer input.
Check is the square % 10 ** len( str( number ) ) matches the original number itself.
Let’s implement the above Logic in Python Language.

Python Code
Run
number = 376
square = pow(number, 2)
mod = pow(10, len(str(number)))

# 141376 % 1000
if square % mod == number:
    print("It's an Automorphic Number")
else:
    print("It's not an Automorphic Number")
Output
it's an Automorphic Number
Method 2 : One Line Method (using Slicing)
Run
# One line method for automorphic number in python
n = 376
# n^2 = 141376 141376[-3::] = 376
print("YES" if int(str(n**2)[-len(str(n))::]) == n else "No")
Output
YES

Method 3 : Using Endswith() Method
The endswith() method returns True if the string ends with the specified value, otherwise False.
Run
num = 376
a = str(num)

num1 = num ** 2
b = str(num1)

if b.endswith(a):
    print("It's an Automorphic Number")
else:
    print("It's not an Automorphic Number")
Output
It's an Automorphic Number
