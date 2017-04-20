#include <stdio.h>

int narcissistic( int number );
void PrintN( int m, int n );

int main()
{
    int m, n;

    scanf("%d %d", &m, &n);
    if ( narcissistic(m) ) printf("%d is a narcissistic number\n", m);
    PrintN(m, n);
    if ( narcissistic(n) ) printf("%d is a narcissistic number\n", n);

    return 0;
}


int narcissistic( int number )
{
    int a,b,c,d;
   if(number>=100&&number<1000)
        {
            a=number/100;
    b=number%100/10;
    c=number%10;
    if (number==a*a*a+b*b*b+c*c*c)
        return 1;
        else return 0;
}

else if(number>=1000&&number<10000)
{
    a=number/1000;
    b=number%1000/100;
    c=number%1000%100/10;
    d=number%10;
   if(number==a*a*a*a+b*b*b*b+c*c*c*c+d*d*d*d)
    return 1;
   else return 0;
}
 else if(number==10000)
    return 0;
}
void PrintN( int m, int n )
{
    int i;
for(i=m;i<n;i++)
{
   if( narcissistic(i)==1)
    printf ("%d\n",i);
}
}

