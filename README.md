#include<stdio.h>
#include <stdlib.h>
int isvowel(char c)
{
    c=tolower(c);
    if(c=='a'||c=='o'||c=='i'||c=='e'||c=='u')
      return 1;
    return 0;  
}
int main()
{
    char s[1000];
    scanf("%s",s);
    int n=strlen(s),i,ct=0;
    for(i=0;i<n-1;i++)
      if(isvowel(s[i])&&isvowel(s[i+1]))
         ct++;
    printf("%d",ct);
}
