# Homework 7

Mark Archual | MTH 515

Dr. Scott | Real Analysis

3/27/17

## Problem 3.3.2

### Original Solution

#### _Part A_

$\mathbb{N}$ is not compact as it does not contain any convergent subsequences.

#### _Part B_

$\mathbb{Q} \cap [0,1]$ is not compact. For $0<q_n<1$, a subsequence of $qn$ can be found such that $q_{n_k} -> \frac{1}{\pi}$ which $\notin \mathbb{Q} \cap [0,1]$. 

#### _Part C_

The Cantor set is compact as it is closed and bounded (Heine-Borel Theorem).

#### _Part D_

This set is not compact as it does not contain all of its limit points, i.e. $\frac{\pi^2}{6}$

#### _Part E_

This set is compact as it is bounded by $[\frac{1}{2}, 1]$ and it contains both of its limit points, $\frac{1}{2}, 1$.

### Self-Evaluation

No real comments on this section other than I incorrectly stated in _Part E_ that the sequence converged to 1/2.

---

## Problem 3.3.5

### Original Solution

#### _Part A_

True. We know that the arbitrary intersection of closed sets remains closed (Thm 3.2.14) so the arbitrary intersection of compact sets retain all of their limit points.  Compact sets must also be bounded, and the intersection of compact sets would remain bounded.

#### _Part B_

This is false as it is essentially the negation of the statement of Part A which we know to be true.

#### _Part C_

False, for example consider the $(0,1) \cap [0,1]$.  The result is not compact, $(0,1)$ as it is not closed.

#### _Part D_

This is false.  An example is given in the proof of theorem 3.4.3.  In general, the arbitrary intersection of closed subsections of $\mathbb{N}$ can only be $\empty$.

### Self-Evaluation

No major differences here either, however I could have given a more rigorous answer for _Part B_ other than relying on my answer for _Part A_.

---

## Problem 4.2.5

### Original Solution

#### _Part A_

>Rough Work

Solve $\lvert (3x+4) - 10 \rvert$ in terms of $\lvert x-2 \rvert$.

$$\lvert (3x-6) \rvert < \epsilon$$
$$3 \lvert (x-2) \rvert < \epsilon$$
$$\lvert (x-2) \rvert < \frac{\epsilon}{3}$$

Thus $\delta = \frac{\epsilon}{3}$.

>Proof

Let $\epsilon > 0$ be arbitrary, and $\delta = \frac{\epsilon}{3}$  If 0 < $\lvert x - 2 \rvert < \delta$  Then $\ldots$

$$\therefore \lvert (3x+4) - 10 \rvert = 3 \lvert (x-2) \rvert < 3\delta = 3(\frac{\epsilon}{3}) = \epsilon$$

#### _Part B_

>Rough Work

Solve $\lvert x^3 \rvert$ in terms of $x$.

$$x^3 < \epsilon$$
$$x < \sqrt[3]{\epsilon}$$

So $\delta = \sqrt[3]{\epsilon}$.

>Proof

Let $\epsilon > 0$ be arbitrary and set $\delta = \sqrt[3]{\epsilon}$. If $0<\lvert x \rvert < \delta$ then $\ldots$

$$ \therefore \lvert x^3 \rvert = x < \delta^3 = (\sqrt[3]{\epsilon})^3 = \epsilon$$

#### _Part C_

>Rough Work

Solve $\lvert (x^2 + x - 1) -5$ in terms of $(x-2)$.

$$ \lvert x^2 + x -6 \rvert < \epsilon $$
$$ \lvert x+3\rvert \lvert x-2 \rvert < \epsilon $$
$$ (x-2) < \frac{\epsilon}{x+3} $$

$x+3$ needs a lower bound.

Suppose $\delta \leq 1$.  So $\lvert x - 2 \rvert < 1 \ldots$

$$-1 < \lvert x - 2 \rvert < 1$$
$$5 < \lvert x + 3 \rvert < 7$$

Taking $\lvert x + 3 \rvert < 7$ and resolving for $\epsilon \dots$

$$ \lvert x+3 \rvert \lvert x-2 \rvert < 6* \lvert x -2 \rvert < \epsilon $$
$$ x - 2 <f \frac {\epsilon} {6} $$

So $\delta = \textrm{min}(1, \frac{\epsilon}{6})$

>Proof

Let $\epsilon > 0$ be arbitrary and $\delta = \textrm{min}(1, \frac{\epsilon}{6})$.  If $0 < x-2 < \delta$ then $\ldots$

$$ \therefore \lvert x^2 + x -6 \rvert = \lvert x+3\rvert \lvert x-2 \rvert < 6\lvert x - 2 \rvert \leq 6(\frac{\epsilon}{6}) = \epsilon$$

#### _Part D_

This one I had some trouble with the algebra and trying to solve for epsilon in terms of the limit.  I could not make any significant progress to generate a proof.

### Self-Evaluation

In general I should have restated the limit at the end of my formal proof.

For _Part D_ I see the approach and how it is similar to _Part C_.  I worked the expression to 

$$ \frac {\lvert x - 3 \rvert} {3 \lvert x \rvert}$$

but I had a hard time seeing where to go from here.

---

## Problem 4.2.8

### Original Solution

#### _Part A_

The limit does not exist as the denominator is undefined at the limit point, so $f(x) - 2 > \epsilon$ as $x -> 2$.

#### _Part B_

$$\lim_{x \to \frac{7}{4}} \frac {\lvert x - 2 \rvert}{x-2} = -1$$.

Set $\delta = \frac {7}{4} - 2 = \frac {1}{4}$ then for $ 0 < \lvert x - \frac{7}{4} \rvert < \delta \ldots$

$ \therefore \lvert \frac {\lvert x -2 \rvert} {x - 2} + 1 \rvert = 0 < \epsilon$

#### _Part C_

This limit does not exists.  Consider separate subsequences $x_{n_e}$ for the even valued terms and $x_{n_o}$ for the odd valued terms.  The even valued terms would converge to 1 whereas the odd valued terms converge to -1, thus by corollary 4.2.5 the limit d.n.e.

#### _Part D_

>Rough Work

Solve $\sqrt[3]{x} (-1)^{\frac{1}{x}}$ in terms of $x$.

$$ \lvert \sqrt[3]{x} (-1)^{\frac{1}{x}} \rvert < \epsilon $$

We can simplify this expression by recongnizing that $(-1)^{\frac{1}{x}}$ reduces to 1 for our purposes.  So $\ldots$

$$\lvert \sqrt[3]{x} \rvert < \epsilon$$

Thus $\delta = \epsilon^3$.

>Proof

Let $\epsilon > 0$ be arbitrary and set $\delta = \epsilon^3$.  If $0<x<\delta$ then $\ldots$

$$\lvert \sqrt[3]{x} (-1)^{\frac{1}{x}} \rvert < \lvert \sqrt[3]{x} \rvert < \sqrt[3]{\delta} = \sqrt[3]{\epsilon^3} = \epsilon$$

### Self-Evaluation

My justification for _Part A_ was different but I believe still valid.

---

## Problem 4.3.1

### Original Solution

#### _Part A_

Prove $g$ is continuous at $c = 0$.

>Rough Work

We want $\lvert \sqrt[3]{x} - 0 \rvert < \epsilon$

$$\lvert \sqrt[3]{x} < \epsilon \rvert$$
$$x < \epsilon^3 = \delta$$

>Clean

Let $\epsilon > 0, \delta = \epsilon^3$ whenever $x \geq 0$ and $\lvert x - 0 \rvert < \delta, x < \epsilon^3$ and $\sqrt[3]{x} < \epsilon$, $\sqrt[3]{x}$ is continuous at $x = 0$.

#### _Part B_

>Rough Work

$\lvert \sqrt[3]{x} - \sqrt[3]{c} \rvert < \epsilon$ when $\lvert x - c \rvert < \delta$

Let $a = \sqrt[3]{x}$ and $b = \sqrt[3]{c}$.  Then $\ldots$

$$\lvert \sqrt[3]{x} - \sqrt[3]{c} \rvert = \lvert \frac{(a -b) (a^2 +ab +b^2)}{a^2 + ab + b^2}$$
$$= \frac {a^3 - b^3}{a^2 + ab + b^2}$$
$$= \frac {x -c}{\sqrt[3]{x}^2 + \sqrt[3]{x}\sqrt[3]{c} + \sqrt[3]{c}^2} < \frac{x - c}{\sqrt[3]{c}^2} < \epsilon$$

So $x-c < \epsilon * \sqrt[3]{c}^2 = \delta$

>Clean

Let $\epsilon > 0$ be arbitrary, $\delta = \epsilon^3$ whenever $x \geq 0$ and $\lvert x - c \rvert < \delta$ then $\ldots$

$\lvert \sqrt[3]{x} - \sqrt[3]{c} \rvert = \frac {x -c}{\sqrt[3]{x}^2 + \sqrt[3]{x}\sqrt[3]{c} + \sqrt[3]{c}^2} \leq \frac{x - c}{-\sqrt[3]{c}} < \epsilon * \sqrt[3]{c}^2  = \epsilon$



### Self-Evaluation

I did not have a justification for why we could assume c to be greater than 0.  Otherwise no comments.

---

## Problem 4.3.4

### Original Solution


#### _Part A_

Let $f(x) = \frac{1}{x}$ and $g(x) = \cos(x)$.

Then $\ldots$

$$\lim_{x \to \infty} \frac {1}{x} = 0$$
$$\lim_{x \to 0} \cos(x) = 1$$

But $\ldots$

$$\lim_{x \to \infty} \frac {1}{\cos (x)} = \textrm{d.n.e.}$$


#### _Part B_

If f and g are continuous then they must be continuous on all of $\mathbb{R}$ per the definition of the problem.  Following the proof for composite functions shows that $g(f(x_n))$ has limit $g(f(c))$ if $(x_n)$ is a sequence in $\mathbb{R}$ with limit $c$.

#### _Part C_

If $f$ is continuous and not $g$ then it does not hold because $g$ must be continuous at $f(c)$ per _Part B_.

If $g$ is continuous and not $f$ then the validity depends on the nature of $g o f$.

### Self-Evaluation

For _Part C_ I got a little 'hand wavey' with the phrase 'the nature of $g o f$.  Looking at the solution, it is more that the sequence $x_n$ must be valid for the limit of $g o f$ to hold.

---

## External References
