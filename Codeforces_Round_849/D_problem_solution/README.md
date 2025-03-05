# 💡 Codeforces Solutions
This folder contains solutions for problems on Codeforces.

## ✅ Problem: [1234A - Problem Title](https://codeforces.com/problemset/problem/1234/A)
- **Difficulty:** 1000  
- **Language:** C++  
- **Approach:** Used brute force, greedy, strings  
- **Time Complexity:** O(n)

### 🚀 Solution Code:
```
#include <bits/stdc++.h>
using namespace std;
int main(){
    #ifndef ONLINE_JUDGE
    freopen("in", "r", stdin);
    freopen("out", "w", stdout);
#endif
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
    
    long long tt;
    cin>>tt;
    while(tt--){
        long long n;
        cin>>n;
        string s;
        cin>>s;
        long long res=0;
        vector<long long> a(n, 0), b(n, 0);
        set<char> ss;
        for(int i=0; i<n; i++){
            ss.insert(s[i]);
            a[i]= (long long)ss.size();
        }
        ss.clear();
        for(int i= n-1; i>=0; i--){
            ss.insert(s[i]);
            b[i]= (long long)ss.size();
        }
        for(int i=0; i<n-1; i++){
            res= max(res, a[i]+b[i+1]);
        }
        cout<<res<<endl;
    }
    return 0;
}



```
