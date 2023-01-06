---
title: "CF455A - Boredom"
date: 2023-01-04T11:39:23+08:00
draft: false
math: true
tags: ["codeforces", "dp"]
---

[CF455A - Boredom](https://codeforces.com/problemset/problem/455/A)

The problem asks to maximize the score. Given an array $a[n]$, the score given by deleting $a[k]$ is $a[k]m[a[k]]$ where $m[a[k]]$ is the number of $a[k]$ in the array. Precalculate the array $c[\max(a)]$, where $\max(a)$ is the maximum $a[k]$, is given by

$$c[k] = k \cdot m[k]$$ where $m[k] = 0$ if $k$ does not exists in array $a[n]$ with $c[0] = 0$ defined.

Define $dp[n^\prime]$ the array the maximum score deleting only $a[k]$ for $a[k]=1..n^\prime$. Then $dp[\max(a)]$ is the solution given by the state transition equation

$$dp[n^\prime] = \max(dp[n^\prime - 1], dp[n^\prime - 2] + c[n^\prime])$$ with $dp[1] = c[1]$ and $dp[0] = 0$ defined.

The solution is $O(n+\max(a))$. 

```cpp
#include <bits/stdc++.h>
using namespace std;

long long c[100001], dp[100001];
int n, x;

int main() {
    scanf("%d", &n);
    
    for (int i=1; i<=n; i++) {
        scanf("%d", &x);
        c[x] += x;
    }
    
    dp[1] = c[1];
    for (int i=2; i<=100000; i++) {
        dp[i] = max(dp[i-1], dp[i-2]+c[i]);
    }
    
    printf("%lli", dp[100000]);
}
```