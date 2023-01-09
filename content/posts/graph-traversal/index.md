---
title: "Graph Traversal"
date: 2023-01-08T15:20:25+08:00
draft: false
math: true
tags: ["graph"]
---

## Depth-first Search
Depth-first search explores unvisited path and goes as far as possible, and backtracks to explore a new path. It repeats until there is no path unexplored. I assume the graph is implemented as a linked adjacency list [Graph Implementation](/posts/graph-implementation).

Depth-first search can be implemented recursively which resembles using a stack:

```cpp
struct edge {
    int to, next, w;
} e[E<<1]; // e[E] if directed graph
int head[V], i;
int visit[V]; // visit[i] marks if vertex i is visited or not

// to start a search, call at the source vertex
void dfs(int u) {
    visit[u]=true;

    int i=head[u];
    while (i) {
        if (!visit[e[i].to])
            dfs(e[i].to);
        i=e[i].next;
    }
}
```

Example of using $dfs$ to find a path in a graph:

```cpp
// ૮ ˶ᵔ ᵕ ᵔ˶ ა
#include <bits/stdc++.h>
using namespace std;

struct edge {
    int to, next, w;
} e[100];
int head[101], i, u, v, w, d;
bool found;

void add_edge(int u, int v, int w) {
    e[++i]={v, head[u], w};
    head[u]=i;

    e[++i]={u, head[v], w};
    head[v]=i;
}

void dfs(int u, int p) {
    if (u==d) {
        printf("%d ", u);
        found=true;
        return;
    }
    
    int i=head[u];
    while (i) {
        if (e[i].to!=p)
            dfs(e[i].to, u);
        
        if (found) {
            printf("%d ", u);
            return;
        }
        
        i=e[i].next;
    }
}

int main() {
    while (cin>>u>>v>>w) {
        add_edge(u, v, w);
    }
    
    d=6;
    dfs(1, 0);
}

/*
Input:
1 2 1
1 3 1
1 4 1
2 3 1 
2 4 1
3 4 1
3 5 1
4 5 1
5 6 1

Output:
6 5 4 1
*/
```

## Bredth-first Search
Breadth-first search is very similar to depth-first search, but it uses a queue to maintain the unexplored vertices and thus finds the shortest path given an unweighted graph.

```cpp
struct edge {
    int to, next, w;
} e[E<<1]; // e[E] if directed graph
int head[V], i;
int visit[V]; // visit[i] marks if vertex i is visited or not
queue<int> q;

// to start a search, call at the source vertex
void bfs(int u) {
    q.push(u);
    visit[u]=true;

    while (!q.empty()) {
        int v=q.front(), i=head[v];
        q.pop();
        
        while (i) {
            if (!visit[e[i].to]) {
                q.push(e[i].to);
                visit[e[i].to]=true;
            }

            i=e[i].next;
        }
    }
}
```

We can do **bidirection search** with $bfs$ from both vertices $u$ and $v$ in order to speed up finding the shortet path between $u$ anad $v$.

