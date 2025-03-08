```cpp
#include <iostream>
#include <vector>

int find_lucky_stone_pairs(int p, int n, int m, std::vector<int>& stones) {
    // Write your logic here.
    int result=0;
    for(int i=0;i<p;i++)
    {
        for(int j=i+1; j<p; j++)
        {
            if((stones[i]%n == 0) || (stones[i]%m == 0))
            {
                if((stones[j]%n ==0) || (stones[j]%m == 0))
                    result++;
            }
        }
    }
    return result;
    return 0;
}

int main() {
    int p, n, m;
    std::cin >> p >> n >> m;
    std::vector<int> stones(p);
    for (int i = 0; i < p; ++i) {
        std::cin >> stones[i];
    }
    int result = find_lucky_stone_pairs(p, n, m, stones);
    std::cout << result << std::endl;
    return 0;
}
```