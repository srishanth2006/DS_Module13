# Ex4 Evaluation of prefix expression
## DATE: 24.04.2025
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm
1. Start the program.
2. Include the required libraries.
3. Define the functions to handle pop and push operations of the stack.
4. Construct a function to evaluate the prefix expression using stack and print the output.
5. End the program.

## Program:
```
/*
Program to evaluate the given prefix expression
Developed by: SRISHANTH J
RegisterNumber: 212223240160
*/

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

void evalprefix(char prefix[50])
{
    	int i,a,b,c;
    	for(i=strlen(prefix)-1;i>=0;i--)
    	{
    	    if(isdigit(prefix[i]))
    	    {
    	        push(prefix[i]-'0');
    	    }
    	    else
    	    {
    	        b=pop();
    	        a=pop();
    	        if(prefix[i]=='+')
    	        {
    	            c=b+a;
    	            push(c);
    	        }
    	        else if(prefix[i]=='*')
    	        {
    	            c=b*a;
    	            push(c);
    	        }
    	        else if(prefix[i]=='-')
    	        {
    	            c=b-a;
    	            push(c);
    	        }
    	    }
    	}
    	printf("%d",pop());
}

int  main()
{
    char prefix[20]="*+69-31*+";
    evalprefix(prefix);
	return 0;
}

```

## Output:
![Screenshot 2025-04-30 091756](https://github.com/user-attachments/assets/e474b273-da3b-485a-b9b9-4311fdcbbb9a)


## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
