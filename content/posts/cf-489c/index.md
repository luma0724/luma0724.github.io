---
title: "CF489C - Given Length and Sum of Digits..."
date: 2023-01-03T14:47:41+08:00
draft: false
math: true
tags: ["codeforces", "greedy"]
---

[CF489C - Given Length and Sum of Digits...](https://codeforces.com/contest/489/problem/C)

Let $x$ and $y$ be the maximum and mininum number with length $m$ and sum of digits $s$. Note that maximum sum of digits of length $m$ is $9m$ and if $s=0$, then there are no solutions with length $m>1$.

Construct $x$ and $y$ incrementally and greedily but note that $y[1]$ has to be at least 1 such that the length is $m$. The solution is $O(m)$.

```cpp
#include <bits/stdc++.h>
using namespace std;

int x[101], y[101];

int main() {
    int m, s;
    scanf("%d %d", &m, &s);
    
    if ((m>1&&s==0)||s>9*m) {
        printf("-1 -1");
        return 0;
    }
    
    int t = s;
    for (int i=1; i<=m&&t>0; i++) {
        x[i] = (t>=9)? 9: t;
        t -= x[i];
    }
    
    for (int i=m; i>1&&s>1; i--) {
        y[i] = (s>=10)? 9: s-1;
        s -= y[i];
    }
    y[1] = s;

    for (int i=1; i<=m; i++) {
        printf("%d", y[i]);
    }
    
    printf(" ");
    for (int i=1; i<=m; i++) {
        printf("%d", x[i]);
    }
}
```