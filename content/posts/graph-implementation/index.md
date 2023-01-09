---
title: "Graph Implementation"
date: 2023-01-07T15:49:30+08:00
draft: false
math: true
tags: ["graph"]
---

## Linked Adjacency List
A graph can be implemented as a **linked adjacency list** (more preferred than adjancency matrix or edge list due to memory constraints)

```cpp
struct edge {
    int to, next, w;
} e[E<<1]; // e[E] if directed graph
int head[V], i;

void add_edge(int u, int v, int w) {
    e[++i]={v, head[u], w};
    head[u]=i;

    e[++i]={u, head[v], w}; // undirected graph
    head[v]=i;
}

// traversing the graph
void dfs(int u, int p) {
    int i=head[u];
    while (i) { // terminate when i=0
        if (e[i].to!=p)
            dfs(e[i].to, u);
        i=e[i].next; // linked list
    }
}
```
