# EX 1 Display operator precedence in the infix expression.
## DATE:
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1.Scan the postfix expression from left to right.
2.If the symbol is an operand, push it onto the stack.
3.If the symbol is an operator, pop two operands from the stack.
4.Apply the operator to the operands and push the result back onto the stack.
5.After the scan, pop and print the final result from the stack.
## Program:
~~~
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: RAKSHITHA K
RegisterNumber:  212223110039

int stack[20];
int top = -1;

void push(int x)
{
    stack[++top] = x;
}

int pop()
{
    return stack[top--];
}

void evalpostfix(char *e)
{
    int n1,n2,n3,num;
    while(*e != '\0')
    {
        if(isdigit(*e))
        {
            num = *e - 48;
            push(num);
        }
        else
        {
            n1 = pop();
            n2 = pop();
            switch(*e)
            {
            case '+':
            {
                n3 = n1 + n2;
                break;
            }
          
            case '*':
            {
                n3 = n1 * n2;
                break;
            }
            }
            push(n3);
        }
        e++;
    }
    printf("%d",pop());

}



~~~

## Output:
![image](https://github.com/user-attachments/assets/5da9d900-c2c3-4536-b009-d763e687f302)

## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
