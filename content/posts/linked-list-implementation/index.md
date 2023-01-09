---
title: "Linked List Implementation"
date: 2023-01-09T13:46:25+08:00
draft: false
math: true
tags: ["linked-list"]
---

A **linked list** can be implemented with pointers and dynamic memory allocation

```cpp
struct node {
    int u;
    struct node* next;
    node(int x): u(x), next(nullptr) {}
}* head=nullptr;
int sz, i;

// insert node with value x after the jth node
void insert(int x, int j) {
    sz++;
    node* n=new node(x);

    if (!j) { // if j==0, insert before head
        n->next=head;
        head=n;
    } else { // else iterate until insertion
        node* cur=head; for (i=1; i<j; i++, cur=cur->next);
        n->next=cur->next;
        cur->next=n;
    }
}

void erase(int j) { // assume the jth node exists
    sz--;

    if (j==1)
        head=head->next;
    else {
        node* cur=head; for (i=1; i<j-1; i++, cur=cur->next);
        node* x=cur->next;
        cur->next=x->next;
        delete x;
    }
}

int query(int j) { // assume the jth node exists
    node* cur=head; for (i=1; i<j; i++, cur=cur->next);
    return cur->u;
}
```
