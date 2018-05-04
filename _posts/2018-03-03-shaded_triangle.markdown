---
layout: post
title:  "Shaded Triangle Problem"
date:   2018-03-03 12:49:00
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
\begin{align*}
h(x) &= \alpha x,
\end{align*}
$$

where $\alpha$ is some constant. In that case, the proportion of area that is shaded, say $A$, can be expressed as

$$
\begin{align}
A &= 1  \\
&= 2 \\
& = 3 \label{eq:1}
\end{align}
$$

