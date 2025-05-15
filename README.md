#include<stdio.h>
#include<string.h>
struct book
{
int code;
char name[20];
};
int main()
{
struct book b[10];
int i,n,ch,o,l,p ;
char a[20] ;
printf("enter number of books\n");
scanf("%d",&n);
printf("enter information\n");
for(i=1;i<=n;i++)
{
printf("enter code\n");
scanf("%d",&b[i].code);
printf("enter name\n");
scanf("%s",b[i].name);
}
printf("the information is \n");
for(i=1;i<=n;i++)
{
printf("the book code is %d\n the book name is %s\n",b[i].code,b[i].name);
}
printf("which operation you want to perform?\n1.insertion\n2.delation\n3.upadation\n4.display\n");
scanf("%d",&ch);
switch(ch)
{
case 1:

printf("enter the postion which you want to perform insertion\n");
scanf("%d",&p);
printf("enter information at %d postion\n",p);
for(i=n-1;i>=p;i++)
{
b[i+1].code=b[i].code;
strcpy(b[i+1].name,b[i].name);
} 
printf("enter book code\n");
scanf("%d" ,&b[i].code);
printf("enter book name");
scanf("%s",b[i].name);
printf("the total information is\n");

 case 2 :

 printf("enter the position at which you want to delet information\n");
 scanf("%d",&l);
 printf("delate information from %d postion\n",l);

for(i=l;i<=n-1;i++)
{
b[i].code=b[i+1].code;
strcpy(b[i].name,b[i+1].name);
}
printf("the data after delation is \n");
for(i=0;i<n-1;i++)
{
printf("The book code is %d\n the book name is %s\n",b[i].code,b[i].name);
}
printf("what do you want to modify?\n 1.book code\n book name\n");
scanf("%d",&ch);
switch(ch)
{
case 1:printf("enter a code you want to modify\n");
scanf("%d",&o);
for(i=1;i<=n;i++)
{
if(o==b[i].code)
{
printf("enter new code\n");
scanf("%d",&b[i].code);
}
else 
{
printf("the book code is not present in the data base\n");
}
}
break;
case 2:printf("enter book name you want to modify\n");
scanf("%s",a); 
for(i=1;i<=n;i++)
{
if(a==b[i].name)
{
printf("enter new name\n");
scanf("%s",b[i].name);
}
else
{
printf("this book does not exist i data base\n");
}
}
break;
default:printf("wrong choice entered\n");
}
printf("the updated information is\n");
for(i=1;i<=n;i++)
{
printf("book code is %d\n book name is %s\n",b[i].code,b[i].name);
}
return 0;
}
}
 
