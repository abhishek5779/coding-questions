```cpp
#include <iostream>
#include <vector>
#include <map>
#include <cmath>
using namespace std;

int calculate_wish_values_sum(int N, const std::vector<int>& A) {
    // Write your logic here.
    vector<int> maxatpoint(N);
    int max=0;
    for(int i=N-1;i>=0;i--)
    {
        if(A[i]>max)
            max=A[i];
        maxatpoint[i]=max;
    }
    int wishvalue=0;
    int min=A[0];
    for(int i=0;i<N;i++)
    {
        if(A[i]<min)
            min=A[i];
        wishvalue+=abs(maxatpoint[i]-min);
    }
    return wishvalue;
    return 0;
}

int main() {
    int N;
    std::cin >> N;
    std::vector<int> A(N);
    for (int i = 0; i < N; ++i) {
        std::cin >> A[i];
    }
    int result = calculate_wish_values_sum(N, A);
    std::cout << result << std::endl;
    return 0;
}
```