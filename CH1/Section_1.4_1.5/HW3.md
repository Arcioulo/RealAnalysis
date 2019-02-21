# Homework 3

Mark Archual | MTH 515

Dr. Scott | Real Analysis

2/6/2019

## Problem 1.4.3

### Original Solution

#### _Prove that $\cap_{n=1}^{\infty}(0,\frac{1}{n}) = \emptyset$._

Let $n=1$, the interval $I_1$ is $(0,1)$
For $n=2$, the interval $I_2$ is $(0,1/2)$
...
For $n=10$, the interval $I_{10}$ is $(0,1/10)$

Notice that in this manner,

$$I_1 \supseteq I_2 \supseteq ... \supseteq I_{10} ... \supseteq I_n$$

This nested sequence of intervals share the same infimum, 0, regardless of the value of n chosen.  There is no common supremum across the sets as the l.u.b. decreases as n increases.  Thus, if there is a common element across $I_n$ it is the infimum, however we know that 0 is not in the interval defined.  Therefore $\cap_{n=1}^{\infty}(0,\frac{1}{n}) = \emptyset$

### Self-Evaluation

I feel that I had the right idea here, but I did not use the Archimedean property to its full extent.  Rather than relying on the idea that the only common intersection point is the infimum (which I think is still fair to say in this case), I could have used this property to better illustrate the relationship between the intersections.

## Problem 1.4.6

### Original Solution

#### _Which of the following sets are dense in $\mathbb{R}$? Take $p \in$ $\mathbb{Z}$ and $q \in$ $\mathbb{N}$ in every case._

#### _Part A The set of all rational numbers $\frac{p}{q}$ with $q \leq 10$_

This set is not dense.  For example, a number cannot be expressed between $\frac{1}{11}$ and $\frac{1}{12}$.

#### _Part B The set of all rational numbers $\frac{p}{q}$ with $q$ a power of 2_

This set is dense.  The set is always a minimum of $\frac{1}{2^n}$ apart for $n \in$ $\mathbb{N}$.

For two numbers, $b$ and $a$

$$\frac{p}{2^n} < b-a$$
$$a*{2^n} < p < b*{2^n}$$

To prove the left hand side of this expression, 

$$p-1 < 2^n*a <p$$

For the right hand side,

$$p \leq 2^n*a +1$$
$$p < 2^n(b - \frac{1}{2^n})+1$$
$$p = 2^n(b)$$
$$\frac{p}{2^n} < b$$

#### _Part C The set of all rational numbers $\frac{p}{q}$ with $10*|p| \geq q$_

This set is not dense. This set is bounded by $10*|p| \geq q$ so $\frac{p}{q}$ is either 

$$\frac{p}{q} \geq 1/10$$

or 

$$\frac{p}{q} \leq 1/10$$

Thus values outside of this range cannot be found.


### Self-Evaluation

#### Part A

This one I missed.  I misunderstood how the distance between values would work out for this one but now I see how to work through this reasoning.

---

## Problem 1.5.5

### Original Solution

#### _Part A Why is $A \sim A$ for every set $A$?_

When $A \sim A$, then a bijection must exist from $A \rightarrow A$.  This bijection is trivial. As an example $f(x) = x_n*1, \forall x \in$ $A$.

#### _Part B Given sets $A$ and $B$, explain why $A \sim B$ is equivalent to asserting $B \sim A$._

$A \sim B$ is equivalent to $B \sim A$ because if a bijection exists for $A \rightarrow B$, then the inverse of the bijection would be a valid mapping from $B \rightarrow A$.

#### _Part C For three sets $A, B,$ and $C,$ show that $A \sim B$ and $B \sim C$ implies $A \sim C$.  These three properties are what is meant by saying that ~ is an equivalence relation_.

If a bijection exists from $A \rightarrow B$ and $B \rightarrow C$, then a valid bijection can be created that maps $A \rightarrow C$ by combining the bijections that create $A \sim B$ and $A \sim C$.

### Self-Evaluation

No comments.

---

## Problem 1.5.7

### Original Solution

#### _Part A Find a 1-1 function that maps (0,1) into, but not necessarily onto, $S$._

Let $f(x) = y, x \in (0,1)$ is a 1-1 mapping.  The line segment over the open interval is mapped across the diagonal of the unit square starting at the origin.

#### _Part B Use the fact that every real number has a decimal expansion to produce a 1-1 function that maps $S$ into (0,1).  Discuss whether the formulated function is onto._

As mentioned in the problem statement, every real number has a valid decimal expansion.  Using these expansions, one can think of a number, $x$, as a combination of these decimal values.  Such as $x_n$ = $0.x_1 x_2 x_3 ... x_n$

Let $f(x,y)$ be a function that maps an ordered pair $(x,y)$ of the open unit square to interval $(0,1)$ by alternating $x$ and $y$ decimal expansion values.

$$f(x,y) = 0.x_1y_1x_2y_2...x_ny_n$$

I received some help on thinking this question through at the resource listed in [External References](#External-References).


### Self-Evaluation

#### Part A
The intent of my answer matched the solution, however I got a little notationally sloppy and should have specified that $y$ was an ordered pair.

#### Part B
I neglected to include my discussion as to whether or not the function is onto, however I intended to argue that is not onto for the reasons shown in the solution.

---

## Problem 1.5.9

### Original Solution

#### _Part A Show that $\sqrt{2}, \sqrt[3]{2},$ and $\sqrt{3} + \sqrt{2}$ are algebraic._

For $x = \sqrt{2}$

$$x^2 = 2$$
$$x^2 - 2 = 0$$

For $x = \sqrt[3]{2}$

$$x^3 = 2$$
$$x^3 - 2 = 0$$

For $x = \sqrt{3} + \sqrt{2}$

Let 

$$a = (\sqrt{3} + \sqrt{2})^2 = 5 + 2\sqrt{6}$$

So we need something to cancel the term with the square root.

Let 

$$b = (\sqrt{3} + \sqrt{2})^4 = 49 + 20\sqrt{6}$$

Combining these terms

$$b - 10a = -1$$

So the polynomial needs an additional constant of 1.

$$x^4 - 10x^3 + 1$$


#### _Part B Fix $n \in$ $\mathbb{N}$ and let $A_n$ be the algebraic numbers obtained as roots of polynomials with integer coefficients that have degree $n$.  Using the fact that every polynomial has a finite number of roots, show that $A_n$ is countable._

$A_n$ is countable if $A_n \sim \mathbb{N}$.  Because $A_n$ is a set of algebraic numbers, each element of the set can be expressed as a polynomial of degree n.  These polynomials are represented by integer coefficients ($\mathbb{Q} \sim \mathbb{N}$), and the number of unique algebraic numbers per choice of n is finite.  Thus a mapping can be found from $A_n \rightarrow \mathbb{N}$.

#### _Part C Now, argue that the set of all algebraic numbers is countable. What may we conclude about the set of transcendental numbers?_

As discussed above, for a fixed n, $A_n$ is countable.  Then by Theorem 1.5.8 the set of all algebraic numbers is countable.  

We can conclude that the transcendental numbers are not countable because they are contained in $\mathbb{R}$ and $\mathbb{R}$ is not countable.

### Self-Evaluation

#### Part B

It looks like I was on the right track here with this one but maybe left out some important details.  I should have decomposed what $A_n$ is more closely, as shown in the solution, and more carefully described how the pieces of $A_n$ build to form a set that is countable.  I can see how my ideas map to the solution, but the solution is much more explicit.

#### Part C

I took a slightly different approach to show $T$ is not countable, but my answer still holds.

---

## External References

http://demonstrations.wolfram.com/BijectiveMappingOfAnIntervalToASquare/ - A Wolfram program that demonstrates mapping a unit square to a unit line segment.
