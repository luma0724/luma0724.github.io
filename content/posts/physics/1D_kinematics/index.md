---
title: "1D Kinematics"
date: 2022-10-29T15:35:59+08:00
draft: false
math: true
tags: ["physics", "kinematics", "calculus"]
---

<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1293576427&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/elliot-hsu" title="Elliot Hsu" target="_blank" style="color: #cccccc; text-decoration: none;">Elliot Hsu</a> · <a href="https://soundcloud.com/elliot-hsu/grimoire-academia" title="Grimoire Academia (w/ Sin:cK)" target="_blank" style="color: #cccccc; text-decoration: none;">Grimoire Academia (w/ Sin:cK)</a></div>

## Example 1 - Kinematics solved with Determinant of Quadratic Equation

Two trains, A and B, travel in the same direction on the same set of tracks. A starts at rest at position $d$, and B starts with velocity $u$ at the origin. A accelerates with acceleration $a$, and B decelerates with acceleration $-a$. What is the maximum $u$ such that A and B don't collide?

### Solution

Let $u_{max}$ be the maximum initial velocity of B such that A and B don't collide. Let $s_A = d + \frac{1}{2}at^2$ and $s_B = ut - \frac{1}{2}at^2$. Then $u = u_{max}$ if $s_A = s_B$, i.e., when A stops, A and B barely touches. Then $d + \frac{1}{2}at^2 = u_{max}t - \frac{1}{2}at^2$. We write the equation making $t$ the subject. Then $at^2 - u_{max}t + d = 0$. A and B barely touches if the determinant $u_{max}^2 - 4ad = 0$. Therefore, $u_{max} = 2\sqrt{ad}$.

## Example 2 - Kinematics

Two cars, A and B, start at the same position with the same speed $u$. Car A travels at constant speed and car B decelerate with constant acceleration $-a$. At the instant when B reaches a speed of zero, what is the ratio of the distances travelled by A and B?

### Solution

Let $s_A = ut$ and $s_B = ut - \frac{1}{2}at^2$ be the distance A and B travelled at $t$ when B stops. Then $0 = u - at$ and $u = at$. Therefore, the desired ratio $\frac{s_A}{s_B} = \frac{ut}{ut - \frac{1}{2}at^2} = \frac{u}{u - \frac{1}{2}at} = \frac{u}{u - \frac{1}{2}u} = 2$.

## Example 3 - Kinematics

An object starts from rest at the origin at time $t = 0$ and accelerates with constant acceleration $a$. A second object starts from rest at the origin at time $t = t_1$ and accelerates with the same $a$. Find the distance between the two objects at $t > t_1$.

### Solution

Let $d = s_a - s_b$ be the distance between the two objects at $t$, where $s_a = \frac{1}{2}at^2$ and $s_b = \frac{1}{2}a(t - t_1)^2$. Then $d = at_1t - \frac{1}{2}at_1^2$. Note that $d$ is a linear function of $t$.

## Example 4 - Kinematics with Constant Acceleration due to Gravity

A ball is dropped from rest at height $h$. Directly below on the ground, a second ball is simultaneously thrown upward with speed $u$. If the two balls collide at the moment the second ball is instantaneously at rest, what is the height of the collision. What is the relative speed of the balls when they collide.

### Solution

Let $t$ be the instant. Then $0 = u - gt$ and $t = \frac{u}{g}$. Let $s_a = \frac{1}{2}gt^2$ and $s_b = \frac{u^2}{2g}$ such that $h = s_a + s_b$. Then $h = \frac{u^2}{2g} + \frac{u^2}{2g} = \frac{u^2}{g}$.

## Example 5 - Kinematics

A lift ascends with constant acceleration $a$, then with constant velocity $u$ and finally stops with constant retardation $a$. If the total distance ascends is $s$ and total time occupied is $t$, show that the time during which the lift ascended with constant velocity is $\sqrt{t^2 - \frac{4s}{a}}$.

### Solution

Let $t_a$ such that $u = at_a$. Let $2x_a$ be distance travelled with acceleration, where $2ax_a = u^2$. Then $s - 2x_a = u(t - 2t_a)$. We try to write it in $t_a$. Then, $s - at_a^2 = att_a - 2at_a^2$. Write it in quadratic, we have $at_a^2 - att_a + s = 0$ and $2t_a = t \pm \sqrt{t^2 - \frac{4s}{a}}$. Then the time required $t - 2t_a = \sqrt{t^2 - \frac{4s}{a}}.

## Example 6 - Kinematics with Calculus

Find the velocity $v$ and position $x$ of a particle of mass $m$ that is subject to a frictional force proportional to velocity.

### Solution

Let $f = -\alpha v$ where $\alpha > 0$ be the frictional force. Then $ma = -\alpha v$. Let $\frac{1}{\tau} = \frac{\alpha}{m}$ and $u$ be the initial velocity. Then $\int_u^v \frac{dv}{v} = - \frac{1}{\tau} \int_0^t dt$ and $v = ue^{-\frac{t}{\tau}}$. Therefore $\int_0^t v dt = u\int_0^t e^{-\frac{t}{\tau}} dt$ and $x = x_0 + u\tau(1 - e^{-\frac{t}{\tau}})$.
