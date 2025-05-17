# EX3 Implementation of Tower of Hanoi
## DATE:
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1.If n = 1, move the disk from source to destination directly.
2.Move n-1 disks from source to auxiliary, using destination as helper.
3.Move the nth (largest) disk from source to destination.
4.Move the n-1 disks from auxiliary to destination, using source as helper.
5.Repeat recursively for smaller values of n until all disks are moved. 

## Program:
~~~
/*
Program to implement Tower of Hanoi
Developed by: RAKSHITHA K
RegisterNumber: 212223110039 
#include<stdio.h>
void TOH(int n,char x,char y,char z)
{
    if(n>0)
    {
    TOH(n-1,x,z,y);
    printf("%c to %c\n",x,y);
    TOH(n-1,z,y,x);
    }
}
int main()
{
    int n=4;
    TOH(n,'A','B','C');
    
}
~~~

## Output:
![image](https://github.com/user-attachments/assets/1645e2dc-9ad0-41f0-aaed-84e9db03b046)

## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
