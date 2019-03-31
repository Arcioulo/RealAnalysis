# Homework Six

Mark Archual | MTH 515

Dr. Scott | Real Analysis

3/6/2019

## Problem 2.7.1 (Part A only)

### Original Solution

Let $S_n$ be the partial sum of

$$S_n = \sum_{k=1}^{n} a_k $$

which is a monotonically decreasing sequence that converges to 0.

By the cauchy criterion for series, $\exists N \in \mathbb{N}$ s.t. $n > m \geq N$ implies $\lvert S_n - S_m \rvert < \epsilon$ for an arbitrary $\epsilon > 0$.

Notice that 

$$ \lvert S_n - S_m \rvert = (a_1 - a_2 + a_3\ldots \pm a_n) + (-a_1+a_2-a_3\ldots\pm a_m)$$

Because the series is decreasing, we know that $S_m \geq S_n$ so

$$(a_m -a_{m+1} + \ldots \pm a_{n-1}) \geq (a_{m+1} - a_{m+2} \ldots \pm a_{n})$$

So 

$$2 \lvert S_n - S_m \rvert = 2*\lvert (a_{m+1} - a_{m+2} \ldots \pm a_{n}) \rvert$$

$$\leq (a_m -a_{m+1} + \ldots \pm a_{n-1}) - (a_{m+1} - a_{m+2} \ldots \pm a_{n})$$
$$= \lvert a_m \pm a_n\rvert$$
$$\leq \lvert a_m + a_n \rvert < 2 * \epsilon$$

$\therefore S_n$ is cauchy.

### Self-Evaluation

I glossed over the behavior of the alternating sign here but I see that I complete solution requires an understanding of how the relationship between the partial sum changes based on the indices.  I did try to use the cancelation of terms to my advantage, but this ended up complicating things as I did not motivate a relationship between the partial sums and the individual terms of the sequence.  If I would have taken the approach shown in the solution, I would lose the triangle inequality and multiplication factor and the relationship would not be as convoluted.

## Problem 2.7.2

### Original Solution

#### _Part A_

$\sum_{n=1}^{\infty} \frac{1}{2^n + n}$ converges because the sequence $(\frac{1}{2^n + n})$ converges to 0.

#### _Part B_

$\sum_{n=1}^{\infty} \frac {\sin{n}}{n^2}$ converges as

$$\sum_{n=1}^{\infty} \frac {\sin{n}}{n^2} \leq \sum_{n=1}^{\infty} \frac {1}{n^2}$$

and the sequence $(\frac{1}{n^2})$ converges to 0 so $\sum_{n=1}^{\infty} \frac {1}{n^2}$ converges, and then by the comparison test $\sum_{n=1}^{\infty} \frac {\sin{n}}{n^2}$ converges.

#### _Part C_

The $\sum \frac {(-1)^{n+1}(n+1)} {2n}$ does not converge.  We know that $\frac {(n+1)} {2n}$ converges to $\frac{1}{2}$, so by the alternating series test, the sum diverges.

#### _Part D_

Let $1 + \frac{1}{2} - \frac{1}{3} + \frac{1}{4} + \frac{1}{5} - \frac{1}{6} \ldots = a_k$.  And let $b_k$ be infinite the sum of the harmonic series.

Then $0 \leq a_k \leq b_k \forall k \in \mathbb{N}$

We know $b_k$ diverges, so by  the comparison test, $a_k$ diverges as well.

#### _Part E_

Let $1 - \frac{1}{2^2} + \frac{1}{3} - \frac{1}{4^2} + \frac{1}{5} - \frac{1}{6^2} \ldots = a_k$ And let $b_k$ be the infinite sum of the harmonic series.

Then $0 \leq a_k \leq b_k \forall k \in \mathbb{N}$

We know $b_k$ diverges, so by  the comparison test, $a_k$ diverges as well.

### Self-Evaluation

## Problem 2.7.9

#### _Part A_

My justification here was a little too loose.  Just because the sequence of a sum goes to zero does not justify the convergence of the sum itself.

#### _Part C_

I used the alternating series test here, but not correctly.  An easy route would have been to show that the positive and negative terms of the sequence converge to different values.

#### _Parts D and E_

I got these wrong by incorrectly trying to use the comparison test.

### Original Solution

#### _Part A_

If $r < r' < 1$, then this implies that $r'$ is an valid upper bound on the value of the ratio, and that it exists between r and 1 by the archimedean property.  _Let $\epsilon = r' - r$_.

Because the $\lim \lvert \frac{a_{n+1}}{a_n} \rvert = r$, then we know it never passes $r$ and therefore never passes $r'$.  _This allows us to say:_

$$\lvert \lvert \frac{a_{n+1}}{a_n} \rvert -r \rvert = \epsilon$$

_Or_


$$- \epsilon <  \lvert \frac{a_{n+1}}{a_n} \rvert -r  < \epsilon$$

_Adding $r$ to both sides, and multiplying by $\lvert a_n \rvert$ gives_


$$ \lvert a_n \rvert r - \epsilon <  \lvert a_{n+1} \rvert  < \epsilon + r \lvert a_n \rvert$$

_Because $r' = \epsilon + r$_

$$\lvert a_{n+1} \rvert \leq \lvert a_n \rvert r'$$

#### _Part B_

$\lvert a_N \rvert \sum (r')^n$ converges because it is a geometric sequence with a ratio less than 1.

#### _Part C_

_Using induction to prove this, we have already proved the base case in (A)_.

_By the inductive hypothesis_

$$\lvert a_{N+k+1} \rvert < \lvert a_{N+k} \rvert r' < (\lvert a_{N} \rvert (r')^k)r' = \lvert a_{N} \rvert (r')^{k+1}$$

_This completes the induction._

$\sum a_n$ is a combination of two different series,

$$\sum_{n=1}^{\infty} a_n = \sum_{n=1}^N \lvert a_n \rvert + \sum_{n=N+1}^{\infty} \lvert a_n \rvert$$

The first summation is finite, so it is guaranteed to converge.  The second summation we know to converges because $\lvert a_{N+k} \rvert < r^k \lvert a_N \rvert \forall k$ which allows us to utilize the comparison test, to show

$$ \sum_{n=N+1}^{\infty} \lvert a_n \rvert =  \sum_{k=1}^{\infty} \lvert a_N+k \rvert $$.

$\therefore \sum \rvert a_n \lvert$ converges and by the absolute convergence test, $\sum a_n$ converges.

>Note: I did some additional reading on the Ratio test at the link provided in [External References](#external-references)

### Self-Evaluation

#### _Part A_

I think I had the right idea here, I just had some trouble expressing it.  Exploiting the use of an $\epsilon$ as a quantifiable expression for $r' -r$ as the indexing term grows makes a lot of sense.  The epsilon term captures what I was thinking about when discussing the archimedean property.  I have corrected my solution above, the additions are in _italics._

#### _Part C_
I got pretty much followed the solution here, but I left out some details that I haved added above in _italics_.


## Problem 3.2.2 (Parts A, B and D Only)

### Original Solution

Let $A = {(-1)^n + \frac{2}{n}}$

Limit Points: -1, 1

The set is not open, because there is no viable epsilon neighborhood for 2, and not closed because it does not contain -1.

$A \cup L = A \cup \{-1\} = \bar{A}$

Let $B = x \in \mathbb{Q}, 0 < x < 1$

The limit points are 0 and 1.

The set is open, as there is a valid epsilon neighborhood for all points in the set.  The set is also not closed because it does not contain its limit points.

$B \cup L = B \cup \{ 0,1 \} = \bar{B}$

### Self-Evaluation

I incorrectly stated that B is open.  The solution's reasoning for why it is not open, that is the density of $\mathbb{Q} \in \mathbb{R}$, is clear to me.  I even stated this as part of my reasoning for 3.2.3 part A.

## Problem 3.2.3

### Original Solution

#### _Part A_

$\mathbb{Q}$ is not closed because every $x \in \mathbb{R}$ is a limit point of $\mathbb{Q}$, so $\mathbb{Q}$ does not contain any of its limit points.

$\mathbb{Q}$ is also not open because by the Archimedean property, each epsilon neighborhood inherently includes irrational numbers between the rationals, i.e. the density of $\mathbb{Q}$ in $\mathbb{R}$

#### _Part B_
$\mathbb{N}$ is closed as it has no limit points, and thus, does not contain them.  Similar to $\mathbb{Q}$, $\mathbb{N}$ is not open as the epsilon neighborhoods are essentially isolated to that point.

#### _Part C_
$x \in \mathbb{R}, x \neq 0$ is open, and closed, for the same reason as $\mathbb{R}$.  That is all epsilon neighborhoods are valid, and it does not have any limit points.  

#### _Part D_
$\sum \frac{1}{n^2}, n \in \mathbb{N}$ is not closed, as the limit, $\frac{\pi^2}{6} \notin \mathbb{N}$.  It is also not open, as each term is a finite point, thus there is no valid epsilon neighborhood for each term.

#### _Part E_
$\sum \frac{1}{n}, n \in \mathbb{N}$ is closed as it has no limit points, similar to $\mathbb{N}$ itself.  It is not open because each term is a finite point, and thus there is no valid epsilon neighborhood for each term.

### Self-Evaluation

#### _Part C_
I missed that the set is not open here.  I was debating about 0 being a limit point of the set when I was deciding on an answer for this one, but I got caught up on the idea of $\mathbb{R}$ going out to infinity, more so than not containing 0.

In general, I could have improved my answers by giving some examples of invalid limit points.

## External References
[Used on 2.7.9, parts B and C](http://tutorial.math.lamar.edu/Classes/CalcII/RatioTest.aspx)
