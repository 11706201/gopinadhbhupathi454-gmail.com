# gopinadhbhupathi454-gmail.com
Write a multithreaded program that implements the banker's algorithm. Create n threads that request and release resources from the bank. The banker will grant the request only if it leaves the system in a safe state. It is important that shared data be safe from concurrent access. To ensure safe access to shared data, you can use mutex locks.

///it is bankers algorithm without using threads

#include<stdio.h>
int main()
{
int pid,[10], maximim[10], need[10], available,i,j,flag[10],x=0,seq[10],c=0;
printf("Enter the number of process \n");
scanf("%d",&pid);
for (i=0;i<p;i++)
{
    flag[i]=0;  //initially no process's need is fulfilled
}
for(i=0;i<p;i++)
{
    printf("Enter the allocation for process P[%d]\n",i);
    scanf("%d",&a[i]);
    printf("Enter the max for process P[%d]\n",i);
    scanf("%d",&maximum[i]);
}
printf("Enter the available resources");
    scanf("%d",&available);
for(i=0;i<p;i++)
{
    need[i]=maximum[i]-a[i];
}

for(i=0;i<p;i++)
{
    printf("Need of P[%d] is %d\n",i,need[i]);
}
for(i=0;i<p;i++)
{
    for(j=0;j<p;j++)
    {
        if(flag[j]==0&&need[j]<=available)
        {
        available=available+a[j];
        flag[j]=1;
        printf("Process %d has been allocated resources\n",j);
        seq[c]=j;
        c++;
        }
    }
}
for(i=0;i<p;i++)
{
    if(flag[i]==0)
    {
    printf("unsafe state\n");
    x=1;
    break;
    }
   
}
if(x==0)
{
printf("safe state\n");
printf("Safe sequence is \n");
for(i=0;i<p;i++)
{
    printf("P[%d],",seq[i]);
}
}
printf("\n");
}
