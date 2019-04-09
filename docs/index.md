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

| Members      	| Exercises      	| Roles                                                   	|   	|
|--------------	|----------------	|---------------------------------------------------------	|---	|
| Vishnu Aerva 	| 2, 5, 7, 16    	| Applications of Lebesgue's Theorem using Cantor Sets      |   	|
| Mark Archual 	| 11, 12, 15    	| Proof of Lebesgue's Theorem 	                            |   	|
| Esra Celik   	| 14, 17, 18, 19 	| Motivation of Topic                                	      |   	|

## Exercise 7.6.2

> Solution provided by Vishnu Aerva

## Exercise 7.6.5

> Solution provided by Vishnu Aerva

## Exercise 7.6.7

> Solution provided by Vishnu Aerva

## Exercise 7.6.11

> Solution provided by Mark Archual

## Exercise 7.6.12

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
