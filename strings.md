C

#Programming Questions

##Strings

### 1.  Write a program in C to input a string and print it.
```c
#include<stdio.h>
int main()
{
   char str[100];
   scanf("%s",str);
   printf("%s",str);
}
```
### 2. Write a program in C to find the length of a string without using library functions
```c
include <stdio.h>

int main()
{
    char str[100];
    int length=0,i=0;
    scanf("%s",str);
    while(str[i]!='\0'){
    length++;
    i++;
    }
    printf("%d",length);
    return 0;
}
```
### 3. Write a program in C to separate individual characters from a string.
```c
#include <stdio.h>
int main()
{
    char str[100];
    int length=0,i=0;
    scanf("%s",str);
    for(i=0;str[i]!='\0';i++)
    printf("%c ",str[i]);
    return 0;
}
```
### 4.  Write a program in C to print individual characters of a string in reverse order.
```c
#include <stdio.h>
#include <string.h>
int main()
{
    char str[100];
    int length;
    scanf("%s",str);
    length=strlen(str);
    for(int i=length-1;i>=0;i--)
    printf("%c ",str[i]);
    return 0;
}
```
### 5. . Write a program in C to count the total number of words in a string.
```c
#include <stdio.h>

int main() {
    char str[100];
    int i = 0, words = 0;

    printf("Enter a string: ");
    fgets(str,sizeof(str),stdin);  
    while (str[i] != '\0') {
        if ((i == 0 && str[i] != ' ') || 
            (str[i] != ' ' && str[i-1] == ' ')) {
            words++;
        }
        i++;
    }
    printf("Total number of words = %d\n", words);
    return 0;
}
```
### 6.Write a program in C to compare two strings without using string library functions
```c
#include <stdio.h>

int main() {
    char str[100], str1[100];
    scanf("%s %s",str,str1);
    int i=0;
    while(str[i]!='\0'){
    if(str[i]!=str1[i]){
    printf("Not equal");
    return 0;
    }
    i++;
    }
     printf("equal");
    return 0;
}
```
### 7. Write a program in C to count the total number of alphabets, digits and special characters in a string
```c
#include <stdio.h>

int main() {
    char str[100];
    scanf("%s",str);
    int i=0,Alph=0,dig=0 ,spec=0;
    while(str[i]!='\0'){
    if(str[i]>='A' && str[i]<='Z' || (str[i]>='a' && str[i]<='z'))
    Alph++;
    else if(str[i]>='0' && str[i]<='9')
    dig++;
    else
    spec++;
    i++;
    }
    printf("Alphabets count %d\n",Alph);
    printf("Digits count %d\n",dig);
    printf("special characters  count %d",spec);
    return 0;
}
```
### 8.  Write a program in C to copy one string to another string
```c
#include <stdio.h>

int main() {
    char str[100],str1[100];
    scanf("%s",str);
    int i=0;
    while(str[i]!='\0')
    {
        str1[i]=str[i];
        i++;
    }
    str1[i]='\0';
    printf("Copying of a sring : %s",str1);
    return 0;
}
```
### 9. Write a program in C to count the total number of vowels or consonants in a string
```c
#include <stdio.h>

int main() {
    char str[100];
    scanf("%s",str);
    int i=0,vowel=0,consonant=0;
    while(str[i]!='\0')
    {
        char ch=str[i];
        if(str[i]>='A' && str[i]<='Z')
        ch=ch+32;
        if (str[i]>='a' && str[i]<='z'){
        if(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u')
        vowel++;
        else
        consonant++;
        }
    i++;
    }
    printf("Vowels count %d\n",vowel);
    printf("Consonant count %d",consonant);
    return 0;
}
```
### 10.. Write a program in C to find the maximum number of characters in a string
```c
#include <stdio.h>

int main() {
    char str[100];
    scanf("%s",str);
    int i=0;
    while(str[i]!='\0')
    {
    i++;
    }
    printf("Count %d",i);
    return 0;
}
```
### 11. Write a C program to sort a string array in ascending order.
### 12.  Write a program in C to read a string from the keyboard and sort it using bubble sort.
```c
#include <stdio.h>
#include <string.h>
int main()
{
    char str[10],temp;
    int i,j;
    printf("Enter a string:");
    fgets(str,sizeof(str),stdin);
    int len=strlen(str);
    for(i=0;i<len-1;i++)
    {
        for(j=0;j<len-1-i;j++)
        {
            if(str[j]>str[j+1])
            {
                temp=str[j];
                str[j]=str[j+1];
                str[j+1]=temp;
            }
        }
    }
    printf("%s",str);
    return 0;
}
```
### 13. Write a program in C to extract a substring from a given string
```
#include <stdio.h>
#include <string.h>
int main()
{
    char str[100],substr[100];
    int start,length,i;
    fgets(str,sizeof(str),stdin);
    printf("Enter starting index:");
    scanf("%d",&start);
    printf("enter substring length:");
    scanf("%d",&length);
    for(i=0;i<length;i++)
    substr[i]=str[start+i];
    substr[i]='\0';
    printf("%s",substr);
    return 0;
}
```
### 14.  Write a C program to check whether a substring is present in a string.
### 15.  write a program in c to read a sentence and replace lowercase characters with uppercase and vice versa
```c
#include <stdio.h>
#include <string.h>
int main()
{
    char str[100],i=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    while(str[i]!='\0')
    {
        if(str[i]>='a'&&str[i]<='z')
        str[i]=str[i]-32;
        else  if(str[i]>='A'&&str[i]<='Z')
        str[i]=str[i]+32;
        i++;
    }
    printf("%s",str);
    return 0;
}
```
### 16. Write a program in C to find the number of times a given word 'the' appears in the given string
```c
#include <string.h>
int main()
{
    char str[100],arr[10][10];
    int i=0,j=0,size=0,c=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    while(str[i]!='\0')
    {
        if(str[i]!=' ')
        arr[size][j++]=str[i];
        else{
            size++;
            j=0;
        }
        i++;
    }
    for(int i=0;i<=size;i++){
    printf("%s ",arr[i]);
    if(strcmp(arr[i],"the")==0)
    c++;
    }
    printf("%d",c);
    return 0;
}
```
### 17. Write a program in C to remove characters from a string except alphabets.
```c
#include <stdio.h>
#include <string.h>
int main()
{
    char str[100];
    int i=0,j=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    while(str[i]!='\0')
    {
        if ((str[i] >= 'A' && str[i] <= 'Z') || (str[i] >= 'a' && str[i] <= 'z')) {
            str[j] = str[i]; 
            j++;
        }
        i++;
    }
    str[j]='\0';
    printf("%s",str);
    return 0;
}
```
### 18.Write a program in C to find the frequency of characters
```c
#include <stdio.h>
#include <string.h>
int main()
{
    char str[100];
    int i=0,j=0,size=0,c=0;
    printf("Enter string:");
    scanf("%s",str);
    int len=strlen(str);
    for(int i=0;i<len;i++)
    {
        c=1;
        if(str[i]=='\0')
           continue;
        for(j=i+1;j<len;j++)
        {
            if(str[j]==str[i]){
            c++;
            str[j]='\0';}
        }
        printf("%c  %d\n",str[i],c);
    }
    return 0;
}
```
### 19.. Write a program in C to combine two strings manually
```c
#include <stdio.h>
#include <string.h>
int main()
{
    char str[100];
    int i=0,j=0,size=0,c=0;
    printf("Enter string:");
    scanf("%s",str);
    int len=strlen(str);
    for(int i=0;i<len;i++)
    {
        c=1;
        if(str[i]=='\0')
           continue;
        for(j=i+1;j<len;j++)
        {
            if(str[j]==str[i]){
            c++;
            str[j]='\0';}
        }
        printf("%c  %d\n",str[i],c);
    }
    return 0;
}
```
### 20. Write a program in C to find the largest and smallest words in a string
```c
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    int i = 0, start = 0, end = 0, len = 0;
    int maxLen = 0, minLen = 100; 
    int maxStart = 0, minStart = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    while (str[i] != '\0') {
        if (str[i] != ' ' && str[i] != '\n') {
            if (len == 0) start = i;  
            len++;
        } else {
            if (len > 0) {
                if (len > maxLen) {
                    maxLen = len;
                    maxStart = start;
                }
                if (len < minLen) {
                    minLen = len;
                    minStart = start;
                }
                len = 0;
            }
        }
        i++;
    }
    if (len > 0) {
        if (len > maxLen) {
            maxLen = len;
            maxStart = start;
        }
        if (len < minLen) {
            minLen = len;
            minStart = start;
        }
    }
     printf("Largest word: ");
    for (i = maxStart; i < maxStart + maxLen; i++)
    printf("%c", str[i]);
    printf("\n");

    printf("Smallest word: ");
    for (i = minStart; i < minStart + minLen; i++) printf("%c", str[i]);
    printf("\n");

    return 0;
}
```
### 21. Write a program in C to convert a string to uppercase
```c
#include<stdio.h>
int main()
{
char str[100];
int i=0;
scanf("%s",str);
for(i=0;str[i]!='\0';i++)
{
    if(str[i]>=65 && str[i]<=90)
    continue;
    else
    str[i]=str[i]-32;
}
printf("%s",str);
}
```
### 22. Write a program in C to convert a string to lowercase
```c
#include<stdio.h>
int main()
{
   char str[100];
   int i=0;
   scanf("%s",str);
   for(i=0;str[i]!='\0';i++)
   {
      if(str[i]>=65 && str[i]<=65)
      str[i]=str[i]+32;
      else
      continue;
  }
printf("%s",str);
}
```
### 23. Write a program in C to check whether a character is a Hexadecimal Digit or not
```c
#include<stdio.h>
int main()
{
  char ch;
  scanf("%c",&ch);
  if((n>='0' && n<='9') || (n>='A' && n<='F'))
  printf("HexaDecimal");
  else
  printf("Not");
}
```
### 24. Write a program in C to check whether a letter is uppercase or not
```c
#include<stdio.h>
int main()
{
 char ch;
 scanf("%c",&ch);
 if(ch>='A' && ch<='Z')
 printf("Uppercase");
 else
 printf("Not");
}
```
### 25.Write a program in C to replace the spaces in a string with a specific character
```c
#include<stdio.h>
int main()
{
  char str[100];
  fgets(str,sizeof(str),stdin);
  for(int i=0;str[i]!='\0';i++)
    {
        if(str[i]==' ')
        str[i]='@';
    }
    printf("%s",str);
}
```
### 26.Write a program in C to count the number of punctuation characters present in a string?
```c
#include<stdio.h>
int main()
{
    int i=0,c=0;
    char str[100];
    scanf("%s",str);
   while(str[i]!='\0')
   {
      if((str[i]>='a' && str[i]<='z')||(str[i]>=0 && str[i]<=9)||(str[i]>='A' && str[i]<='Z')||str[i]=='\n'||str[i]=='\t'||str[i]==' '){
      }
      else
       c++;
    i++;
  }
  printf("%d",c);
}
```
