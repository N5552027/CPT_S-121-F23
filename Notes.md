// Week 1

// Week 2 

// Week 3

// Week 4

// Week 5

// Week 6 

// Week 7

#define _CRT_SECURE_NO_WARNINGS
#ifndef POINTERS_OUTPUT_PARA_H // guard code
#define POINTERS_OUTPUT_PARA_H
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

  // October 4th Function declaration
    void divide(int num, int den, double* res_ptr, int* rem_ptr);
    void roll_dice(int* die1_ptr, int* die2_ptr);

#endif

int main()
{
	// October 4th Modular Programming 
		/*
		- Defining a function that can return multiple outputs or values

		Example:
		One_function() -> char
		One_function() -> double

		Pointers: Variables that stores the address of another variable.
			- The direct value is the the value of the variable itself
			- The indirect value is the value of the variable it's attached to

			- the ampersand "&" is used in the function call to store the pointer values resulting from the function
			- '*' is the indirection or deferection operator

		The pointer should be used in the function declaration and function header when in three file format.
		*/

	int n1 = 7, n2 = 3, remainder = 0;
	double result = 0;

	divide(n1, n2, &result, &remainder);
	printf("The result of dividing %d by %d is %lf and a remainder of %d", n1, n2, result, remainder);

	int die1 = 0, die2 = 0;
	

	roll_dice(&die1, &die2);

	roll_dice(&die1, &die2);
	printf("\n\nDie one is %d and die two is %d.", die1, die2);
	printf("\nThe sum of both die is %d.", die1 + die2);


	// October 6th
	/*
	function - the call stack/the stack/system stack

		- creation of parameters and kocal variables for a given function
		- designation of the variables
		- determining when to return from a call

	A scope is anything between '{}' and local variables only apply within their scopes.
		- you can have multiple local variables with different designations but the same name 
		(not recommended as it may get confusing within larger projects)
			- EX: {double num1 = 0.0;} {int num1 = 0;}
	
	How do pointers work in a stack?
		- The address of a pointed variable is stored into the stack as blanks
			- EX: *rm_ptr will be stored as *rm_ptr in the stack. When used in the stack, the value of the pointer is
			replaced by the address of the local variable

				
	*/

	return 0;
}

    // Functions from October 4th
  void divide(int num, int den, double* res_ptr, int* rem_ptr) 
{

	// n1 will be copied over as num, n2 will be copied as den
	// the pointer refers to the variable (The variable won't have a value but it saves the address of the variable)

	*res_ptr = num / den;
	// Replaces the address of *res_ptr to the value of the result of the equation (*res_ptr is the indirect value)

	*rem_ptr = num % den;

}

void roll_dice(int* die1_ptr, int* die2_ptr) 
{

	*die1_ptr = rand() % 6 + 1;
	*die2_ptr = rand() % 6 + 1;

}

// Week 8 

// Week 9

// Week 10 

// Week 11

// Week 12 

// Week 13

// Week 14 

// Week 15

// Week 16
