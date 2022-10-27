---
title: "Relative Motion"
date: 2022-10-27T21:21:53+08:00
draft: false
math: true
---

## Example 1

A river has a steady speed of 0.5 $m s^{-1}$. A student swims upstream a distance of 1 $km$ and swims back to the start. If the student can swim at a speed of 1.2 $m s^{-1}$ in still water, how long does the trip takes?

Solution:

Since $1000 = (1.2 - 0.5)t_{upstream}$, $t_{upstream} = 1430\ s$. Since $1000 = (1.2 + 0.5)t_{downstream}$, $t_{downstream} = 588\ s$. Therefore, $t_{total} = 1430 + 588 = 2020\ s$.

## Example 2

A car travels due east with a speed of 50 $km/h$. Rain drops are falling at constant speed vertically with respect to the Earth. The traces of the rain on the side of the windows of the car makes an angle of 60 $^{\circ}$ with the vertical. Find the velocity of the rain with respect to the car and the Earth respectively.

Solution:

Let $v_{rain}$ and $v_{car}$ be the velocity of the rain and the car with respect to the Earth respectively, and $v_{rc}$ the velocity of the rain with respect to the car. Then $v_{car} = 50\ km\ h^{-1}$. Then $v_{rc} = \frac{50}{\sin 60^{\circ}} = 57.7\ km\ h^{-1}$ and $v_{rain} = \frac{50}{\tan 60^{\circ}} = 28.9\ km\ h^{-1}$.

## Example 3

Two swimmers, Alan and Beth, start together at the same point on the bank of a wide stream that flows with a constant speed $v$. Both moves at the same speed $c > v$ relative to the water. Alan swims downstream a distance $L$ and then upstream the same distance. Beth swims such that her motion relative to the Earth is perpendicular to the banks of the stream. She swims the distance $L$ and then back the same distance, so that both swimmers return to the starting point. Which swimmer returns first?

Solution:

For Alan, $L = (c + v)t_{downstream}$ and $L = (c - v)t_{upstream}$. $t_{Alan} = t_{downstream} + t_{downstream} = \frac{L}{c + v} + \frac{L}{c - v} = \frac{\frac{2L}{c}}{1 - \frac{v^2}{c^2}}$.

For Beth, $2L = (\sqrt{c^2 - v^2})t_{Beth}$ and $t_{Beth} = \frac{\frac{2L}{c}}{\sqrt{1 - \frac{v^2}{c^2}}}$. Since $c > v$ and $\sqrt{1 - \frac{v^2}{c^2}} < 1$, Beth returns first.

## Example 4

A man traveling East at 8 $km\ h^{-1}$ finds the wind seems to blow from the North. On doubling his speed his finds that it seems to come NE. Find the velocity of the wind.

Solution:

Let $w = xi + yj$ be the velocity of the wind relative to the Earth. Then $w - 8i = (x - 8)i + yj = yj$, hence $x = 8$. Also $w - 16i = -8i + yj$ buy $y = -8$. Therefore $w = 8i - 8j$ and $w = 8\sqrt 2\ km\ h^{-1}$

## Example 5

At a particular instant, ship A is travelling due North at 30 $km/h$ and ship B is at a certain distance N60$^{\circ}$W from A. Ship B is travelling at constant velocity in direction N45$^{\circ}$E. The two ships finally met. What is the magnitude of velocity of ship B?

Solution:

We choose the coordinates such that ship A and B have the same $y$ position. Then $v_B\cos(60^{\circ} + 45^{\circ} - 90^{\circ}) = 30\cos 30^{\circ}$ and hence $v_B = 26.9\ m\ s^{-1}$.
