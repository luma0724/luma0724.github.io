---
title: "Evaluate Reverse Polish Notation"
date: 2023-01-09T12:00:05+08:00
draft: false
math: true
tags: ["stack", "RPN"]
---

Maintain a stack of result of the arithemetic expression. Push numbers into the stack. If it is an operator, pop two numbers out of the stack and evaluate it with the operator, and push the result back to the stack. The answer is the result left in the stack in the end, assume the expression is in valid Reverse Polish Notation.

```cpp
#include <bits/stdc++.h>
using namespace std;

stack<int> sol; // the solution; assume int
vector<string> rpn; // assume tokenized rpn expression

// supports simple arithmetics: +-*/
int eval_expr(int x, int y, char t) { // assume all operators only single charactered
    switch(t) {
        case '+': return x+y;
        case '-': return x-y;
        case '*': return x*y;
        case '/': return x/y;
        default: return 0;
    }
}

int eval_rpn() {
    // clean-up
    while (!sol.empty()) sol.pop();

    for (auto& t: rpn) {
        if (isdigit(t[0])) // assume all numbers valid
            sol.push(stoi(t));
        else { // an operator
            int y=sol.top(); sol.pop();
            int x=sol.top(); sol.pop();

            sol.push(eval_expr(x, y, t[0]));
        }
    }

    // assume rpn valid then the number left in the stack is the solution
    return sol.top();
}
```
