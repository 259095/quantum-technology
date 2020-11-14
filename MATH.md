# MATH NOTES

## Boolean Algebra.
Concerns true or false events.

### De Morgan's laws
```
NOT(A AND B) = NOT(A) OR NOT(B)
```
```
NOT(A OR B) = NOT(A) AND NOT(B)
```
Usign laws we conclude that:
```
A AND B = NOT( NOT(A) OR NOT(B) )
```
Therefore true is that:
```
NOT(NOT(A)) AND NOT(NOT(B)) = A AND B
```

XOR needs quantum assigment in QC at the beginning of the computation (e.g. A = 0)
Assigment is irreversible, but XOR is a reversible operation (e.g. A = A XOR B)

Applying XOR C twice gives us value of variable A.
```
A = B XOR C XOR C -> A = B
```
This concept is widely used in cryptography!

====

## Probability
Probablility, unlike boolean algebra which talks about events we have definite knowledge of, deals with uncertain events.
```
P(A) -> probability of event A
```
---
### Mutually exclusive events. 
Complete set of mutually exclusive events has probability of 1.

```
P(A AND B) = 0
P(A OR B OR C) = P(A) + P(B) + P(C) = 1 
```
---
### Independent events. 
There is no connection between events.

This is why below is true for mutually exclusive and independent events:
```
P(A OR B) = P(A) + P(B) - P(A AND B)
P(A AND B) = P(A) x P(B)
```
--- 

Example of using boolean algebra inside probability algebra.
Always true P(A) = P (A AND TRUE) and B OR NOT(B) = TRUE results in P(A) = P( A AND (B OR NOT(B))) = P((A AND B) OR (A AND NOT(B))) = P(A)

Example for full set of mutually exclusive events (e.g. OR gate)
P(10 OR 11) = P((bit1=1 AND bit2=1) OR (bit1=1 AND NOT(bit2=1) = P(bit1=1) results in P(10) + P(11) = P(that first bit is 1)

Similar for other combinations.
P(01) + P(11) = P(that second bit is 1)
P(00) + P(11) = P(that first bit is 0)
P(10) + P(00) = P(that second bit is 0)

---

### Venn diagrams and conditional probability
For venn diagrams events are represented as regions. Probabilities of events represented as areas of regions.

Examples of conditional probability

Probability of B if A occured: P( B/A ) = P( A AND B) / P(A) 
Probability of A if B occured: P( A/B ) = P( A AND B) / P(B)

====

## Statistics
Concerns uncertain events.

We can map TRUE to +1 and FALSE to -1.

We need a complete set of mutually exclusinve uncertain events. We assign a value to each outcome.


### Mean (estimate or average)
Cosidering dice where v is value of the outcome and P(v) is probablility of the outcome:
Mean = Average = Estimate = v1 P(v1) + v2 P(v2) + v3 P(v3) + v4 P(v4) + v5 P(v5) + v6 P(v6)

(add formula)

E(X+Y) = E(X) + E(Y)

### Standard deviation.
A measure how much random variable diviates from its mean.

Variations: (value - mean)squared

```
Mean of a variations is called variance
```

```
Square root of the variance is called standard deviation
```

### Correlation

Example:

E(XY) test if random variables are correlated or not.

Consider two random variables X and Y
X is -1 with a probability of 0.5, and +1 with a probability of 0.5
Y is -2 with a probability of 0.5, and +2 with a probability of 0.5

Consider the random variable XY and XY can be either -2 or +2. No other values are possible.

Suppose that X and Y are independent. Lets find the probabilities of XY being -2 and +2.

X = -1, Y = -2   XY = +2   Probability = 0.25
X = +1, Y = -2   XY = -2   Probability = 0.25
X = -1, Y = +2   XY = -2   Probability = 0.25
X = +1, Y = +2   XY = +2   Probability = 0.25

This means that P(XY=-2) = 0.5 and P(XY=+2) = 0.5

E(XY) = 0.5x-2 + 0.5x+2 = 0

Instead, suppose that X and Y are related to one another. For instance, lets say that Y = 2X

Lets find the probabilities of XY being -2 and +2

X = -1, Y = -2   XY = +2   Probability = 0.5
X = +1, Y = +2   XY = +2   Probability = 0.5

In other words, the only value possible for XY is +2. 
This means that P(XY=+2) = 1

E(XY) = +2

When X and Y are independent of each other, E(XY) = 0
But when X and Y are related, the value of E(XY) is likely to be different from 0. In the example, we studied above, where Y = 2X, E(XY) was +2

This can be used to find out if random variables in the real world are independent or not.

Suppose you have two real-world random variables A and B.

A is -1 with a probability of 0.5
A is +1 with a probability of 0.5
B is -2 with a probability of 0.5
B is +2 with a probability of 0.5

You measure AB over a billion experiments and find that the average value of AB you obtained through experiments is 0.7

This tells you that A and B are most likely not independent of each other.

If they had been independent, then over a billion experiments, the average of AB would have been much closer to 0.

In this way, the expected value can be used to determine if random variables are independent or not.

## Complex numbers

```
a + bi
```
```
(-4)^(1/2) = (-1)^(1/2) x 4^(1/2) = i x 4^(1/2) = 2 i
```
```
i^(1/2) = (1+i)/(2^(1/2))
```
```
k(a + bi) = ka + kbi
```

Treat i as any other variable.

### Complex conjugate

Change the sign of imaginary part.

### Squared magnitude

Mutiply a complex number by its complex conjugate.

| a + bi|^2 = a^2 + b^2

### Complex division

Multiply both numerator and denominator by the complex conjugate of the denominator.

### Euler's Formula

e^ix = cos(x) + isin(x)

Any complex number whose squared magnitude is 1 can be written in the form a + bi = cos(x) + isin(x) = e^ix

### Polar Form

re^ix

(TBE)

### Fractional powers

Use Polar Form to represent number you want to compute fractional powers for.

(TBE)