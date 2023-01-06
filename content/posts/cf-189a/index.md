---
title: "CF189A - Cut Ribbon"
date: 2023-01-04T09:25:51+08:00
draft: false
math: true
tags: ["codeforces", "dp", "complete-knapsack"]
---

**Complete Knapsack Problem**: Given $a[4]$ weight of items with each value 1 and knapsack capacity $n$, define 

$$dp[n^\prime] = \sum_{i=1}^{3} k[i]$$

the maximum value with knapsack with capacity $n^\prime$ such that $k[i] >= 0$ is the number of times $a[i]$ is taken and 

$$\sum_{i=1}^{3} k[i]a[i] = n^\prime$$

Note that if there is no $\sum_{i=1}^{3} k[i]a[i] = n^\prime$, we define $dp[n^\prime] = -1$. The problem gurantees that $dp[n] \neq -1$.

The state transition equation is given by:

$$dp[n^\prime] = -1$$ if $dp[n-a[i]] = -1$ for $i=1..3$, and else

$$dp[n^\prime] = \max(dp[n^\prime-a[1]], dp[n^\prime-a[2]], dp[n^\prime-a[3]]) + 1$$ with $dp[0] = 0$.

We find $dp[n^\prime]$ for $n^\prime = a[i]..n$ incrementally with items $\lbrace a[1], \cdots, a[i] \rbrace$ for $i=1..3$ such that $dp[n] = \max(dp[n-a[1]], dp[n-a[2]], dp[n-a[3]])$. At each iteration, assuming $dp[n^\prime-a[i]] \neq -1$, $dp[n^\prime] = \max(dp[n^\prime-a[i]]+1, dp[n^\prime])$. Initially no item is taken, so $dp[n^\prime] = -1$ for all $n^\prime$. Note that if we only take the item $a[i]$, $dp[n^\prime] = -1$ for $n^\prime = 1..a[i]-1$. 

The solution is $O(n)$.

[CF189A - Cut Ribbon](https://codeforces.com/problemset/problem/189/A)

```cpp
#include <bits/stdc++.h>
using namespace std;
 
int n, a[4], dp[4001];
 
int main() {
    scanf("%d", &n);
    
    for (int i=1; i<4; i++) {
        scanf("%d", &a[i]);
    }
    
    memset(dp, -1, sizeof(dp));
    dp[0] = 0;
    
    for (int i=1; i<4; i++) {
        for (int j=a[i]; j<=n; j++) {
            if (dp[j-a[i]]==-1) continue;
            dp[j] = max(dp[j], dp[j-a[i]]+1);
        }
    }
    
    printf("%d", dp[n]);
}
```