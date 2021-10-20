# Evaluation-of-Postfix-using-Stack
This concept is regarding to c programming.


#include<stdio.h>
#include<math.h>
#define MAX 70
int stack[MAX];
int top=-1;
void push(int);
int pop();
main()
{
	 int i,a,b,res;
	 char postfix[50];
	 puts("Enter the postfix Expression");
	 gets(postfix);
	 for(i=0;postfix[i]!='\0';i++)
	 {
		  switch(postfix[i])
		  {
			   case '+':
				         a=pop();
				         b=pop();
				         push(b+a);
				         break;
			   case '-':
				         a=pop();
				         b=pop();
				         push(b-a);
				         break;
			   case '*':
				         a=pop();
				         b=pop();
				         push(b*a);
				         break;
			   case '/':
				         a=pop();
				         b=pop();
				         push(b/a);
				         break;
			   case '%':
				         a=pop();
				         b=pop();
				         push(b%a);
				         break;
			   case '^':
				         a=pop();
				         b=pop();
				         push(pow(b,a));
				         break;
			   default:
				         push(postfix[i]-48);
		  }
	 }res=pop();
	 printf("Result is %d \n",res);
}
void push(int n)
{
	 top++;
	 stack[top]=n;
}
int pop()
{
	 int n=stack[top];
	 top--;
	 return n;
}



Hii, This is Ankur Aman Dash. I am a student of GITAM UNIVERSITY studying as CSBS (Computer Science and Business Systems). My aim is to be a professional Code Developer and Broker.
