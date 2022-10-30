---
title: "Equations for Uniformly Accelerated Motion"
date: 2022-10-29T23:18:06+08:00
draft: false
math: true
tags: ["physics", "calculus", "kinematics"]
---

<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1230374854&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/renpul" title="Renpul" target="_blank" style="color: #cccccc; text-decoration: none;">Renpul</a> · <a href="https://soundcloud.com/renpul/find-a-way" title="Find A Way 【Stream Palette 3】" target="_blank" style="color: #cccccc; text-decoration: none;">Find A Way 【Stream Palette 3】</a></div>

{{< lead >}} Uniformly accelerated motion with constant acceleration gives beautiful formulae on the motion {{< /lead >}}

## First Equation of Motion

We derive $v = u + at$, where $u,\ v$ are initial and final velocity, $a$ is a constant acceleration.

### Derivation

Since $a$ is a constant, $\int_0^t adt = \int_0^t adt$ is $v - u = at$. Therefore $v = u + at$.

## Second Equation of Motion

We now derive $x = x_0 + ut + \frac{1}{2}at^2$, where $x_0$ is the initial position.

### Derivation

By the first equation of motion, $v = u + at$. Then $\int_0^t vdt = \int_0^t udt + \int_0^t at dt$ and $x - x_0 = ut + \frac{1}{2}at^2$. Therefore $x = x_0 + ut + \frac{1}{2}at^2$.

## Third Equation of Motion

We now derive $2a\Delta x = v^2 - u^2$, where $\Delta x = x - x_0$.

### Derivation

Since $\int_0^t vdt = \int_0^t udt + \int_0^t at dt$, then substituting $dv = adt$ and $t = \frac{v - u}{a}$, we have $\int_0^t vdt = a\int_u^v udv + \int_u^v \frac{(v - u)}{a}dv$. Then $\Delta x = a(uv - u^2) + \frac{(v^2 - u^2)}{2a} - a(uv - u^2)$. Therefore, $2a\Delta x = v^2 - u^2$. 