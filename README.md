# SieveOfEratosthenes
  code is implemented in c++;
       #include<iostream>
#include<limits.h>
using namespace std;
void sieve(int n)
{
    if(n<=1)
        return;
    bool isPrime[n+1];
    fill(isPrime , isPrime +n +1, true);
    for(int i = 2;i*i<=n;i++){
        if(isPrime[i])
        {
            for(int j = 2*i ;j<=n;j=j+i)
            {
                isPrime[j] = false;
            }
        }
    } for(int i = 2;i<=n;i++)
    {
        if(isPrime[i])
            cout<< i << "  ";
    }
}
int main()
{
    int n ;
    cin>>n;
    sieve(n);
    return 0;
}

// code with brdcoder007
