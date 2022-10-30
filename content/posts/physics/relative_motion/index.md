---
title: "Relative Motion"
date: 2022-10-27T21:21:53+08:00
draft: false
math: true
tags: ["physics", "kinematics"]
---

<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/393401091&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/od8vuui09c4z" title="D.G.K." target="_blank" style="color: #cccccc; text-decoration: none;">D.G.K.</a> · <a href="https://soundcloud.com/od8vuui09c4z/vacuum-trackadd8e6" title="無人区-Vacuum Track#ADD8E6-" target="_blank" style="color: #cccccc; text-decoration: none;">無人区-Vacuum Track#ADD8E6-</a></div>

## Example 1 - Linear Relative Motion

A river has a steady speed of 0.5 $m s^{-1}$. A student swims upstream a distance of 1 $km$ and swims back to the start. If the student can swim at a speed of 1.2 $m s^{-1}$ in still water, how long does the trip takes?

### Solution

Since $1000 = (1.2 - 0.5)t_{upstream}$, $t_{upstream} = 1430\ s$. Since $1000 = (1.2 + 0.5)t_{downstream}$, $t_{downstream} = 588\ s$. Therefore, $t_{total} = 1430 + 588 = 2020\ s$.

## Example 2 - Relative Velocity

A car travels due east with a speed of 50 $km/h$. Rain drops are falling at constant speed vertically with respect to the Earth. The traces of the rain on the side of the windows of the car makes an angle of 60 $^{\circ}$ with the vertical. Find the velocity of the rain with respect to the car and the Earth respectively.

### Solution

Let $v_{rain}$ and $v_{car}$ be the velocity of the rain and the car with respect to the Earth respectively, and $v_{rc}$ the velocity of the rain with respect to the car. Then $v_{car} = 50\ km\ h^{-1}$. Then $v_{rc} = \frac{50}{\sin 60^{\circ}} = 57.7\ km\ h^{-1}$ and $v_{rain} = \frac{50}{\tan 60^{\circ}} = 28.9\ km\ h^{-1}$.

## Example 3 - Relative Velocity

Two swimmers, Alan and Beth, start together at the same point on the bank of a wide stream that flows with a constant speed $v$. Both moves at the same speed $c > v$ relative to the water. Alan swims downstream a distance $L$ and then upstream the same distance. Beth swims such that her motion relative to the Earth is perpendicular to the banks of the stream. She swims the distance $L$ and then back the same distance, so that both swimmers return to the starting point. Which swimmer returns first?

### Solution

For Alan, $L = (c + v)t_{downstream}$ and $L = (c - v)t_{upstream}$. $t_{Alan} = t_{downstream} + t_{downstream} = \frac{L}{c + v} + \frac{L}{c - v} = \frac{\frac{2L}{c}}{1 - \frac{v^2}{c^2}}$.

For Beth, $2L = (\sqrt{c^2 - v^2})t_{Beth}$ and $t_{Beth} = \frac{\frac{2L}{c}}{\sqrt{1 - \frac{v^2}{c^2}}}$. Since $c > v$ and $\sqrt{1 - \frac{v^2}{c^2}} < 1$, Beth returns first.

## Example 4 - Relative Velocity solved with Vectors

A man traveling East at 8 $km\ h^{-1}$ finds the wind seems to blow from the North. On doubling his speed his finds that it seems to come NE. Find the velocity of the wind.

### Solution

Let $w = xi + yj$ be the velocity of the wind relative to the Earth. Then $w - 8i = (x - 8)i + yj = yj$, hence $x = 8$. Also $w - 16i = -8i + yj$ buy $y = -8$. Therefore $w = 8i - 8j$ and $w = 8\sqrt 2\ km\ h^{-1}$

## Example 5 - Relative Velocity solved with Geometry

At a particular instant, ship A is travelling due North at 30 $km/h$ and ship B is at a certain distance N60$^{\circ}$W from A. Ship B is travelling at constant velocity in direction N45$^{\circ}$E. The two ships finally met. What is the magnitude of velocity of ship B?

### Solution

We choose the coordinates such that ship A and B have the same $y$ position. Then $v_B\cos(60^{\circ} + 45^{\circ} - 90^{\circ}) = 30\cos 30^{\circ}$ and hence $v_B = 26.9\ m\ s^{-1}$.

## Example 6 - Relative Velocity with Geometry

Ship A is steering at a course N60$^{\circ}$W at 30 $km/h$. At a certain instant, ship B is 20 $km$ due west of ship A and is moving with constant speed of 10 $km/h$. Find the shortest possible distance between ship A and B.

### Solution

Take Ship A as the reference frame. Let $-v_a$ be the opposite vector of the velocity of ship A, $v_b$ the velocity of ship B and $v_{ba}$ be that respect to ship A. We choose $v_b$ such that $v_{ba} = v_b - v_a$ is tangent to the circle with radius $v_b$ with center $(v_a, -30^{\circ})$. Let $\theta$ be the angle between $v_{ba}$ and $-v_a$. Then $\theta = \arcsin \frac{10}{30} = 19.5^{\circ}$. Let $\psi$ be the angle between $AB$ and $v_{ba}$. Then $\psi = 30^{\circ} - 19.5^{\circ} = 10.5^{\circ}$. Let $BP$ be the line ship B travels along abd $AQ$ such that it is perpendicular to line $BP$ and is the shortest possible distance between ship A and B. Then $AQ = 20\sin 10.5^{\circ} = 3.65\ km$.

## Example 7 - Relative Velocity solved with Geometry and Sine Law

A boat A is travelling to B on the opposite bank of a river. B is at a downstream distance of 30 $m$ from A and the width of the river is 40 $m$. The speed of water flow of the river is 5 $m/s$ and the speed of the boat relative to still water is 4.5 $m/s$. If $\theta$ the steering angle of boat A upstream is constant, find its possible values.

### Solution

Let $v_a$ be the velocity of boat A, $v_w$ the velocity of the water and $v_{aw}$ that of boat A with respect to the water. Then we choose $v_a$ such that $v_{aw} = v_a + v_w$ is along $AB$. Let $\theta$ be the angle between $v_{aw}$ and $v_w$. Then $\theta = \arctan \frac{40}{30} = 53.1^{\circ}$. Let $\alpha$ be the angle between $v_{aw}$ and $v_a$. Then $\sin \theta = 0.8$. By sine law, $\frac{\sin \alpha}{5} = \frac{0.8}{4.5}$. Then $\alpha = 62.7^\circ$ or $\alpha = 117^\circ$. Afterall $\theta = 64.2^\circ$ or $\theta = 9.9^\circ$.

## Example 8 - Relative Velocity solved with Geometry

A swimmer wishes to across a swift, straight river of width $d$. The speed of the swimmer in still water is $u$ and that of the water is $v$, where $v > u$. If the swimmer wants to cross the swift river with a minimum time, find the minimum time and position that he reaches in the opposite bank. Also, what is the direction along which the swimmer should proceed such that the downstream distance he has traveled when he reaches the opposite bank is the smallest possible? What is the corresponding time required.

### Solution

The swimmer swims in the direction of $j$ to achieve a minimum time $t_{min}$. Then $d = ut_{min}$ and $t_{min} = \frac{d}{u}$. Then the x-component of the velocity of the swimmer is $v$. Let $s$ be the displacement of the swimmer. Then $s = vt_{min} = \frac{dv}{u}$.

Let $v_s$ be the velocity of the swimmer in the river. We choose $v_s = u + v$ such that $v_s$ is tangent to the circle produced with radius $u$ and center at $(v, 0^\circ)$. Let $\theta$ be the angle between $v$ and $v_s$ such that it points to the direction along which the swimmer should proceed such that the downstream distance is minimum. Then $\theta = \arcsin \frac{u}{v}$. Let $s_{min}$ be the minimum downstream distance. Then $s_{min} = d\cot \theta$, where $\cot \theta = \frac{v_s}{u} = \frac{\sqrt{v^2 - u^2}}{u}$. Therefore, $s_{min} = \frac{d\sqrt{v^2 - u^2}}{u}$.

Let $v_y$ be the y-component of the velocity of the swimmer. Then $v_y = u\cos \theta = \frac{u\sqrt{v^2 - u^2}}{v}$. Since $d = v_yt$, then $t = \frac{vd}{u\sqrt{v^2 - u^2}}$.

## Example 8 - Linear Relative Motion

A bus is moving with a speed of 10 $m\ s^{-1}$ on a straight road. A scooterist wishes to overtake the bus in 100 $s$. If the bus is at a distance of 1 $km$ from the scooterist, with what speed should the scooterist chase the bus?

### Solution

Let $v$ be the speed of the scooterist as required. Take the reference frame of the bus. Then $1000 = (v - 10) \times 100$. Therefore $v = 20\ m\ s^{-1}$.

## Example 9 - Linear Relative Motion

The distance between two spots A and B on the same bank of the river is 75 $km$. Speed of the boat in still water is twice as much as that of the speed of the water current of the river. The boat travels in the river from A to B and returns to the original spot in 16 hours. What is the speed of the boat in still water.

### Solution

Let $u$ be the speed of the water current such that the speed of the boat in still water is $2u$. Then $\frac{75}{2u + u} + \frac{75}{2u - u} = 16$ and $u = 6.25\ km\ h^{-1}$. Therefore the speed of the boat is $12.5\ km\ h^{-1}$.

## Example 10 - Relative Velocity solved with Sine Law

An aircraft, whose speed in still air is 300 $km\ h^{-1}$, flies in a straight line from R to S. The bearing of $S$ from $R$ is 195$^\circ$. There is wind blowing from the east. The pilot needs to set a course due south to go to S. Suppose the wind remains unchanged. Find the direction of course the pilot needs to set to go back from S to R.

### Solution

Let $v_w$ be the velocity of the wind. Then $v_w = 300\tan 15^\circ = 80.4 km\ h^{-1}$. Let $u$ be the velocity of the aircraft in still air and $v_{SR} = u + v_w$ be that from S to R. Let $\theta$ be the angle between $u$ and $v_{SR}$. Then by sine rule, $\frac{\sin \theta}{300\tan 15^\circ} = \frac{\sin 105^\circ}{300}$. Therefore $\theta = 15^\circ$ and the direction of course is $N30^\circ E$.

## Example 11 - Relative Velocity solved with Geometry and Sine Law

An aeroplane A is flying horizontally due north at 500 $km/h$. An enermy aeroplane B is at the same height and flying due east at 400 $km/h$. Find the velocity of aeroplane B relative to A. Also at a certain moment, B is directly ahead of A. In which direction should A aim its machine gun? Its bullet travels at 300 $m/s$ as seen by pilot of A. Ignore air resistance.

### Solution

Let $v_a$ and $v_b$ be the velocity of A and B respectively. Then $v_{ba} = v_b - v_a$ is the velocity of B relative to A. Therefore $v_{ba} = \sqrt{400^2 + 500^2} = 640\ km\ h^{-1}$.

Take the reference frame of aeroplane A. Let $\theta$ be the angle between $v_{ba}$ and $v_b$. Then $\theta = \arctan \frac{500}{400} = 51.3^\circ$. Then aeroplane B is flying at the direction of $51.3^\circ SE$. Let $v_m$ be the velocity of the bullet fired from the machine gun. Then $v_m = 1080\ km\ h^{-1}$. Choose $v_m$ such that it forms a triangle with $v_{ba}$ and $AB$. Let $\psi$ be the angle between $AB$ and $v_m$. Then by sine rule, $\frac{\sin \psi}{640} = \frac{\sin 38.7}{1080}$. Therefore $\psi = 21.7^\circ$ and the pilot of A should aim its machine gun in the direction $N21.7^\circ E$.

## Example 12 - Relative Velocity solved with Geometry

A ship A is steering at a course $N60^\circ W$ at 30 $km/ h^{-1}$. At a certain instant, a second ship B is 20 $km$ due west of ship A and is moving with a constant speed of $15\sqrt{2}$km h^{-1}$. Find the earliest possible time that ship B can reach the ship A.

### Solution

Take the reference frame of ship A. Let $v_a$ and $v_b$ be the velocity of ship A and B. Choose $v_b$ such that $v_{ba} = v_b - v_a$ the velocity of ship B with respect to A is due east. Let $\theta$ be the angle between $AB$ and $-v_a$. Then $\theta = 30^\circ$. Let $\psi$ be the angle opposite to $v_{a}$. Then by sine rule, $\frac{\sin \psi}{30} = \frac{\sin 30^\circ}{15\sqrt{2}}$. Then $\psi = 45^\circ$. Then $v_{ba} = 30 \cos 30^\circ + 15\sqrt{2} \cos 45^\circ = 41.0\ km\ h^{-1}$. Let $t_{min}$ be the minimum time. Therefore $20 = 41.0t$ and $t = 0.488 hr$.

## Example 13 - Relative Velocity solved with Sine and Cosine Rule

Ship A is 10 $km$ due west of ship B. Ship A is heading directly north at a speed of 30 $km/h$ while ship B is heading in a direction $60^\circ$ west of north at a speed of 20 $km/h$. What is the relative velocity of ship B with respect to A? What will the shortest possible distance between ship A and B?

### Solution

Take reference frame of ship A. Let $v_a$ and $v_b$ be the velocity of ship A and B respectively such that $v_{ba} = v_b - v_a$ is the velocity of A with respect to B. Then by consine rule $v_{ba} = \sqrt{20^2 + 30^2 - 2(20)(30)\cos 60^\circ} = 26.5\ km\ h^{-1}$. Let $\theta$ be the angle opposite of $v_{b}$. Then by sine rule $\frac{\sin \theta}{20} = \frac{\sin 60^\circ}{26.5}$, and $\theta = 40.8^\circ$. Let $d$ be the minimum distance. Then $d = 10\sin 49.2^\circ = 7.57\ km$.
