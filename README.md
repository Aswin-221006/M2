# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
#include <stdio.h>

int main() {
    int M, N, i;

    // Step 2: Prompt the user
    printf("Enter the starting value (M): ");
    scanf("%d", &M);

    printf("Enter the ending value (N): ");
    scanf("%d", &N);

    // Step 4: Loop from M to N
    printf("Even numbers from %d to %d are:\n", M, N);
    for (i = M; i <= N; i++) {
        // Step 5: Check if the current number is even
        if (i % 2 == 0) {
            // Step 6: Print the even number
            printf("%d ", i);
        }
    }

    printf("\n");
    return 0;
}

## OUTPUT:
Enter the starting value (M): 5
Enter the ending value (N): 15
Even numbers from 5 to 15 are:
6 8 10 12 14










## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
#include <stdio.h>

int main() {
    int rows, i, j;

    // Step 2: Prompt the user
    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    // Step 3: Loop through each row
    for (i = 1; i <= rows; i++) {
        // Step 4: Inner loop to print asterisks
        for (j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n"); // Move to the next line after each row
    }

    return 0;
}


## OUTPUT:
Enter the number of rows: 5
* 
* * 
* * * 
* * * * 
* * * * * 





## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
#include <stdio.h>

// Step 1: Function to perform addition
void add(int a, int b) {
    int result = a + b;
    printf("Addition result: %d\n", result);
}

// Step 1: Function to perform subtraction
void subtract(int a, int b) {
    int result = a - b;
    printf("Subtraction result: %d\n", result);
}

int main() {
    int num1, num2;

    // Step 3: Read the values of num1 and num2
    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);

    // Step 4: Call the addition and subtraction functions
    add(num1, num2);
    subtract(num1, num2);

    return 0;
}


## OUTPUT:
Enter the first number: 12
Enter the second number: 5
Addition result: 17
Subtraction result: 7






## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
#include <stdio.h>

int main() {
    int num, sum = 0, digit;

    // Step 2: Read the input number
    printf("Enter a number: ");
    scanf("%d", &num);

    // Step 3: Use a for loop to iterate through each digit of the number
    for (; num != 0; num /= 10) {
        // Step 4: Extract the rightmost digit
        digit = num % 10;

        // Step 5: If the digit is odd, add it to the sum
        if (digit % 2 != 0) {
            sum += digit;
        }
    }

    // Step 6: Print the sum of odd digits
    printf("Sum of odd digits: %d\n", sum);

    return 0;
}


## OUTPUT:
Enter a number: 123456
Sum of odd digits: 9




## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
#include <stdio.h>

// Step 2: Declare the fact() function
void fact() {
    int N, fact = 1;

    // Step 4b: Read an integer N from the user
    printf("Enter a number to find its factorial: ");
    scanf("%d", &N);

    // Step 4c: Use a for loop to calculate the factorial
    for (int i = 1; i <= N; i++) {
        fact *= i;
    }

    // Step 4d: Print the factorial value
    printf("Factorial of %d is: %d\n", N, fact);
}

int main() {


## OUTPUT:
Enter a number to find its factorial: 5
Factorial of 5 is: 120

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
