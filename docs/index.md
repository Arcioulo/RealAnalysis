---
layout: default
---

<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML' async></script>


# Chapter 7 Project

## Project Members and Roles

| Members      	| Exercises      	| Roles                                                   	|   	|
|--------------	|----------------	|---------------------------------------------------------	|---	|
| Vishnu Aerva 	| 2, 5, 7, 16    	| Introduction of Presentation                            	|   	|
| Mark Archual 	| 9, 11, 12, 15  	| Prepared Write-Up, Presented Proof of Lebesgue's Theorem 	|   	|
| Esra Celik   	| 14, 17, 18, 19 	| Closing of Presentation                                 	|   	|

## Exercise 7.6.2

> Solution provided by Vishnu Aerva

## Exercise 7.6.5

> Solution provided by Vishnu Aerva

## Exercise 7.6.7

> Solution provided by Vishnu Aerva

## Exercise 7.6.9

> Solution provided by Mark Archual

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

> Solution provided by Esra Celik

## Exercise 7.6.18

> Solution provided by Esra Celik

## Exercise 7.6.19

> Solution provided by Esra Celik





## External References
