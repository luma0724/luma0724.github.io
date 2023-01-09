---
title: "CF580C - Kefa and Park"
date: 2023-01-07T14:45:12+08:00
draft: false
math: true
tags: ["codeforces", "dfs", "tree"]
---

[CF580C - Kefa and Park](https://codeforces.com/problemset/problem/580/C)

Depth-first search but maintain $s$ the number of consecutive cats till vertex $u$. If $s>m$, leaves. If $u$ is not vertex 1 and the degree of $u$ is 1, i.e., it is a leaf, it is an answer.

The solution is $O(n)$.

```cpp
// ૮ ˶ᵔ ᵕ ᵔ˶ ა
#include <bits/stdc++.h>
using namespace std;

int a[100001], n, m, i, u, v, ans;
vector<int> tree[100001];

void dfs(int u, int p, int s) {
    if (s>m) return;
    if (u!=1&&tree[u].size()==1) ans++;
    
    for (auto& v: tree[u]) {
        if (v==p) continue;
        
        if (a[v]) dfs(v, u, s+1);
        else dfs(v, u, 0);
    }
}

int main() {
    scanf("%d%d", &n, &m);
    
    for (i=1; i<=n; i++) {
        scanf("%d", &a[i]);
    }
    
    while (cin>>u>>v) {
        tree[u].push_back(v);
        tree[v].push_back(u);
    }

    dfs(1, 0, a[1]);
    
    printf("%d", ans);
}
```