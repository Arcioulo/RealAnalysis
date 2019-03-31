# Homework 2

Mark Archual | MTH 515

Dr. Scott | Real Analysis

1/30/19

## Problem 1.3.3

### Original Solution

#### _Part A Show that $\textrm{ sup } B = \textrm{ inf } A$_

#### _Part B Use Part A to explain why there is no need to assert that greatest lower bounds exist as part of the AOC_

### Self-Evaluation

<br>
<br>
<br>
<br>
<br>

## Problem 1.3.4

### Original Solution

#### _Part A Find a formula for $\textrm{sup ( } A_1 \bigcup A_2)$. Extend this to $\textrm{sup (} \bigcup_{k=1}^n A_k)$

#### _Part B Consider $\textrm{sup (} \bigcup_{k=1}^{\infty} A_k)$.  Does the formula in Part A extend to the infinite case?_

### Self-Evaluation

<br>
<br>
<br>
<br>
<br>

## Problem 1.3.5

### Original Solution

#### _Part A If $c \geq 0$, show that $\textrm {sup (} cA) = c*\textrm{sup}(A)$_

Let $s = \textrm{ sup (}A)$ then

$$ \forall a \in A, a \leq s $$

so 

$$c*a \leq c*s$$

thus, s in an upper bound.

Let b be any upper bound for $c*A$

Let $a \in A$ so $c*a \in c*A$. Then

$$c*a \leq b$$
$$a \leq b/c$$
If $b/c$ is an upper bound for $a$, then

$$s \leq b/c$$
$$c*s \leq b$$
$$c*s = \textrm{ sup(}cA)$$

#### _Part B Postulate a similar type of statement for $\textrm{sup(}cA)$ for the case $c < 0$_

$\textrm{ sup(}cA) = c*\textrm{inf(}A)$

### Self-Evaluation

<br>
<br>
<br>
<br>
<br>

## Problem 1.3.6

### Original Solution

#### _Part A Let $s = \textrm{sup}A$ and $t = \textrm{sup}B$.  Show $s + t$ is an upper bound for $A + B$_.

By the definition of supremum...

$$s \geq a, \forall a \in A$$
$$t \geq b, \forall b \in B$$
$$s+t \geq A + B$$

#### _Part B Now let $u$ be an arbitrary upper bound for $A + B$, and temporarily fix $a \in A$. Show $t \leq u - a$._

$$u \geq a + b$$
$$u-a \geq b, \forall b \in B$$
$$u-a \geq t$$


#### _Part C Finally, show $\textrm{sup (}A+B) = s+t$_

#### _Part D Construct another proof of this same fact using Lemma 1.3.8_

Assume $s+t$ is an upper bound for $A+B$.  Then, by Lemma 1.3.8

$$s + t < a + b - \epsilon, \forall \epsilon > 0$$

Therefore $s+t = \textrm{sup(}A+B)$

### Self-Evaluation

<br>
<br>
<br>
<br>
<br>

## Problem 1.3.8

### Original Solution

#### _Part A $(\frac{m}{n} : m,n \in N \textrm{ with } m < n)$_

Sup = 1

Inf = 0

#### _Part B $(\frac{-1^m}{n} : m,n \in N)$_

Sup = 1

Inf = -1

#### _Part C $(\frac{n}{3n+1} : n \in N)$_

Sup = 1/3

Inf = 1/4

#### _Part D $(\frac{m}{m+n} : m,n \in N)$_

Sup = 1

Inf = 0

### Self-Evaluation

<br>
<br>
<br>
<br>
<br>

## External References
