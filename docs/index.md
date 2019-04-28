---
layout: default
---

<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>

<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML' async></script>


# Chapter 7 Project

## Project Members and Roles

| Members      	| Exercises      	|
|--------------	|----------------	|
| Vishnu Aerva 	| 2, 5, 7, 16    	|
| Mark Archual 	| 11, 12, 15    	|
| Esra Celik   	| 14, 17, 18, 19 	|

---

## Topic Summary

Our group was tasked with studying Lebesgue's Criterion for Riemann Integration.

### Motivation

Riemann integration provides us with a foundation to define integration, even if a function is not perfectly continuous.  However, Riemann integration does not cover all discontinuous functions, which may lead to the question, how discontinuous can a function be, and still maintain some form of integrability?  What other definitions of integration exist, and how do expand upon, Riemann integration?

As shown in the book, Thomae's function and Dirichlet's function can provide some useful contrast for the scenario described above.  Observe that thomae's function, while certainly discontinuous one can construct the necessary conditions to show that it is indeed Riemann integrable (see Exercise 7.6.2).  Dirichlet's function does not fit the criteria, due to it being discontinuous at every point in its domain (as discussed in class).  Dirichlet's function is just an example, of many functions that fail to be Riemann integrable, so the need for a stronger form of integration is certainly justified.

### Theory

Lebesgue's Criterion for Riemann Integrability relies on two key definitions.

#### Sets of Measure Zero

A set $A \subseteq \mathbb{R}$ has _measure zero_ if, for all $\epsilon > 0$, there exists a contable collection of open intervals, $O_n$ wiht the property that A is contained in the union of all of the intervals $O_n$ and the sum of the lengths of all of the intervals is less than or equal to $\epsilon$.  More precisely, if $\lvert O_n \rvert$ refers to the length of the interval $O_n$, then we have $\ldots$

See Exercise 7.6.5 for more details.

$$ A \subseteq \cup_{n=1}^{\infty} O_n$$

and

$$\sum_{n=1}^{\infty} \lvert O_n \rvert \leq \epsilon$$

#### $\alpha$-Continuity

Let $f$ be defined on $[a,b]$ and let $\alpha > 0$. The function $f$ is $\alpha$-continuous at $x \in [a,b]$ if there exists $\delta > 0$ such that for all $y,z \in (x - \delta, x + \delta)$ it follows that $\lvert f(y) - f(z) \rvert < \alpha$

See Exercise 7.6.7 for more information.

#### Lebesgue's Criterion for Riemann Integrability

Let $f$ be a bounded function defined on the interval $[a,b]$. Then, f is Riemann-integrable if and only if the set of points where $f$ is not continuous has measure zero.

A partial proof is presented in Exercises 7.6.11 and 7.6.12.

### Consequences

Practically, Lebesgue's criterion helps further define what functions are Riemann integrable by giving a more specific criteria for continuity ($\alpha$-continuity) and setting a bound on what is acceptable for discontinuity.

Can we apply Lebesgue's Criterion to Dirichlet's function?  Yes, however we still see that the function is not integrable because the discontinuities do not form a set of measure zero.  The book also provides an example of a function that is differentiable, but fails to be integrable, breaking with the fundamental theorem of calculus.  Clearly, there is further room for improvement on our definition of integration and the book briefly discusses Lebesgue integration as that next step. Further investigation into this topic is outside of the scope of this project.

> Write-up prepared by Mark Archual

---

## Exercise 7.6.2

> Solution provided by Vishnu Aerva

## Exercise 7.6.5

> Solution provided by Vishnu Aerva

## Exercise 7.6.7

> Solution provided by Vishnu Aerva

## Exercise 7.6.11

Let $P_G$ be the partition containing the intervals in the set $G = {G_1, G_2, ... ,G_N}$ as defined in exercise 7.6.9.

Let $P_I$ be the partition formed from the set $K$, where $K = [a,b] \setminus \cup_{n=1}^{N} = {I_{N+1}, I_{N+2}, ... I_{n}}$ as defined in the text.

We know that $f$ is $\alpha$-continuous on this set because they do not contain the points from $G$, which are the points where $\alpha$-continuity fails.  We also know from previous exercises that, 

$$ \sum_{n=1}^{N} \lvert G_n \rvert < \frac{\epsilon}{4M} $$

where $M$ is supremum of $f(x)$.

Then for $P_G$ $\ldots$

$$U(f, P_G) - L(f, P_G) = \sum_{n=1}^{N} \lvert G_n \rvert * \lvert M_n - m_n \rvert \leq M \sum_{n=1}^{N} \lvert G_n \rvert < \frac{\epsilon}{2}$$

And for $P_I$ $\ldots$

$$U(f, P_I) - L(f, P_I) = \sum_{n = N+1}^{N + k} \lvert M_n - m_n \rvert \lvert I_n \rvert < \frac{\epsilon}{2}$$ for some $k \in \mathbb {N}$.

Then let $P_{\epsilon} = P_G + P_I$ and

$$U(f, P_{\epsilon}) = L(f, P_{\epsilon}) = \sum_{n=1}^{N} \lvert G_n \rvert * \lvert M_n - m_n \rvert + \sum_{n = N+1}^{N + k} \lvert M_n - m_n \rvert \lvert I_n \rvert < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

> Solution provided by Mark Archual

## Exercise 7.6.12

### _Part A_

Because $f$ is Riemann integrable, there exists a partition, $P_{\epsilon}$ of $[a,b]$ such that $f$ is Riemann integrable over the partition.

From theorem 7.6.4, we see that because $[a,b]$ is closed and bounded, and because $P_{\epsilon}$ is a union of open sub-intervals that covers $[a,b]$ there exists a finite sub-collection of intervals, $I_{N+1}, I_{N+2}, ... , I_{N+k}, k \in \mathbb{N}$, that also cover $[a,b]$.  Let this set be the interval over which $f$ is Riemann integrable.  Then, there also exists a set where $f$ fails to be $\alpha$-continuous, $I_1, I_2, ... I_N$.

Putting these ideas together, we see that $\ldots$

$U(f,$ $P_{\epsilon}$)$ - L(f,$ $P_{\epsilon}$)$ < \alpha \epsilon$

$\sum_{n = 1}^{N+k} \lvert M_n - m_n \rvert \lvert I_n \rvert < \epsilon$

$\sum_{n = 1}^{N} \lvert M_n - m_n \rvert \lvert I_n \rvert \leq \epsilon$

$\alpha \sum_{n = 1}^{N} \lvert I_n \rvert \leq \epsilon$

$\sum_{n = 1}^{N} \lvert I_n \rvert \leq \frac{\epsilon}{\alpha}$

where $\alpha > 0$.

$\therefore D^{\alpha}$ has zero measure.

### _Part B_

We know from previous exercises, that $D = \cup_{n=1}^{\infty} D^{\alpha_n}$ where $\alpha_n = \frac {1}{n}$ and $D^\alpha \subseteq D$.  Because each $D^{\alpha_n}$ has measure zero (as shown above), and from exercise 7.6.5 we have that the union of countable sets of measure zero also have measure zero, 

$$ D = \cup_{n=1}^{\infty} D^{\alpha_n} = 0 $$

> Solution provided by Mark Archual

## Exercise 7.6.14

### _Part A_

Given 

$$g(x) = \left\{
        \begin{array}{ll}
            x^2 \sin(\frac{1}{x}) & \quad x > 0 \\
            0 & \quad x \leq 0
        \end{array}
    \right.
$$

$$g'(0) = \lim_{x \to 0}{\frac{g(x) - 0}{x}} = \lim_{x \to 0}{x\sin(\frac{1}{x})} = 0$$    

### _Part B_

Using standard rules for differentation $g'(x)$ for $x \neq 0$ can be computed as follows:

$$g'(x) = 2x\sin(\frac{1}{x}) - \cos(\frac{1}{x})$$

### _Part C_

By the Archimedean Property there exists $2n$ such that $\frac{1}{2n\pi} < g$.  Consider the interval $[\frac{1}{(2n+1)\pi}, \frac{1}{2n\pi}]$

$$g'(\frac{1}{(2n+1)\pi}) = -\cos((2n+1)\pi) = 1$$

Similarly $\ldots$

$$g'(\frac{1}{2n\pi}) = -\cos((2n\pi) = -1$$

Since $g'(x)$ is continuous on $[\frac{1}{(2n+1)\pi}, \frac{1}{2n\pi}]$ by the intermediate value theorem, $g'(x)$ attains every value between -1 and 1.  Then $\forall \delta > 0, \exists x \in (-\delta, \delta)$ such that $g'(x) \neq 0 = g'(0)$ which shows that $g'(x)$ is not continuous at $x=0$.

> Solution provided by Esra Celik

## Exercise 7.6.15

### _Part A_

For $c \in C$,

$$ lim_{n \to \infty} f_n(c) = 0$$

as $f$ is defined to be zero for values within the cantor set.

### _Part B_

For $x \notin C$, 

then for all values of $n$, $f_n$ takes on the shifted values of $g(x)$,, which does not equal 0.

Thus 

$$ lim_{n \to \infty} f_n(x) \neq 0 $$

> Solution provided by Mark Archual

## Exercise 7.6.16

> Solution provided by Vishnu Aerva

## Exercise 7.6.17

$f'(x)$ is Riemann-integrable on [0,1] because _$f'$ is discontinuous only on C which is known to have measure zero_.  By Lebesgue's Theorem for Riemann-integrability, $f'$ must be integrable on [0,1].

> Solution provided by Esra Celik

## Exercise 7.6.18

On the first step, $\frac{1}{9}$ of the middle part is removed and on the second step, the middle $\frac{1}{27}$ is removed from the remaining two parts after the first step. Continuing on, the sum of the remaining portion is given by

$$ \frac{1}{9} + \frac {1}{27} + \frac{2^2}{3^4} + \ldots = \sum_{n=1}^{\infty} \frac {2^{n-1}}{3^{n-1}} = \frac{1}{9} \sum_{n=1}^{\infty} \frac{2}{3}^n = \frac {1}{3} $$

This shows that the sum of lengths of intervals that make up $C_n$ is $1 - \frac{1}{3} = \frac{2}{3}$ which is not zero.

__Result:__ Sum of intervals that make up $C_n$ tends to $\frac{2}{3}$ as $n \to \infty$.

> Solution provided by Esra Celik

## Exercise 7.6.19

Let $c_1' = [0, \frac{4}{9}] \cup [\frac{5}{9}, 1]$ and $c_{n+1}' = \frac{1}{3^{n+1}}c_n' \cup (\frac{5}{9} + \frac{1}{3^{n+1}}c_n')$

$c' = \cap_{n=1}^{\infty} c_n'$ is called the fat Cantor set which is discussed above the problem.  Define $g_n: [0,1] \to [0,1]$ as a continuously increasing function that maps each interval of $c_n$ to $c_n'$ (where $c_n$ is used to construct c).  Each $g_n$ is a bijection that maps the partition of $[0,1]$ by $c_n$ to partition of $[0,1]$ by $c_n'$.  Each boundary point of $c_n$ is mapped to a boundary point of $c_n'$ and for all $m \geq n, g_m(x) = g_n(x)$ if $x \notin c_n$ so $\lim_{n \to \infty} g_n(x)$ exists if $x \notin c$.  If $c \in C$, then there exists some interval in $C_n$ whose length is $\frac{1}{3}n$ which gets mapped to the interval in $c_n'$ whose length is not greater than $\frac{1}{3^{n-1}}$, i.e. there exists $c' \in C'$ such that $\lvert g_n(c) - c' \rvert < \frac {1}{3^{n-1}}$ so $\lim_{n \to \infty} g_n(c)$ exists.

Define

$$ g(x) = \lim_{n \to \infty} g_n(x)$$

where $g: [0,1] \to [0,1]$ such that $g: c \to c'$ and g is continuous and increasing and is a bijection as well.  Let f be defined as 

$$f(x) = \lim_{n \to infty}f_n(x)$$

as in 7.6.15 which is integrable on $[0,1]$ as it is discontinuous on $c$ with measure zero but $f o g$ is not integrable as it is discontinuous on $c'$ whose measure is $\frac{2}{3}$.

> Solution provided by Esra Celik

## External References

Understand Analysis, Course Textbook


