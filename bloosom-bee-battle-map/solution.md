```cpp
#include <iostream>
#include <vector>
#include <map>
using namespace std;

vector<int> user_logic(int n1, vector<int>& flowers, int n2, vector<int>& herbs) {
    map<int,int> lilycount;
    map<int,int> rosecount;

    for(int i=0;i<n1;i++)
        lilycount[flowers[i]]++;
    for(int i=0;i<n2;i++)
        rosecount[herbs[i]]++;

    vector <int> results;
    for(int i=0;i<n1;i++)
    {
        if(rosecount.find(flowers[i])!=rosecount.end())
        {
            if(lilycount[flowers[i]] > rosecount[flowers[i]])
                results.push_back(flowers[i]);
        }
        else
        {
            results.push_back(flowers[i]);
        }
    }
    if(results.size()==0)
    results.push_back(-1);
    return results;
    
}

int main() {
    int n1, n2;
    cin >> n1;
    vector<int> flowers(n1);
    for (int i = 0; i < n1; ++i) {
        cin >> flowers[i];
    }
    cin >> n2;
    vector<int> herbs(n2);
    for (int i = 0; i < n2; ++i) {
        cin >> herbs[i];
    }

    vector<int> result = user_logic(n1, flowers, n2, herbs);

    if (result.size() == 1 && result[0] == -1) {
        cout << -1 << endl;
    } else {
        for (int i = 0; i < result.size(); ++i) {
            cout << result[i] << " ";
        }
        cout << endl;
    }
    return 0;
}
```