---
title: "Scope and Lifetime of Variables"
date: 2022-10-26T14:52:58+08:00
draft: false
tags: ["C++"]
---

<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/532893699&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/whitefists" title="WHITEFISTS" target="_blank" style="color: #cccccc; text-decoration: none;">WHITEFISTS</a> · <a href="https://soundcloud.com/whitefists/g2r2018vector" title="【G2R2018】VECTOЯ" target="_blank" style="color: #cccccc; text-decoration: none;">【G2R2018】VECTOЯ</a></div>

{{< lead >}}A declaration introduces a name into a scope.{{< /lead >}}

## Scope

> The scope defines where a variable can be accessed.

### Local Scope

A name declared in a function or lambda function has a **local scope** (block scope). The scope extends from its point of declaration to the end of the block.

```cpp
#include <vector>
using namespace std;

int main() {
    vector<int> vi; // vi has local scope to main()
}
```

### Class Scope

A **class member name** is defined in a class, or outside any function, lambda function or `enum` class. The scope extends to the class.

```cpp
#include <string>

struct Record {
    string name; // name has class scope to Record    
}
```

### Namespace Scope

A **namespace member name** is defined in a namespace outside any function, lambda function or `enum` class. The scoep also extends to the namespace.

A **global name** is outside any construction and is said to be in the **global namespace**.

```cpp
void g(); // g() is in the global namespace

namespace A {
    namespace B {
        void f(); // A::B::f() has namespace scope to A::B
    }
    
    void B::f() {} // definition of A::B::f()
}
```

## Lifetime

{{< alert >}}
**Initialize** the object before using it!
{{< /alert>}}

An local scope name lives until and is destroyed at the end of its scope. A class member name lives until the point of destruction of the object of which the name is a member. A namespace member name lives until the end of the program. A **dynamic object** lives until it is `delete`.

{{< alert >}}
Remember to **delete dynamic objects** or **memory leak**!
{{< /alert >}}

```cpp
#include <vector>

auto vi = new vector<int>{1, 2, 3};

int main() {
    delete vi; // vi is destroyed
    return 0;
}
```
