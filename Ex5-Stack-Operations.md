# Ex5 Stack Operations
## DATE:
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm
1.Initialize an empty stack to hold operators.
2.Read the infix expression from left to right.
3.If an operand is found, add it directly to the postfix output.
4.If an operator is found, pop from the stack until the top has lower precedence, then push the operator.
5.After the expression ends, pop all remaining operators from the stack to the postfix output.  
## Program:
~~~
Program to find and display the priority of the operator in the given Postfix expression
Developed by: RAKSHITHA K
RegisterNumber:  212223110039


#include<stdio.h>
#include<string.h>
#include<ctype.h>

int s[50];
int top=0;

void push(int ch)
{
	top++;
	s[top]=ch;
}

int pop()
{
	int ch;
	ch=s[top];
	top=top-1;
	return(ch);
}

void evalprefix(char p[50])
{
    int a,b,c,i;
    for(i=strlen(p)-1;i>=0;i--)
    {
        if(p[i]=='-')
        {
            a=pop();
            b=pop();
            c=a-b;
            push(c);
        }
        else if(p[i]=='*')
        {
            a=pop();
            b=pop();
            c=a*b;
            push(c);
        }
        else{
            push(p[i]-48);
        }
    }
    printf("%d",pop());
}




~~~

## Output:
![image](https://github.com/user-attachments/assets/d0640e4d-df5d-4016-9c40-27ca1cffcade)

## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
