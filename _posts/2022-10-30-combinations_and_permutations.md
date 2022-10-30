---
layout: post
title:  "Permutations"
date:   2022-10-30 12:00:11 -0400
categories: math
---
Don't fear the big words! They have very simple meanings.
A permutation is an arrangement of items from a set or list.

For example, if you have a list of numbers $$(1, 2, 3, 4)$$ than a permutation
of this list would be $$(2, 1, 3, 4)$$ or $$(3, 1, 2, 4)$$ or $$(4, 3, 2, 1)$$.
Any different ordering of the original set items is a permutation.

The ordering doesn't have to contain all elements. You can make permutations of only
2 items from the set. For example, $$(1, 2)$$, $$(1, 3)$$, and $$(2, 3)$$ are each
permutations as well.

You may also see the notation $$nPr$$ around. This just means that you're looking
at a set that contains $$n$$ elements and you want to create permutations using
$$r$$ items.

The original example I gave above would be $$4P4$$ since I made permutations of a
set of size $$n = 4$$ and permutations of size $$r = 4$$.

Also the second example uses 2 elements. So the size of the set is still $$n = 4$$
and my permutations are of size $$r = 2$$. So the notation would be $$4P2$$

## Deeper Analysis
Now that you know what permutations are, (very simply, just different arrangements
of a set or subset), let's look more closely at them.

Using the basic set $$(1, 2, 3, 4)$$, how many different arrangements of this can
we make? We could list them all out and count them, but there is really a much more
clever way to count them.

We must choose any one of the elements for our first value. So we have 4 options
to start with. Let's choose 1. Now for the second item in our arrangement, we only
have 3 options left to choose from $$(2, 3, 4)$$. After picking one at random, let's say 3. Now we only have 2 options left $$(2, 4)$$. Every time we pick one the options
we have remaining reduces by one. The first time we have 4, then we have 3, and then
2, and then at the end we only have 1 to choose from.

If we start with 4 elements. Each of those 4 elements has 3 options for the next element.
Then each of those 12 options has 2 options for the 3rd element.

So the total number of permutations is $$4 * 3 * 2 * 1$$. In fact for any set of 4 unique
items, the number of permutations is $$4 * 3 * 2 * 1$$ whether it's numbers, birds,
or friends. There are 24 different ways to arrange them.

The mathematical notation for this $$4 * 3 * 2 * 1$$ is $$4!$$

And for any list of size $$n$$, the number of permutations for all the elements is $$n!$$

### Subsets
We can take the same idea if we only want to take 2 elements from the list we can do that too.
Back to our $$(1, 2, 3, 4)$$ list we can arrange 2 elements. For the first of our 2 we have 4
options, and for the second we have 3 remaining options. So the result is 12 options.
Or $$4P2 = 12$$

There is a more clever way to do this as well. If we analyze what we're doing we see something like this.

$$\begin{align}
Option\ 1\ &= (n)\\
Option\ 2\ &= (n - 1)\\
...\\
Option\ r\ &= (n - r + 1)\\
nPr &= (n) * (n-1) * ... * (n-r+1)
\end{align}$$

Try it out! If we have 5 elements and want to choose 3, then we get:

$$\begin{align}
n &= 5\\
r &= 3\\
nPr &= (5)(5-1)(5-2)
\end{align}$$

We stop at $$5 - 2$$ because $$(n - r + 1) = (5 - 3 + 1) = (5 - 2)$$
Which is the same as saying first we have 5 options, then 4 options, then 3 options.

Now the final formula you'll see around is this:

$$nPr = \frac{n!}{(n - r)!}$$

We can prove this easily. Take the reasoning we used above.

$$
nPr = n * (n-1) * (n-2) * ... * (n - r + 1)
$$

If we expand this equation the way out even further, we actually just end up with $$n!$$

$$
n! = n * (n-1) * (n-2) * ... * (n - r + 1) * (n - r) * (n - r - 1) * (n - r - 2) * ... * (2) * (1)
$$

Since this is just a bunch of multiplication, we can can easily see that starting from $$(n - r)$$ all the way to $$(1)$$ is
in fact $$(n - r)!$$.

So if we want $$nPr$$ we can divide by $$(n - r)!$$ to cancel all of those terms.

$$
nPr = \frac{n * (n-1) * (n-2) * ... * (n - r + 1) * (n - r) * (n - r - 1) * (n - r - 2) * ... * (2) * (1)}{(n - r) * (n - r - 1) * (n - r - 2) * ... * (2) * (1)} = \frac{n!}{(n - r)!}
$$
