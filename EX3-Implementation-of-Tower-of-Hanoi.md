# Ex3 Implementation of Tower of Hanoi
## DATE: 24.04.2025
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1. Start the program.
2. Include the required libraries.
3. Define a recursive function to handle the tower of hanoi problem.
4. Call the defined function in the main function and print the moves.
5. End the program.

## Program:
```
/*
Program to implement Tower of Hanoi
Developed by: SRISHANTH J
RegisterNumber: 212223240160
*/

#include<stdio.h>
void TOH(int n,char x,char y,char z)
{
    if(n==1)
    {
        printf("%c to %c\n",x,y);
        return;
    }
    TOH(n-1,x,z,y);
    printf("%c to %c\n",x,y);
    TOH(n-1,z,y,x);
    
}
int main()
{
   int n=4;
   TOH(n,'A','B','C');
}
```

## Output:
![Screenshot 2025-04-30 091145](https://github.com/user-attachments/assets/841a78da-3896-4e31-8f02-8923659e40c3)



## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
