# Homework 5

Mark Archual | MTH 515

Dr. Scott | Real Analysis

2/20/2019

## Problem 2.4.1

### Original Solution

#### _Part A_

Show the sequence is bounded and monotone.

>Monotone

$$x_2 = \frac{1}{4-3} = 1$$

Thus $x_2 < x_1$ and the induction is grounded.

$$x_{n+1} \leq x_n$$
$$4-x_{n+1} \geq 4-x_n$$
$$\frac{1}{4-x_{n+1}} \leq \frac{1}{4-x_{n}}$$

Thus $x_{n+1} \leq x_n$.  Inductive step complete and the sequence is decreasing.

>Bounded

Try $a_n > \frac{1}{4}$

$$a_1 = 3 > \frac{1}{4}$$

Suppose $a_n > \frac {1}{4}$ for some $n \geq 1$.

$$\frac{1}{4-a_n} > \frac{1}{4}$$

Thus the sequence is bounded.

#### _Part A_
A small mistake in the conclusion, I should have stated $x_{n+2} \leq x_{n+1}$

#### _Part B_
If $x_n$ exists, then we can use induction to show $x_{n+1}$ exists.  Alternatively, $x_{n+1}$ can be thought of as a subsequence of $x_n$ and because $x_n$ converges, $x_{n+1}$ converges as well.

#### _Part C_
$$lim{x_{n+1}} = lim{\frac{1}{4-x_n}}$$

Let $lim{x_{n+1}} = l$.

$$l = \frac{1}{4-lim{x_n}}$$

$$l = \frac{1}{4-l}$$

$$l(4-l) = 1$$
$$l^2 - 4l + 1 = 0$$
$$(l+2)^2 - 3 = 0$$
$$l = \sqrt{3} - 2$$

### Self-Evaluation

#### _Part B_
My answer here differs, but I believe the fact about subsequences would hold here and be correct.

#### _Part C_
Bad algebra mistake here on finding the square root. I was close!

## Problem 2.4.3

### Original Solution

#### _Part B_

Let $(a_n) = \sqrt{2}, \sqrt{2 \sqrt{2}}, etc.$

If $(a_n)$ converges, then it is bounded and monotone.

> $(a_n)$ is monotone

$$a_2 = \sqrt{2 \sqrt{2}} > \sqrt{2}$$

The induction is grounded.

Suppose by way of induction that

$$a_{n+1} > a_n$$

for some $n \geq 1$.

$$2*a_{n+1} > 2*a_n$$
$$\sqrt{2*a_{n+1}} > \sqrt{2*a}$$
$$a_{n+2} > a_{n+1}$$

Inductive step complete.


### Self-Evaluation

Somehow I neglected to include the evaluation of the limit for the sequence.  I have added my original work above.

## Problem 2.4.6

### Original Solution

#### _Part A_

For any two positive real numbers,

$$(x-y)^2 \geq 0$$

$$(x+y)^2 - 4xy \geq 0$$

$$(x+y)^2 \geq 4xy$$

$$(x+y) \geq 2 \sqrt{xy}$$
$$\frac{x+y}{2} \geq \sqrt{xy}$$

#### _Part B_
Part B I ran out of time and was a bit confused on.  I was not sure if the problem was telling me that the sequence values of the one limit, fed into the recursion of the other, or not.

### Self-Evaluation

#### _Part B_
I see that I was mistaken and that the terms of the two sequences do not interact with each other.  I think the book could have maybe done a better job here with the notation, but regardless I could have done some more critical thinking here.  I see that the key was utilizing the known relationships between $x_n$ and $y_n$ and using the MCT to know they converge.

## Problem 2.5.2

### Original Solution

#### _Part A_

This is true and is a result of Theorem 2.5.2.

#### _Part B_

This is false.  To be able to say that $(x_n)$ diverges, at least two divergent subsequences need to be found.

#### _Part C_

This is true and is a result of Theorem 2.5.2.

#### _Part D_

This is true and is a result of Theorem 2.5.5.

### Self-Evaluation

#### _Parts B and C_
I got parts B and C a little confused in my analysis.  I remebered us going over Part C in class, and I relied on that example a little too heavily for Part B.  In Part B, I was thinking too similarly and was thinking that the subsequence just converged to a different term than the overall sequence, not that it diverged all together.  This was a pretty bad error on my part, and I see why B is simply the contrapositive of Theorem 2.5.2.

Expanding on Part C, I could have given more background to my answer but I assumed that since it was stated pretty explicitly in the text that we could simply refer back to the claim that was made there.

#### _Part D_
Looks like I needed to read the question more carefully and see that the sequence was not bounded.  The solution presented makes sense.

## Problem 2.6.4

### Original Solution

#### _Part A_

Let $c_n = \lvert a_n - b_n \rvert$

If $a_n$ is cauchy, then $\forall \frac{\epsilon}{2} > 0, \exists N_1 \in \mathbb{N}$ s.t. for $m, n \geq N_1$

$$\lvert a_n - a_m \rvert < \frac{\epsilon}{2}$$

If $b_n$ is cauchy, then $\forall \frac{\epsilon}{2} > 0, \exists N_2 \in \mathbb{N}$ s.t. for $m, n \geq N_2$

$$\lvert b_n - b_m \rvert < \frac{\epsilon}{2}$$

Let $N = max(N_1, N_2)$, then $c_n$ is cauchy if for $n, m \geq N, \exists \epsilon > 0$ s.t.

$$\lvert c_n - c_m \rvert < \epsilon$$

$$\lvert c_n - c_m \rvert = \lvert \lvert a_n - a_m \rvert + \lvert b_n - b_m \rvert \rvert$$
$$\lvert c_n - c_m \rvert \leq \lvert a_n - a_m \rvert + \lvert b_n - b_m \rvert$$
$$\lvert c_n - c_m \rvert = \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

Thus $c_n$ is cauchy.

#### _Part B_

$c_n$ is not cauchy because it does not converge.  The odd and even terms will converge to different values.  For example if $a_n$ was $\frac{n}{n+1}$ the even terms would converge to 1 and the odd terms to -1.

#### _Part C_

$c_n$ is not cauchy.  If $a_n = \frac{(-1)^n}{n}$ then the even terms converge to 0 and the odd terms converge to -1. 

### Self-Evaluation

#### _Part A_

My answer here takes a different approach, but I believe still holds.

## External References
