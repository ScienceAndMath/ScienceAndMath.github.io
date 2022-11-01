---
layout: post
title:  "Moon's Gravity"
date:   2022-10-31 21:55:00 -0400
categories: science
---
This is question 3.4 from [_Exercises for the Feynman Lectures on Physics_](https://archive.org/details/exercises-for-the-feynman-lectures-on-physics-etc.-z-lib.org).

The radii of the earth and the moon are 6378km and 1738km respectively, and their masses are in the ratio of 81.3 to 1. Calculate the acceleration g of the moon at the surface of the moon.

# Solution
To solve this you need to combine Newton's 2nd law and the force of gravity $$\begin{align}F &= G\frac{m_1m_2}{r^2}\\F &= ma\end{align}$$

We're looking exclusively at the gravitational force. At the surface of the earth, the radius is just the radius of the earth. The same goes for the moon, at the surface of the moon, the radius is the radius of the moon. This gives us the following equations

$$\begin{align}
F = ma_{earth} &= G\frac{M_{earth}m}{r_{earth}^2}\\
F = ma_{moon} &= G\frac{M_{moon}m}{r_{moon}^2}
\end{align}
$$

If we solve for acceleration, then the mass of the imaginary object the force is being acted on cancels out. That is when solving for $a$, the $m$ gets divided away. So we're left with:

$$\begin{align}
a_{moon} &= G\frac{M_{moon}}{r_{moon}^2}\\
a_{earth} &= G\frac{M_{earth}}{r_{earth}^2}
\end{align}
$$

Now, we're not given the masses directly, but we do know the proportions of the mass. We're given the mass of the earth compared to the moon is 81.3. Mathematically that is 

$$\frac{M_{earth}}{M_{moon}} = 81.3$$

So, let's divide these equations so that we can take advantage of that proportion.

$$
\frac{a_{moon}}{a_{earth}} = \frac{M_{moon}}{M_{earth}}\frac{r_{earth}^2}{r_{moon}^2}
$$

The G's cancel, and the division results in the radius squared of the moon divided by the radius squared of the earth. Double check this yourself. We can now plug in all the terms we know and solve for the moon. Make sure to use the radii in meters, which results in the $10^3$, since the earth gravity 9.8 is in meters per second per second.

$$
\frac{a_{moon}}{9.8} = \frac{1}{81.3}\frac{(6378*10^3)^2}{(1738*10^3)^2}
$$

Math it all out and you get

$$a_{moon} = 1.6233\ ms^{-2}$$

This is about 1/6 of the earth's gravity.
