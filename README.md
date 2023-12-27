#include<stdio.h>
#include<string.h>
#include<stdbool.h>
bool check(char*s,char*t)
{
	int c=0;
	if(strlen(s)!=strlen(t))
	{
		return false;
	}
	for(int i=0;i<strlen(s);i++)
	{
		for(int j=0;j<strlen(t);j++)
		{
			if(s[i]==t[j])
			{
				c++;
			}
		}
	}
	if(c==strlen(s))
	{
		return true;
	}
	else
	{
		return false;
	}
}
int main()
{
	char s[200],t[200];
    printf("Enter the 1st string: ");
    scanf("%s",s);
    printf("Enter the 2nd string: ");
    scanf("%s",t);
    bool result = check(s,t);
    if(result==true)
    {
    	printf("\n%s and %s strings are anagram",s,t);
    }
    else if(result==false)
    {
    	printf("\n%s and %s strings are not anagram",s,t);
    }
	return 0;
}
