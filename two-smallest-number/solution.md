```cpp
#include <iostream>
#include <vector>
#include <climits>
using namespace std;

// Placeholder function for user logic
int findLargestNumber(vector<int>& arr) {
    // Write your logic here
    int n=arr.size();
    if(n==1)
    return arr[0];
    int small1, small2;
    small1=arr[0];
    small2=100;
    for(int i=1;i<n;i++)
    {
        if(arr[i]<small1)
        {
            small2=small1;
            small1=arr[i];
        }
        else
        {
            if(arr[i]<small2 && arr[i]!=small1)
                small2=arr[i];
        }
    }
    if(small2==100)
        small2=small1;
    return (small2*10)+small1;

    return 0; // Placeholder return value
}

int main() {
    int n;
    cin >> n;
    vector<int> arr(n);
    for (int i = 0; i < n; ++i) {
        cin >> arr[i];
    }
    // Call user logic function and print the output
    int result = findLargestNumber(arr);
    cout << result << endl;
    return 0;
}
```