# Ex4 Evaluation of prefix expression
## DATE:
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm
1.Start scanning the prefix expression from right to left.
2.If the symbol is an operand, push it onto the stack.
3.If the symbol is an operator, pop two operands from the stack.
4.Apply the operator to the popped operands and push the result back.
5.After the scan, pop and return the final result from the stack.  

## Program:
~~~
Program to evaluate the given prefix expression
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
![image](https://github.com/user-attachments/assets/f90bc213-b8b1-4d8b-93e8-e7fa2b637570)

## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
