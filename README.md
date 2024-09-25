
# stack
#include<stdio.h>
#define SIZE 5
void push(int);
void pop();
int peek();
void display();
void exit();

int stack[SIZE];
int top=-1;
int main()
{
	int choice,data,r ;
	while(1){
	
	printf("Enter 1 for Push:\n");
	printf("Enter 2 for Pop:\n");
	printf("Enter 3 for Peek:\n");
	printf("Enter 4 for Display:\n");
	printf("Enter 5 for Exit:\n");
	scanf("%d",&choice);
	switch (choice)
	{
		case 1:
			printf("Enter you data:");
			scanf("%d",&data);
			push(data);
		break;
		
			case 2:
			pop();
			break;
		
			case 3:
				r=peek();
				printf("\n%d is in top\n",r);
			break;
		
			case 4:
			display();
			break;
		
			case 5:
			printf("go to home.\n");
			return 0;
			
			default:
				printf("You have entered invalid data.");
		}
	}
	return 0;
}
	void push(int d)
	{
		if(top==SIZE-1)
		{
			printf("Stack is overflowed.\n");
			
		}
		else
		{
			top++;
			stack[top]=d;
			printf("\n Your Push is sucessfull.\n");
		}
	}
	void pop()
	{
		if (top==-1)
		{
			printf("Your stack is underflowed.\n");
		}
		else
		{
			printf(" %d is popped\n",stack[top]);
			top--;
		}
	}
	int peek()
	{
		if(top==-1)
		{
			printf("Your stack is empty.\n");
		}
		else
		{
		 return stack[top];
		}
	}
void display()
{
	if(top==-1)
	{
		printf("Your stack is empty.\n");
	}
	else
	{
		int i;
		for( i=0; i<=top; i++)
		{
		printf("\n%d\n",stack[i]);	
		
		}
	}
}
