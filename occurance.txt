#include <stdio.h>
#include <string.h>


int main()
{
    int fStringNumber,sStringNumber,count=0;
    char fString[100],sString[100];
    
    scanf(" %[^\n]s",fString);
    scanf(" %[^\n]s",sString);
    
    fStringNumber = strlen(fString);
    sStringNumber = strlen(sString);
    int i = 0,j;
    for(  ;i < fStringNumber;i++)
    {
        j = 0;
        while(j < sStringNumber )
        {
            if(fString[i]==sString[j])
            {
                i++;
                j++;
            }
            
            else
            break;
        }
        printf("\nj-%d sn-%d",j,sStringNumber);
        if(j== sStringNumber)
        {
            count++;
            i--;
        }
        
    }

    printf("\n%d",count);

    return 0;
}
