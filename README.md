<div align="center">

## User defined string Functions \(Length and Reversal\)


</div>

### Description

This program explains beginners to write functions to find the length of a string and to reverse a string without using the in-built functions strlen and strrev. Rate the code if you like it and also comment on the code.
 
### More Info
 
A word (string)

Basics of pointers

Its length and the reversed string.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Karthik A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/karthik-a.md)
**Level**          |Beginner
**User Rating**    |3.0 (9 globes from 3 users)
**Compatibility**  |C, Borland C\+\+
**Category**       |[Strings](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/strings__3-26.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/karthik-a-user-defined-string-functions-length-and-reversal__3-9588/archive/master.zip)

### API Declarations

```
#include&lt;stdio&gt;
#include&lt;conio&gt;
```


### Source Code

```
/* This program explains string functions strlen and strrev without the use of in-built functions*/
#include<stdio>
#include<conio>
/* Function to return the length of a string */
int length(char *base)    //The argument to this function is the base address of the input string
{
int ct=0;      //Counters for accessing the string and count
while(*(base+ct)!='\0')    //Increment the counter if '\0' is not encountered
{
ct++;
}
return ct;       //Return the length
}
/*Function to reverse the string */
void reverse(char *base,int length) //There are two arguments 1. Base address
{         //2. Length of the string obtained by using length function
int i;
for(i=length-1;i>=0;i--)
{         //i is stored with the length of the string and now can be accessed in the reverse
printf("%c",*(base+i));    //The string is printed using pointers with base address and the counter 'i'
}
}
void main()
{
char str[20];
int len;
clrscr();
printf("\n Enter a word:");
scanf("%s",str);
printf("\n Call the function length with the parameter as the string's base address");
len=length(str);    //Call the function length with the parameter as the string's base address
printf("\n The length is %d",len);
getch();
/* Strrev */
printf("\n The function reverse is called with two param 1. base address and 2. length");
printf("\n");
reverse(str,len);    //The function reverse is called with two param 1. base address and 2. length
getch();
}
```

