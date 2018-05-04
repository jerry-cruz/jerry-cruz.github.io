---
layout: post
title:  "Shaded Triangle Problem"
date:   2018-05-03 12:49:00
categories: geometry
---

I first became aware of this problem through the article in this tweet (it came up on my google newsfeed):
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">😂&quot;That damn pink triangle&quot; <a href="https://t.co/0HIQDqo3tB">https://t.co/0HIQDqo3tB</a></p>&mdash; Ed Southall (@solvemymaths) <a href="https://twitter.com/solvemymaths/status/990201229094645760?ref_src=twsrc%5Etfw">April 28, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

It didn't seem that hard despite "Stumping the Internet" so I decided to try to solve it from first principles. I came up with a solution using the fractal nature of the problem. I thought it was clever so I wrote it up. Here it is.

# Problem Statement
Find the proportion of area that is shaded in the figure:

<p align="center">
    <img src="https://raw.githubusercontent.com/jerry-cruz/jerry-cruz.github.io/master/_posts/shaded_triangle_images/shaded.png">
    <br>
    Figure 1. The enclosing shape is a perfect square and the line coming from the lower left corner cuts the top edge of the square in half.
</p>

# Solution
Let $x$ be the length of one side of the square and $h$ be the height of the leftmost triangle. See Figure 2.

<p align="center">
    <img src="https://raw.githubusercontent.com/jerry-cruz/jerry-cruz.github.io/master/_posts/shaded_triangle_images/shaded_1.png">
    <br>
    Figure 2. Variable definitions.
</p>

For the moment, assume that $h$ can be expressed as a linear function of $x$:

$$
\begin{align}
h(x) &= \alpha x, \label{eq:1}
\end{align}
$$

where $\alpha$ is some constant. In that case, the proportion of area that is shaded, say $A$, can be expressed as

$$
\begin{align}
A &= \frac{\frac{x^2}{2} - \frac{xh}{2}}{x^2}  \nonumber \\
&= \frac{\frac{x^2}{2} - \frac{\alpha x^2}{2}}{x^2} \nonumber \\
& = \frac{1-\alpha}{2}. \label{eq:2}
\end{align}
$$

Thus, we need only to show that $h$ is in fact a linear function of $x$ and find the value of $\alpha$.

## Finding $h$
Divide the square in Figure 1 evenly into four quadrants. See Figure 3.

<p align="center">
    <img src="https://raw.githubusercontent.com/jerry-cruz/jerry-cruz.github.io/master/_posts/shaded_triangle_images/divide_1.png">
    <br>
    Figure 3. Evenly divided into four quadrants.
</p>

The square on the top left resembles the statement of the original problem, just on a smaller scale. In fact, the top left square is an inverted version of the original problem scaled by one fourth. Divide this (top-left) square into four quadrants. See Figure 4.

<p align="center">
    <img src="https://raw.githubusercontent.com/jerry-cruz/jerry-cruz.github.io/master/_posts/shaded_triangle_images/divide_2.png">
    <br>
    Figure 4. Top-left evenly divided into four quadrants
</p>

The square labeled $s$ in the resulting figure (Figure 4) is exactly the original problem scaled by one sixteenth. Thus, the problem is fractal (i.e. exhibits self-similarity). We will use this fact to find $h$.

We can express $h$ as 

$$
\begin{align}
h &= \frac{1}{4}x + h', \label{eq:3}
\end{align}
$$

where $h'$ is the length in $s$ that corresponds to $h$ in the original problem; i.e. it is the scaled version of $h$. See Figure 5.

<p align="center">
    <img src="https://raw.githubusercontent.com/jerry-cruz/jerry-cruz.github.io/master/_posts/shaded_triangle_images/h_form.png">
    <br>
    Figure 5. Illustrates equation $\eqref{eq:3}$
</p>

Now, since $s$ is exactly the same problem, only scaled, we can express $h'$ as

$$
\begin{align}
h' &= \frac{1}{4}x' + h'' \label{eq:4}
\end{align}
$$

where $x'$ corresponds to the scaled version of $x$, and $h''$ corresponds to $h'$ in an even smaller version of the original problem, call it $s'$ (not shown in the figures). From the figure it is easy to see that $x'=\frac{1}{4}x$, so we can write \eqref{eq:4} as

$$
\begin{align*}
h' = \left(\frac{1}{4}\right)^2 x + h''.
\end{align*}
$$

Using this equation, we can write \eqref{eq:3} as

$$
\begin{align*}
h = \frac{1}{4}x + \left(\frac{1}{4}\right)^2 x + h''.
\end{align*}
$$

Now, as mentioned above, h'' corresponds to another fractal version of the original problem, so we can apply the same reasoning to get 

$$
\begin{align*}
h = \frac{1}{4}x + \left(\frac{1}{4}\right)^2 x + \left(\frac{1}{4}\right)^3 x + h'''.
\end{align*}
$$
 
We can continue this proccess indefinitely (since the problem is fractal), and so (using mathematical induction) we can conclude that

$$
\begin{align*}
h = x\sum_{i=1}^\infty\left(\frac{1}{4}\right)^i.
\end{align*}
$$

This sum represents a geometric series and so converges to

$$
\begin{align*}
h &= x\sum_{i=1}^\infty\left(\frac{1}{4}\right)^i \\
&= x\left(\frac{1}{1-\frac{1}{4}} - 1 \right) \\
&= \frac{1}{3}x.
\end{align*}
$$

Thus, we have shown that $h$ is a linear function of $x$ with $\alpha=\frac{1}{3}$. Using \eqref{eq:2} from the first part of the solution, we have that the proportion of area that is shaded is

$$
\begin{align*}
A = \frac{1-\alpha}{2} = \frac{1-\frac{1}{3}}{2} = \frac{1}{3}
\end{align*}
$$

## Discussion
Although the solution was written very informally, it can be made as mathematically rigorous as needed. Moreover, this is not the only solution method; and it may not necessarily be the "simplest" (e.g. use facts regarding similar triangles). It, however, uses very few facts:

1. Symmetry (not explicitly stated in the solution above) to deduce that the problem is fractal
2. Fractality to derive an algebraic expression
3. Knowledge of the closed form expression for the sum of an infinite geometric series

Because of 3, the above solution is not exactly entirely from first principles, but deriving 3 is not difficult (see [geometric series formula](https://en.wikipedia.org/wiki/Geometric_series#Formula)).

Another appealing aspect of the solution method is that self-similarity can actually be used to help solve the problem (and not to just sound smart or draw pretty pictures).

<p align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/2/21/Mandel_zoom_00_mandelbrot_set.jpg">
</p>

