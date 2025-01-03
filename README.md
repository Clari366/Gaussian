# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm. 
1. Import numpy and sys to use the built -in functions for calculations
2. Get the size of the matrix (order) from the user and initialize an empty matrix and vector 
3. Using for loop get elements of the matrix and vector user
4. using another for loop to take each element in the matrix and solve in row echelon form 
5. perform back subtitution and print the values with two decimal places
6. End the program


## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: 
RegisterNumber: 
*/
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Janani.S
RegisterNumber: 24901127
'''
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
#Back substitution
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")


## Output:
![gaussian elimination]()

![Screenshot from 2024-12-26 11-55-21](https://github.com/user-attachments/assets/d1053fa5-80b1-4d04-b3f1-c0724071b0d7)





## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

