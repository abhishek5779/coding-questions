```cpp
#include <iostream>
#include <vector>
#include <bits/stdc++.h>
using namespace std;

void validate_password(const std::vector<int>& password, std::string& result, int& most_frequent_element) {
    // Write your logic here.
    int n=password.size();
    map<long int, long int> frequency;
    for(long int i=0;i<n;i++)
        frequency[password[i]]++;
    result="VALID";
    long int max=0;
    int even_check=0;
    for(auto x: frequency)
    {
        if((x.second)%2 != 0)
            result="INVALID";
        if((x.second) == 2)
            even_check=1;
        if(x.second > max)
        {
            max=x.second;
            most_frequent_element=x.first;
        }
        else if (x.second == max)
        {
            if(x.first < most_frequent_element)
                most_frequent_element=x.first;
        }
    }
    if (even_check == 0)
        result="INVALID";
}

int main() {
    int N;
    std::cin >> N;
    std::vector<int> password(N);
    for (int i = 0; i < N; ++i) {
        std::cin >> password[i];
    }
    std::string validation_result;
    int most_frequent_element;
    validate_password(password, validation_result, most_frequent_element);
    std::cout << validation_result << '\n';
    std::cout << most_frequent_element << '\n';
    return 0;
}
```