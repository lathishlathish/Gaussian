# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display.

## Program:
```
Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: LATHISH KANNA M
RegisterNumber: 212222230073
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in  range(n):
    print('X%d = %0.2f'%(i,x[i]),end = ' ') 
```
## Output:

![image](https://github.com/lathishlathish/Gaussian/assets/120359170/0086db69-fa24-42cb-8aff-4635371b1bac)
![image](https://github.com/lathishlathish/Gaussian/assets/120359170/f63a1d3a-82c4-4879-b7b2-5d54349fb62b)
![image](https://github.com/lathishlathish/Gaussian/assets/120359170/d0577d40-8c8d-4ba6-ba54-80f6141a29c6)
```

 

```
## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.
```
