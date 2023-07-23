---
layout: post
title: Grasshopper and Dominoes
date_: 22 July 2023
tags: probability counting
---

#### Q1
A grasshopper is sitting on a little stone, which we'll call stone zero. Ahead of him, arranged in a line, are stones, one, two three, et cetera, all the way up to nine.

The grasshopper would like to reach that ninth stone, for reasons unknown. What we do know is that he'll get there by combining little grasshopper jumps, each of which will take our friend forward by either one or two steps. To be clear, this means the grasshopper has exactly two ways to reach stone two: he could take one big jump, or two little ones.

How many different paths can the grasshopper take to reach his destination?

<details>
    <summary>
        Answer
    </summary>
    <p>
    Immediately, you can try $1+1+...+1 = 2 + 1 + 1 + ... + 1 = 9$. In fact, any sequence be described with just a string of $1$'s and $2$'s.
    </p>

    <p>
    Given a fixed number of $2$'s, the problem becomes really easy. For example, say there are four $2$'s that must be used. Then, the number of possible jumps using that number of $2$'s is $\text{nCr}(4+1, 4) = \text{nCr}(5, 4)$. See the Mississippi problem/formula (and application on an n-bit string) for more information.
    </p>

    <p>
    So we can just partition based on the number of $2$'s used: 
    </p>

    <p>
    $$
    \begin{align*}
    \text{#(possible jump sequences)} = &\text{ #(use zero 2 jumps)}\\ &+ \text{#(use one 2 jump)}\\ &+ \text{#(use two 2 jumps)}\\ &+ \text{#(use three 2 jumps)}\\ &+ \text{#(use four 2 jumps)}
    \end{align*}
    $$
    </p>
</details>

#### Q2
How many ways are there to be a tile a 2-by-10 board with 2-by-1 dominoes?

The rules are simple: your tiling must cover the board perfectly; no dominoes can stick out; and they can't overlap.


![An example of a tiling of dominoes](image.png)

<details>
    <summary>
        Answer
    </summary>
    <p>
    It might help to try and solve the previous puzzle, since you can reduce this problem into that.
    </p>

    <p>
    Observation: horizontal pieces come in pairs. So if you know that there's a horizontal piece on the top, there must be a horizontal piece on the bottom. Along with the fact that a vertical piece covers both the top and bottom, one possible idea is to only look at the top, since you can imagine what the rest of the board will look like given only the top information.
    </p>

    <p>
    So let's only look at the top row. Each vertical piece covers 1, and each horizontal piece covers 2. Some combination of these must add up to the 10 pieces. See puzzle 12 for the rest of the solution.
    </p>
</details>