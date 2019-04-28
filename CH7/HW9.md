# Homework 9

Mark Archual | MTH 515

Dr. Scott | Real Analysis

4/17/19

## Problem 7.2.4

### Original Solution

The upper sum of $g$ is equal to the lower sum so $\inf(g, P) = \sup(g, P)$.  If the infimum of a function is equal to the supremum, the the function's value is constant across its domain.

$g$ is integrable.  The criterion for Riemann Integrability requires that $U(g, P) - L(g, P) < \epsilon$  In this case, $U(g, P) - L(g, P) = 0$ so $g$ is Riemann Integrable.

The value of $\int^b_a g(x) = \gamma*(b-a)$ where $\gamma$ is the constant value of the function, $g$.

### Self-Evaluation

My solution agrees with the one presented.

## Problem 7.2.6

### Original Solution

If $f$ satisfies the given definition, then

$$L(f, P_o) \leq R(f, P_o) \leq U(f, P_o)$$

because $m_k \leq c_k \leq M_k$.  This means that $P_o$ is the result of a common refinement, so $\exists$ partitions, $P_1, P_2$ s.t. $P_o = P_1 \cup P_2$.  It then follows that for these partitions,

$$U(f, P_1) \leq U(f) + (\frac{\epsilon}{2} - A)$$
$$L(f, P_2) \geq L(f) + (\frac{\epsilon}{2} - A)$$

Then $\ldots$

$$U(f, P_o) - L(f, P_o) \leq U(f, P_1) - L(f, P_2) < U(f) + (\frac{\epsilon}{2} - A) - (L(f) + (\frac{\epsilon}{2} - A)) < U(f) - L(f) + \frac{\epsilon}{2} + \frac{\epsilon}{2}$$

By definition 7.2.7 we know $U(f) - L(f) = 0$ so the above expression reduces to

$$U(f, P_o) - L(f, P_o) < \epsilon$$

$\therefore f$ is integrable.

### Self-Evaluation

I had the right idea here, but I think using the idea of a refinement was a little misguided.  I was trying to find a way to bound $U(f, P) - L(f, P)$ using $R(f, P)$ but I think that the additional partitions don't quite do that because $R(f, P)$ could simply be shifted based on the partition selected and then the relationships between the upper and lower sums wouldn't quite hold.


## Problem 7.3.2

### Original Solution

#### _Part A_

By the Axiom of Completeness we know that every rational number is "surrounded" by two irrational numbers.  Thus, for any partition, $P$, the $\inf(f(x)), x \in P = 0$

#### _Part B_

Part B I struggled with because I wasn't sure how to go about finding the size of the set.  I understood what values would be a part of the set, but I could not find a way to succinctly describe its size.  I felt like there was maybe some implied information about the set that could have helped me get there, but I had a hard time seeing it.

#### _Part C_

This part depends on the question before it, so I am also not able to provide a complete answer.  I can tell that the partition, $P_\epsilon$ depends on the insights gained into the set from part B as knowing when $t(x)$ exceeds $\frac{\epsilon}{2}$ would be key for understanding how to construct $P_\epsilon$.

### Self-Evaluation

#### _Part B_

I knew how to find what values of $x$ would be in the given set, but I mainly struggled with quantifying it.  I see how to do that now.

#### _Part C_

The solution presented makes sense.  I see that the key is really the selection of $\delta$, which would have been difficult to see without an insight into the answer from _Part B_.


## Problem 7.4.5

### Original Solution

#### _Part A_

$U(f + g, P) = \sum (M_k)\Delta x_k$, where $M_k = \sup(f(x) +g(x)))$

Then by the triangle inequality,

$$\sum \sup(f(x) + g(x))\Delta x_k \leq \sum \sup (f(x))\Delta x_k + \sum \sup(g(x))\Delta x_k = U(f, P) + U(g, P)$$ for some partition, P.

For lower sums, 

$$L(f+g, P) \geq L(f, P) + L(g, P)$$

The inequality is strict if f and g have counteracting behaviors over P.  For example, if f is monotonically decreasing while g is monotonically increasing.

#### _Part B_

$\int^b_a (f+g) = \int^b_a f + \int^b_a g$

$\int^b_a (f+g)$ implies that $U(f+g) = L(f+g)$ for some partition, P.

Then, using the relations found in _Part A_ $\ldots$

$$U(f, P) + U(g, P) \geq U(f+g, P) \geq L(f+g, P) \geq L(f, P) + L(g, P)$$

Because $f$ and $g$ are known to be integrable, 

$$U(f, P) = L(f, P)$$

and 

$$U(g, P) = L(g, P)$$

which implies that

$\int^b_a (f+g) = U(f+g, P) = L(f+g, P) = \int^b_a f + \int^b_a g$

### Self-Evaluation

My solution agrees with the one presented.

## Problem 7.4.8

### Original Solution

Using the Weierstrauss M-test, we see that 

$$ \lvert h_n(x) \rvert \leq \frac {1}{2^n} \forall x \in A$$.

The geometric sum $\sum \frac{1}{2^n}$ converges to 1, so $\sum h_n(x)$ converges uniformly to $H$ and is integrable.

$$\int^1_0 H = \sum \int^1_0 h_n(x) = \sum \frac{1}{2^n}*\frac{1}{2^n} = \sum \frac{1}{4^n} = \frac{1}{3}$$

### Self-Evaluation

My approach agrees with the solution, however we arrived at different answers for the integral.  I am pretty confident that my solution is correct and that the $(1-\frac{1}{2^n})$ term is incorrect.  Integrating $h_n$ given $(\frac{1}{2^n}*x)$.  Inserting the terms of integration, when x = 0, the whole term is zero, and when x = 1, an additional $\frac{1}{2^n}$ term is earned, as shown in my solution.


## External References
