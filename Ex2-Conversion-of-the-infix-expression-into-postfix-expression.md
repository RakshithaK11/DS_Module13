# Ex2 Conversion of the infix expression into postfix expression
## DATE:
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1.Scan the expression from left to right.
2.If operand, add it directly to the output.
3.If ‘(’, push it to the stack; if ‘)’, pop until ‘(’.
4.If operator, pop operators with higher or equal precedence from stack, then push current operator.
5.After scan ends, pop and add all remaining operators from the stack to output.
## Program:
~~~
Program to convert the infix expression into postfix expression
Developed by: RAKSHITHA K
RegisterNumber: 212223110039  

char IntoPost(char *exp)
{
    char *e,x;
    e = exp;
  while(*e != '\0')
    {
        if(isalnum(*e))
            printf("%c",*e);
        else if(*e == '(')
            push(*e);
        else if(*e == ')')
        {
            while((x = pop()) != '(')
                printf("%c", x);
        }
        else
        {
            while(priority(stack[top]) >= priority(*e))
                printf("%c",pop());
            push(*e);
        }
        e++;
    }
    
    while(top != -1)
    {
        printf("%c",pop());
    } 
    return 1;
}
~~~

## Output:
![image](https://github.com/user-attachments/assets/569ccef3-d61c-4cc3-87e8-269a8d52fa99)

## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
