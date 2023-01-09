---
title: "Parentheses Balance"
date: 2023-01-08T16:55:15+08:00
draft: false
math: true
tags: ["stack"]
---

Given a sequence of parentheses, determine if the parentheses are balanced or not. For example, "(())(()())" is balanced but "(()()))(" is not balanced.

Solution: Maintain a stack of left parentheses. If a right parentheses mismatches, the sequence is unbalanced.

```cpp
#include <bits/stdc++.h>
using namespace std;

string s; // the sequence
stack<char> st; // stack of '('

bool is_balance() {
    getline(cin, s);

    for (auto& c: s) {
        if (c=='(')
            st.push(c);
        else if (st.empty()) // no '(' in the stack but there is a ')' to be matched
            return false;
        else // pop the top '(' if matched
            st.pop();
    }

    if (st.empty()) // every '(' in the stack has been matched
        return true;
    else // there are unmatched '('
        return false;
}
```
