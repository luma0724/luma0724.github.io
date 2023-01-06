---
title: "CF489B - BerSU Ball"
date: 2023-01-05T11:24:58+08:00
draft: false
math: true
tags: ["codeforces", "greedy", "2-pointers"]
---

[CF489B - BerSU Ball](https://codeforces.com/problemset/problem/489/B)

Sort arrays $a, b$. Match $a[i], b[j]$ greedily with two pointers $i, j$. Assume $a[x], b[y]$ the first pair inconsistent with the optimal pair. Note that if $a[i^\prime], b[j^\prime]$ match, $b[j^\prime]$ is always the minimum $b[j]$ upon $a[i]$ not paired in array $b$. Let $a[x^\prime], b[y^\prime]$ be the optimal pair, then $a[x^\prime]\geq a[x]$ and $b[y^\prime] > b[y]$. Let $tol$ and $tol^\prime$ be the total number of pairs given by the algorithm and the optimal solution respectively, we can show that $tol^\prime \leq tol$, i.e., the solution given by the algorithm is more "optimal", which contradicts. Therefore, the greedy is correct.

The solution is $O(n\lg n + m\lg m)$.

```cpp
#include <bits/stdc++.h>
using namespace std;

int n, m, a[101], b[101], i, j, x;

int main() {
    scanf("%d", &n);
    for (i=1; i<=n; i++) {
        scanf("%d", &a[i]);
    }
    
    scanf("%d", &m);
    for (j=1; j<=m; j++) {
        scanf("%d", &b[j]);
    }
    
    sort(a+1, a+1+n);
    sort(b+1, b+1+m);
    
    for (i=1, j=1; i<=n&&j<=m;) {
        if (abs(b[j]-a[i])<=1) {
            x++, i++, j++;
        } else if (a[i]<b[j]) {
            i++;
        } else j++;
    }
    
    printf("%d", x);
}
```