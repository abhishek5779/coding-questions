```cpp
#include <iostream>
#include <vector>
#include <bits/stdc++.h>
#include <algorithm>
using namespace std;

int calculate_min_moves(const std::vector<int>& seats, const std::vector<int>& students) {
    int n=seats.size();
    if(n==1)
    return 0;
    vector<int> copyseats;
    vector<int> copystudents;
    copyseats=seats;
    copystudents=students;
    sort(copyseats.begin(),copyseats.end());
    sort(copystudents.begin(),copystudents.end());
    int sum=0;
    for (int i=0;i<n;i++)
    {
        sum+=abs(copyseats[i]-copystudents[i]);
    }
    return sum;
    return 0;
}

int main() {
    int n;
    std::cin >> n;
    std::vector<int> seats(n);
    std::vector<int> students(n);
    for (int i = 0; i < n; ++i) {
        std::cin >> seats[i];
    }
    for (int i = 0; i < n; ++i) {
        std::cin >> students[i];
    }
    int result = calculate_min_moves(seats, students);
    std::cout << result << std::endl;
    return 0;
}
```