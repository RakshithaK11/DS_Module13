# EX 1 Display operator precedence in the infix expression.
## DATE:
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1.Start from the right of the prefix expression.
2.Scan each symbol from right to left.
3.If operand, push it onto the stack.
4.If operator, pop two operands, apply the operator, and push the result.
5.After the scan, the result will be on top of the stack—pop and print it.
## Program:
~~~
/*
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
![image](https://github.com/user-attachments/assets/a2f6527d-8d2b-4b5f-ac29-58b604a63315)

## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
