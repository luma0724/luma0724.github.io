---
title: "CF279B - Books"
date: 2023-01-06T12:37:01+08:00
draft: false
math: true
tags: ["codeforces", "2-pointers"]
---

[CF279B - Books](https://codeforces.com/contest/279/problem/B)

Use 2-pointers $i, j$ to iterate throught $i=1..n$ to find $j$ such that $\sum_{k=j}^i a[k] <= t$ is maximized in order to find the $\max(i-j+1)$.

```cpp
#include <bits/stdc++.h>
using namespace std;

int a[100001], n, t, i, j, s, c;

int main() {
    scanf("%d %d", &n, &t);
    
    for (i=1, j=1; i<=n; i++) {
        scanf("%d", &a[i]);
        
        s+=a[i];
        while (j<=n&&s>t) {
            s-=a[j++];  
        }
        
        c=max(c, i-j+1);
    }
    
    printf("%d", c);
}
```