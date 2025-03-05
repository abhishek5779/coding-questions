```cpp
#include <bits/stdc++.h>
using namespace std;

#define MAX_SIZE 1000005

int main()
{
    int n;
    cin>>n;

    if(n==1)
    cout<<2*2<<endl;
    else
    {
        bool arr[MAX_SIZE];
        // Initialize the array to true
        memset(arr,true,sizeof(arr));
        int primecount=0;
        
        // Sieve of Eratosthenes to find prime numbers
        for(int i=2;primecount<n;i++)
        {
            if(arr[i])
            {
                primecount++;
                if(primecount==n)
                {
                    cout<<i*i<<endl;
                    break;
                }
                for(int j=i*i;j<MAX_SIZE;j=j+i)
                    arr[j]=false;
            }
        }
    }
    return 0;
}


```