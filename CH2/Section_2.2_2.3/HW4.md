# Homework 4

Mark Archual | MTH 515

Dr. Scott | Real Analysis

2/13/19

## Problem 2.2.2

### Original Solution

#### _Part A_

$\lim \frac{2n+1}{5n+4} = \frac{2}{5}$

> Rough Work

$$\lvert \frac {2n+1}{5n+4} - \frac{2}{5} \rvert < \epsilon$$
$$\lvert \frac {2n+1 - 2(n+4)}{5n+4} \rvert < \epsilon$$
$$\lvert \frac {2n+1 - 2n - 8}{5n+4} \rvert < \epsilon$$
$$\lvert \frac {-7}{5n+4} \rvert < \epsilon$$

Notice then that

$$\frac {1}{5n+4} < \frac {1}{5n}$$

Solving for epsilon

$$\frac{7}{5n} < \epsilon$$
$$\frac{7}{5 \epsilon} < n$$

> Formal Proof

Let $\epsilon > 0$ be arbitrary
Let $N \in \mathbb{N}$ be greater than $\frac {7}{5 \epsilon}$
Suppose $n \geq N$, then

$$\lvert \frac {2n+1}{5n+4} - \frac{2}{5} \rvert = \frac {7}{5n} \leq \frac {7}{5N} < \frac{7}{5 \frac{7}{5 \epsilon}} = \epsilon$$

#### _Part B_

$\lim \frac{2n^2}{n^3+3} = 0$

> Rough Work

Denominator

$$n^3 + 3 > n^3$$

so

$$\frac{1}{n^3 + 3} < \frac{1}{n^3}$$

Numerator

$$2n^2 > n^2$$

so

$$\lvert \frac{2n^2}{n^3+3} \rvert < \frac{2n^2}{n^3}$$
$$\frac{2}{n} < \epsilon$$
$$n>\frac{2}{\epsilon}$$

> Formal Proof

Let $\epsilon > 0$ be arbitrary
Let $N \in \mathbb{N}$ be greater than $\frac{2}{\epsilon}$

Suppose $n \geq N$, then

$$\lvert \frac{2n^2}{n^3+3} \rvert < \frac{2n^2}{n^3} < \frac{2}{n} \leq \frac{2}{N} < 2*\frac{\epsilon}{2} =  \epsilon$$

#### _Part C_

$lim \frac{\sin(n^2)}{\sqrt[3]{n}} = 0$

> Rough Work

Numerator: Notice that $\sin(n^2)$ is bounded by 1.  So $\sin(n^2) < 1$

This simplifies the problem to

$$\frac{1}{\sqrt[3]{n}} < \epsilon$$
$$\frac{1}{n} < \epsilon^3$$
$$\frac{1}{\epsilon^3} < n$$

> Formal Proof

Let $\epsilon > 0$ be arbitrary
Let $N \in \mathbb{N}$ be greater than $\frac{1}{\epsilon^3}$

$$\lvert \frac{\sin(n^2)}{\sqrt[3]{n}}\rvert < \frac{1}{\sqrt[3]{n}} \leq \frac{1}{\sqrt[3]{N}} \frac {1}{\sqrt[3]{\frac{1}{\epsilon^3}}} = \epsilon$$


### Self-Evaluation

#### Part A
Basic algebra issues are my achilles heel.  I have the wrong common denominator here.

#### All
To fully complete each proof I should have restated the limit of each expression.

## Problem 2.2.6

### Original Solution

If $(a_n) -> a$, then, by the definition of convergence $\exists N_1 \in \mathbb{N}$ for $n \geq N_1$

$$\lvert a_n - a \rvert < \frac{\epsilon}{2}, \forall \epsilon > 0$$

If $(a_n) -> b$, then, by the definition of convergence $\exists N_2 \in \mathbb{N}$ for $n \geq N_2$

$$\lvert a_n - b \rvert < \frac{\epsilon}{2}, \forall \epsilon > 0$$

Using the triangle inequality

$$ \lvert a_n - a \rvert + \lvert b - a_n \rvert \geq \lvert a_n - a + b_n - b \rvert \geq \lvert b - a \rvert$$
$$\lvert b - a \rvert < \epsilon \space \forall \epsilon > 0$$

Therefore $b = a$, otherwise if $b \neq a$, then an $\epsilon$ may be found such that $\epsilon < b-a < \epsilon$, which is not possible.

### Self-Evaluation

My solution follows the one given, but I should have specified that $n = max(N_1, N_2)$. 

## Problem 2.3.3

### Original Solution

By the Order Limit Theorem if $a_n \leq b_n \forall n$ then $a \leq b$.  Applying this idea here, we have

$$x_n \leq y_n$$

so $l \leq y$.  Similarly 

$$y_n \leq z_n$$

so $y \leq l$.  Notice then that

$$l \leq y \leq l$$

Thus $l = y$

### Self-Evaluation

Looks like I fell into a pretty common mistake here by trying to apply the Order Limit Theorem.  Reviewing the problem statement, I see that there was no information given to prove that $y$ converges.  Looking at the solution though, I can see that I was thinking about the problem correctly.  I was trying to work with idea that if you know a limit is located between two other limits, both of which have the same value, then the only solution must be that all limits are equal.  The difference here being that you can find the limit of the differences between the sequences, and not the sequences themselves.

## Problem 2.3.7

### Original Solution

#### _Part A_

Let $(x_n) = \sin(x_n)^2$, and $(y_n) = \cos(y_n)^2$.

Both sequences oscillated between 0 and 1, however their sum is 1 for all values of n.

#### _Part B_
This is not possible by tenant (ii) of the Algebraic Limit Theorem.  If $(y_n)$ diverges, then it is not possible that $(x_n) + (y_n)$ converges, as it would contradict the assumption of the A.L.T. that each sequence must converge.

#### _Part C_
Let $(b_n) = \frac{1}{x_n}$ then $\frac{1}{b_n} = x_n$, which diverges.

#### _Part D_
This is not possible.  If $(a_n)$ is unbounded, then $(a_n - b_n)$ is unbounded as well, as it would be impossible to find a value that satisfies the definition of boundedness for this difference.

#### _Part E_
$(a_n) = \frac{1}{\sqrt{x_n}}$ and $(b_n) = \sqrt{x_n}$ then
$(a_n * b_n) = 1$ which converges.

### Self-Evaluation

#### Part D

My answer here lacks some depth in its explanation, even though my intuition is correct.  I think I struggled trying to motivate a more thorough explanation here because the idea seemed obvious to me.  After reviewing the solution, I like how the triangle inequality was used to express why $a_n$ has to be bounded.

## Problem 2.3.9

### Original Solution

If the $\lim b_n = 0$, then the expression $\lim(a_n*b_n) = 0$ because if we know that all of the possible values of the sequence $(a_n)$ fall within a definable range it will follow the convergence of $(b_n)$ to 0.  If $a_n$ was not bounded, this could not be guaranteed.

We cannot use the Algebraic Limit Theorem because it assumes that the sequence $(a_n)$ converges.

### Self-Evaluation
My answer for why $(a_n*b_n)$ converges I feel verbally matches the relationships shown in the solution, granted the solution is much more well quantified.  I think one way I could have improved upon my answer was discussing the relationship between the limits for $b_n$ and $a_n$.  This would expand upon my answer, where I state 'it will follow the convergence to 0', without giving the details.

## External References
