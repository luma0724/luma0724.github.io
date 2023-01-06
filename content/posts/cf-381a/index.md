---
title: "CF381A - Sereja and Dima"
date: 2023-01-05T10:50:14+08:00
draft: false
math: true
tags: ["codeforces", "2-pointers", "greedy"]
---

[CF381A - Sereja and Dima](https://codeforces.com/problemset/problem/381/A)

Let $x[n]$ be the cards and $l, r$ the left and right pointers. Sereja and Dima takes $\max(x[l], x[r])$ greedily each round then move the pointers. The game always terminate when $l>r$.

The solution is $O(n)$.

```cpp
#include <bits/stdc++.h>
using namespace std;

int x[1001], a[2], n, l, r, i;

int main() {
    scanf("%d", &n);
    
    for (i=1; i<=n; i++) {
        scanf("%d", &x[i]);
    }
    
    for (l=1, r=n, i=0; l<=r; i++) {
        if (x[r]>x[l]) {
            a[i%2]+=x[r--];
        } else {
            a[i%2]+=x[l++];
        }
    }
    
    printf("%d %d", a[0], a[1]);
}
```