---
title: "CF706B - Interesting Drink"
date: 2023-01-04T13:45:08+08:00
draft: false
math: true
tags: ["codeforces", "dp", "prefix-sum"]
---

[CF706B - Interesting Drink](https://codeforces.com/problemset/problem/706/B)

Let $c[max(x)]$ array such that $a[x]$ is the number of $x$. Let $s[max(x)]$ be the prefix sum of $c[max(x)]$ given by

$$s[i] = s[i-1] + c[i]$$ with $s[1] = c[1]$.

The solution is $s[m]$ for $m \leq max(x)$, else it is simply $n$.

The solution is $O(n+q)$.

```cpp
#include <bits/stdc++.h>
using namespace std;
 
int x, c[100001], s[100001], n, m, q;
 
void solve() {
    scanf("%d", &m);
    
    printf("%d\n", s[min(100000, m)]);
}
 
int main() {
    scanf("%d", &n);
    
    for (int i=1; i<=n; i++) {
        scanf("%d", &x);
        c[x]++;
    }

    s[1] = c[1];
    for (int i=2; i<=100000; i++) {
        s[i] = s[i-1] + c[i];
    }
    
    scanf("%d", &q);
    
    while (q--) {
        solve();
    }
}
```