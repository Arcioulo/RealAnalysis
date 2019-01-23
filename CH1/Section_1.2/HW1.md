# Homework 1

Mark Archual | MTH 515

Dr. Scott | Real Analysis

1/24/2019

## Problem 1.2.1

### Original Solution

#### Part A

#### _Prove that $\sqrt{3}$ is irrational_

Assume $\sqrt{3}$ is rational.  If $\sqrt{3}$ is rational, then it can be written as a ratio of two relatively prime natural numbers, a and b, such that:

$$\frac{a}{b} = \sqrt{3}$$

Proof:

$$\frac{a}{b} = \sqrt{3}$$

$$\frac{a^2}{b^2} = {3}$$

$${a^2} = {3}{b^2}$$

This implies that ${a^2}$ and thus a, are divisible by 3.  We can rewrite a as a multiple of 3:

$$a = 3*c$$

where c is some natural number.  Subtituting in for a, we see:

$${(3*c)}^2  = 3b^2$$

$$9c^2 = 3b^2$$

$$3c^2 = b^2$$

This is a contradiction as both a and b were assumed to be relatively prime.  Thus $\sqrt{3}$ is irrational.

#### _Does a similar argument work to show $\sqrt{6}$ is irrational?_

Assume $\sqrt{6}$ is rational.  If $\sqrt{6}$ is rational, then it can be written as a ratio of two relatively prime natural numbers, a and b, such that:

$$\frac{a}{b} = \sqrt{6}$$

Proof:

$$\frac{a}{b} = \sqrt{6}$$

$$\frac{a^2}{b^2} = {6}$$

$${a^2} = {6}{b^2}$$

This implies that ${a^2}$ and thus a, are divisible by 6, as well as its factors 2 and 3.  We can rewrite a as a multiple of 2:

$$a = 2*c$$

where c is some natural number.  Subtituting in for a, we see:

$${(2*c)}^2  = 6b^2$$

$$4c^2 = 6b^2$$

$$2c^2 = 3^2$$

This is a contradiction as both a and b were assumed to be relatively prime.  Thus $\sqrt{6}$ is irrational.

#### Part B
 
#### _Where does the proof of Theorem 1.1.1 break down if we try to use it to prove $\sqrt{4}$ is irrational?_

Assume $\sqrt{4}$ is rational.  If $\sqrt{4}$ is rational, then it can be written as a ratio of two relatively prime natural numbers, a and b, such that:

$$\frac{a}{b} = \sqrt{4}$$

Proof:

$$\frac{a}{b} = \sqrt{4}$$

$$\frac{a^2}{b^2} = {4}$$

$${a^2} = {4}{b^2}$$

This implies that ${a^2}$ and thus a, are divisible by 2.  We can rewrite a as a multiple of 2:

$$a = 2*c$$

where c is some natural number.  Subtituting in for a, we see:

$${(2*c)}^2  = 4b^2$$

$$4c^2 = 4b^2$$

$$c^2 = b^2$$

From theorem 1.1.1 we should able to rewrite $b^2$ at this point in a way that breaks the assumption that b is relatively prime.  However, this is not the case and thus we can assume that $\sqrt{4}$ is rational.

### Self-Evaluation

---

## Problem 1.2.7

### Original Solution

#### _Let $f(x) = x^2, A = [0,2], B = [1,4]$_

#### Part A
#### _Find $f(A)$ and $f(B)$.  Does $f(A \bigcap B) = f(A) \bigcap f(B)?$  Does $f(A \bigcup B) = f(A) \bigcup f(B)?$_

$$f(A) = f([0,2])$$
$$f(A) = [0, 4]$$
---
$$f(B) = f([1,4])$$
$$f(B) = [1,16]$$
---
$$f(A \bigcap B) = f([0,2] \bigcap [1,4])$$
$$f(A \bigcap B) = f([1,2])$$
$$f(A \bigcap B) = [1,4]$$
---
$$f(A) \bigcap f(B) = f([0,2]) \bigcap f([1,4])$$
$$f(A) \bigcap f(B) = [0,4] \bigcap [1,16]$$
$$f(A) \bigcap f(B) = [1,4] = f(A \bigcap B)$$
---
$$f(A) \bigcup f(B) = f([0,2]) \bigcup f([1,4])$$
$$f(A \bigcup B) = f([0,4])$$
$$f(A \bigcup B) = [0,16]$$
---
$$f(A) \bigcup f(B) = f([0,2]) \bigcup f([1,4])$$
$$f(A) \bigcup f(B) = [0,4] \bigcup [1,16]$$
$$f(A) \bigcup f(B) = [0,16] = f(A \bigcup B)$$

#### Part B
#### _Find two sets, $A$ and $B$ for which $f(A \bigcap B) \neq f(A) \bigcap f(B)$_

Let $A = [-1, 0], B = [0,1]$

$$f(A \bigcap B) = f([-1,0] \bigcap [0,1])$$
$$f(A \bigcap B) = f([0])$$
$$f(A \bigcap B) = 0$$
---
$$f(A) \bigcap f(B) = f([-1,0]) \bigcap f([0,1])$$
$$f(A) \bigcap f(B) = [0,1] \bigcap [0,1]$$
$$f(A) \bigcap f(B) = [0,1] \neq f(A \bigcap B)$$

#### Part C
#### _Show that, for an arbitrary function $g : R -> R$ it is always true that $g(A \bigcap B) \subseteq g(A) \bigcap g(B)$ for all sets $A, B \subseteq R$_

Let $x \in A \bigcap B$ this then implies

$$g(x) \in g(A) \bigcap g(B)$$

The next step in the justification process I struggled with some, as I could not find a good way to justify why $g(A \bigcap B) \subseteq g(A) \bigcap g(B)$ other than the fact it is obvious given the above relationship.

#### Part D
#### _Form and prove a conjecture about the relationship between $g(A \bigcup B) \textrm{ and } g(A) \bigcup g(B)$ for an arbitrary function $g$_

My conjecture is that $g(A \bigcup B) = g(A) \bigcup g(B)$

My intuition about this comes from a background in boolean logic.  My first inclination was to try and prove this with a truth table, but I could not make it generic enough for this process.

Let $x \in A \bigcup B$ this then implies

$$g(x) \in g(A \bigcup B) = g(A \bigcup B)$$

Again I somewhat struggled with the last step of this process as I could not find a clear way to communicate the equality of this relationship other than the fact that I feel it is intuitively obvious.

### Self-Evaluation

---

## Problem 1.2.8

### Original Solution

#### Part A
#### _$f : N -> N \textrm{ that is 1-1 but not onto}$_

Let $f(x) = 2(x)+1$

then

$$f(1) = 3$$
$$f(2) = 5$$
$$...$$

so the mapping is 1-1, in that it maps every element uniquely, but not all of B is represented, i.e. there are no even numbers in the mapping.

#### Part B
#### _$f : N -> N \textrm{ that is onto but not 1-1}$_

Let

$$
f(x) = \left\{
        \begin{array}{ll}
            x & \quad x < 5 \\
            x-5 & \quad x \geq 5
        \end{array}
    \right.
$$

The mapping is onto, in that all of B is represented.  However it is not 1-1. For example $f(6) = f(1)$.

#### Part C
#### _$f : N -> Z \textrm{ that is 1-1 and onto}$_

### Self-Evaluation

---

## Problem 1.2.11

Form the logical negation of each claim.  In each case, make an intuitive guess as to wether the claim or its negation is the true statement.

### Original Solution

#### Part A  
#### _For all real numbers satisfying $a<b$, there exists an $n \in N$ such that $a + \frac{1}{n} < b$_

There exists real numbers $a<b$ such that for all $n \in N a + \frac{1}{n} \geq b$

The negated statement falls apart when trying to prove the statement holds *for all* $n$.  For example if we let $a = 1, b = 2, \textrm{ and } n = 10$, the negated statement is false (for all $n>1$).  Conversely, $n$ can always be chosen in such a way that the original statement is true, regardless of the values for $a$ and $b$.

#### Part B
#### _There exists a real number $x>0$ such that $x<1/n$ for all $n \in N$_

For all real numbers, $x>0$, there exists an n ($n \in N$) such that $x \geq \frac{1}{n}$

I would hypothesize that the orignal statement is correct.  The negated statement does not hold across $R$ for all possible $x$.  For example if $x = 0.1, \textrm{ and } n = 1$  the orignal statement would hold, for all $n$, while the negated statement does not.

#### Part C
#### _Between every two distinct real numbers there is a rational number_

Between every two distinct real numbers, there is not a rational number.

The original statement is correct.  $R$ exists as an extension of $Q$.  As the book describes it, $R$ "fills in the gaps" left behind by $Q$.  While these "gaps" may not be as literal as I am assuming, the expression helps visualize how the two sets coexist, which leads me to my conclusion.

### Self-Evaluation

---

## Problem 1.2.12

Let $y_1 = 6$ and for each $n \in N$ define $Y_{n+1} = \frac{(2y_n-6)}{3}$

### Original Solution

#### Part A

#### _Use induction to prove that the sequence satisfies $y_n > -6$ for all $n \in N$_

For $n=1$ 

$$y_1 = 6 > -6$$

> The induction is grounded

Suppose $y_n > -6$

$$y_{n+1} = \frac{2y_n-6}{3} > \frac{2(-6)-6}{3} = -6$$

#### Part B

#### _Use another induction argument to show the sequence is decreasing_

For $n=1$

$$y_2 = \frac{2(y_1)-6}{3} = \frac{2(6)-6}{3} = 2 < 6$$

> The induction is grounded

For $y_{n+1} < y_n$

$$2y_{n+1} < 2y_n$$
$$2y_{n+1} - 6 < 2y_n - 6$$
$$\frac{2y_{n+1} - 6}{3} < \frac{2y_n - 6}{3}$$

It then follows that $y_{n+2} < y_{n+1}$, etc.

### Self-Evaluation

---

## External References
