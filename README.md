# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Jayaharshini s
RegisterNumber: 212224100024
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
X=np.zeros(n)
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
X[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2, -1, -1):
    X[i]=a[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-a[i][j]*X[j]
    X[i]=X[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,X[i]),end=' ')

## Output:
![gaussian elimination]()
<img width="1563" height="941" alt="Screenshot 2025-09-09 101234" src="https://github.com/user-attachments/assets/991234ec-6f8e-41a1-b589-4ef37c4a23b5" />
<img width="1457" height="980" alt="Screenshot 2025-09-09 101244" src="https://github.com/user-attachments/assets/824f9bb3-ecea-4c51-8898-3002a1d6eb75" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

