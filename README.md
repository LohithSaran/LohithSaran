
// Stack ex 4

#include <stdio.h>
#include <limits.h>
#include <stdbool.h>

#define STACK_SIZE 5
#define EMPTY (-1)
#define STACKEMPTY INT_MIN

int stack[STACK_SIZE];
int top=EMPTY;

bool push(int value) 
{

	if(top>=STACK_SIZE-1)
		return false;
	
	top++;
	stack[top]=value;
	return true;
}

int pop() {
	if(top == EMPTY)
		return STACKEMPTY;

	int result = stack[top];
	top--;
	return result;
}

int main() {

	push(1);
	push(2);
	push(3);
	push(4);

	int t; 

	while ((t=pop())!=STACKEMPTY)
	{
		printf("t = %d ",t);
		printf("\n");
	}
	
	
}
