---
title: "Constants"
date: 2022-10-26T22:03:59+08:00
draft: false
---

<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/357540014&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/nagiha" title="Nagiha" target="_blank" style="color: #cccccc; text-decoration: none;">Nagiha</a> · <a href="https://soundcloud.com/nagiha/reprosperitas" title="Re:prosperitás" target="_blank" style="color: #cccccc; text-decoration: none;">Re:prosperitás</a></div>

{{< lead >}}Constants are promises by the compiler.{{< /lead >}}

## Constants

C++ has two notions of **immutability**:
1. `const`
2. `constexpr`

### `const` Keyword

The compiler enforces the promise of immutability with the `const` keyword. This is used primarily to specify interface, that arguments passed to a function will NOT be modified. `const` variable may be evaluated in **run-time**.

### `constexpr` Keyword

The compiler allows **compile-time evaluated constants** named `constexpr`. It instructs the compiler to write data into read-only memory. Philosophically, a variable is `constexpr` if and only if the compiler can always replace it with an exact value that can be computed in compile time.

For a function to appear in the definition of a `constexpr` variable, the function must be `constexpr`. The function must be simple enough for it to be evaluated in compile-time e.g. `return` a value.

### Examples

```cpp
#include <vector>
using namespace std;

constexpr double square(double x) { // constexpr function
    return x*x;
}

const int dmv = 17; // const variable
int var = 12; // var is NOT a const variable

constexpr double max1 = 1.4*square(dmv); // constexpr as square is constexpr and dmv is const
// constexpr double max2 = 1.4*square(var); // error as var is NOT a const

double sum(const vector<double> &v); // declares sum will not modify v
vector<double> v = {1, 2, 3, 4};
const double s1 = sum(v); // evaluated at run-tiime
constexpr double s2 = sum(v); // error: v is NOT a const
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/Hj4EowvYAOQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
