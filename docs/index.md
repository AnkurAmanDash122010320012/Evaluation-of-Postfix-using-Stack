## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/AnkurAmanDash122010320012/Evaluation-of-Postfix-using-Stack/edit/main/docs/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Ankur](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

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

//- Bulleted
//- List

//1. Numbered
//2. List

//**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Ankur Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/AnkurAmanDash122010320012/Evaluation-of-Postfix-using-Stack/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
