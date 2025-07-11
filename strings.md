C
#Programming Questions
##Strings
### 1.
```
#include<stdio.h>
int main()
{
   char str[100];
   scanf("%s",str);
   printf("%s",str);
}
```
2.include <stdio.h>

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
3.#include <stdio.h>

int main()
{
    char str[100];
    int length=0,i=0;
    scanf("%s",str);
    for(i=0;str[i]!='\0';i++)
    printf("%c ",str[i]);
    return 0;
}
4.#include <stdio.h>
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
5.#include <stdio.h>

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
6.#include <stdio.h>

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
7.#include <stdio.h>

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
8.#include <stdio.h>

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
9.#include <stdio.h>

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
10.#include <stdio.h>

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
12.#include <stdio.h>
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
13.*******************************************************************************/
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
15.#include <stdio.h>
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
16.#include <string.h>
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
17.#include <stdio.h>
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
18.include <stdio.h>
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
19.#include <stdio.h>
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
20.
