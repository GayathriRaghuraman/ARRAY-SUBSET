# ARRAY-SUBSET
#include<stdio.h>
bool isSubset(int a1[], int a2[], int m, int n)
{
    int i = 0;
    int j = 0;
    for (i=0; i<n; i++)
    {
      for (j = 0; j<m; j++)
        {
          if(a2[i] == a1[j])
          break;
        }
        if (j == m)
           return 0;
    }
    return 1;
}
  
int main()
{
    int a1[] = {77,88,9,4,21,47,6};
    int a2[] = {4,5,9,18};
   
    int m = sizeof(a1)/sizeof(a1[0]);
    int n = sizeof(a2)/sizeof(a2[0]);
 
    if(isSubset(a1, a2, m, n))
      printf("A2 is subset of A1 ");
    else
      printf("A2 is not a subset of A1");      
     getchar();
    return 0;
}
