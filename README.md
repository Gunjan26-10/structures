# structures
Developed by gunjan narkhede
#include<stdio.h>
struct employee
{
	int number;
	char name[50];
	char dept[50];
	int salary;
}details[20];
int displayno(int n)
{
	int i;
	for(i=0;i<n;i++)
	{
		printf("%d\n",details[i].number);
	}
	return 0;
}
int displayname(int n)
{
	int i;
	for(i=0;i<n;i++)
	{
		printf("%s\n",details[i].name);
	}
	return 0;
}
int displaydept(int n)
{
	int i;
	for(i=0;i<n;i++)
	{
		printf("%s\n",details[i].dept);
	}
	return 0;
}
int displaysalary(int n)
{
	int i;
	for(i=0;i<n;i++)
	{
		printf("%d\n",details[i].salary);
	}
	return 0;
}	
int main()
{
	int n,p,i;
	printf("enter the number of employees whose details are to be added:");
	scanf("%d",&n);
	for(i=0;i<n;i++)
	{
	printf("enter employee number,name,department,salary:");
	scanf("%d %s %s %d",&details[i].number,details[i].name,details[i].dept,&details[i].salary);
	}
	while(1)
	{
	printf("enter 1 to display emp nos.,2 to display emp name,3 to display emp department,4 to display emp salary :");
	scanf("%d",&p);
	
	switch(p)
	{
		case(1):
		{
			displayno(n);
		    break;
		}
	    case(2):
		{
			displayname(n);
			break;
		}
		case(3):
		{
			displaydept(n);
			break;
		}
		case(4):
		{
			displaysalary(n);
			break;
		}
		default:
		{
			printf("invalid input");
	    }
    }
   }
}
