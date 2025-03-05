# Solution 1

```cpp
#include <iostream>
using namespace std;

// Function to check if a number is prime
bool isprime(int k)
{
    int i;
    for(i=2; i*i<=k; i++)
    {
        if(k % i == 0)
            return false;
    }
    if(i*i > k)
        return true;
    else
        return false;
}

int main()
{
    int n;
    cin >> n;

    // Special case for the first prime number
    if(n == 1)
        cout << 2*2 << endl;
    else
    {
        int primecount = 1; // Count of prime numbers found
        long int result;

        // Loop to find the N-th prime number
        for(long int i = 3; primecount < n; i++)
        {
            if(isprime(i))
                primecount++;

            if(primecount == n)
                result = i;
        }
        // Output the square of the N-th prime number
        cout << result*result << endl;
    }
    return 0;
}
```