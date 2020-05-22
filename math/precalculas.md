# Complex numbers

## imaginary number

- $x^2 = -1$ it is **impossible to square a real number and get a negative number**
- However, a solution does exist in a new number system called the **complex number system**

### imaginary unit

- $i = sqrt(-1)$ is an imaginary unit
  > The previously unsolvable equation is now solvable. $x = i$

### Pure imaginary numbers

- A complex number that has no real part

### powers of i

| $i^0$ | $i^1$ | $i^2$ | $i^3$ | $i^4$ | $i^5$ | $i^6$ | $i^7$ | ... |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | --- |
| 1     | i     | -1    | -i    | 1     | i     | -1    | -i    | ... |

## Complex numbers

- Real numbers + imaginary unit
- Standard form is **z = a + bi**
- Eg: $z = 5 + 4i$, where $Re(z) = 5$ & $Im(z) = 4$
- A Complex number is a point in a 2D Plane where Real part is x, imaginary is y
- The representation in a 2D Plane is called **Argand Diagram**

## Operations

### Addition

- $(4 + 3i) + (5 + 2i) = 9 + 5i$

### Subtraction

- $(4 + 3i) - (5 + 2i) = -1 + i$

### Multiplication

- $(4 + 3i) * (5 + 2i) = 20 + 8i + 15i + 6i^2 $ $= 20 + 23i -6 = 14 + 23i because i^2 = -1$

### Division

- With the help of conjugates.
- $(4 + 3i) / (5 + 2i) = ((4 + 3i) / (5 + 2i)) * ((5 - 2i) / (5 - 2i))$
- $= (20 - 8i + 15i - 6i^2)/(5^2 - (2i)^2) = (26+7i)/(29) = 26/29 + 7/29 i$

## Properties

- Let $z_1 = a_1 + b_1 i$ & $z_2 = a_2 + b_2 i$

### Distance

- $sqrt(a_1 - a_2 + b_1 - b_2)$

### Midpoint

- $(a_1 + a_2)/2 + (b_1 + b_2)/2 i$

### Conjugate

- $bar z = a - b i$
- $z * bar z = (a + b i) * (a - b i) $ $= a^2 - (b i)^2 = a^2 + b^2 = |z|^2$

## Absolute

- Absolute = Length
- $|a + b i| = sqrt(a^2 + b^2) = |z|$

### **Intuition**

- Absolute value of a real number is its distance from 0, similarly for complex numbers its the distance from origin **(0, 0)** to the position **(a, b)** in a **complex plane**.

## Other representation

- Complex number is a point in a 2D plan and can also be represented, with a angle $phi$ and length $|z|$

### $a+bi$ $->$ $phi and |z|$

- $|z| = sqrt(a^2 + b^2)$
- $phi = tan^-1(b/a)$

### $phi and |z|$ $->$ $a+bi$

- $a = |z| cos(phi)$
- $b = |z| sin(phi)$

## complex numbers Forms

### Rectangular

- $a+bia+bi$

### Polar

- In terms of angle and length
- $r (cos θ + i sin θ)$ where $r = |z|$

### Exponential

- $r * e^iθ$
- $because$ Euler's Expansion

## Multiplication in other Forms

### Polar

- $r_1 (cos θ_1 + i sin θ_1) * r_2 (cos θ_2 + i sin θ_2)$
- $= r_1 * r_2 (cos (θ_1 - θ_2) + i sin (θ_1 + θ_2))$

### Exponential

- $r_1 e^iθ_1 * r_2 e^iθ_2 $
- $= r_1 * r_2  e^i(θ_1 + θ_2)$

## Division in other Forms

### Polar

- $(r_1 (cos θ_1 + i sin θ_1)) / (r_2 (cos θ_2 + i sin θ_2))$
- $= r_1/r_2 (cos (θ_1 - θ_2) + i sin (θ_1 - θ_2))$

### Exponential

- $(r_1 * e^iθ_1) / (r_2 * e^iθ_2) = r_1/r_2 * e^i(θ_1 - θ_2)$

## Powers of complex number

- $(r * e^iθ)^x = r^x * e^(i(xθ))$

### Easy way to deal with powers

- Convert to **polar form**
- Apply powers to the **distance** and **angle**
- Convert back to rectangular form

# Polynomials

## Intro

- involves only the operations of **addition**, **subtraction**, **multiplication**, and **non-negative integer exponents** of variables
- Degree of a polynomial = max exponent

## Pascal's triangle

![](https://mathbitsnotebook.com/Algebra2/Polynomials/expanded2.png)

![](https://www.sitesbay.com/program/images/pascals-triangle.png)

## Binomial Theorem

- Simplifies the algebraic expansion of powers of a binomial
- $(a+b)^2 = sum_(k=0)^n ((n),(k)) a^(n-k) b^k$ where $((n),(k))=(n!)/(k! (n-k)!)$

## Expansion vs Factorization

![](https://www.mathsisfun.com/algebra/images/expand-vs-factor-quadratic.svg)

## Polynomial Expansion

- $"Cur. coeff" = ("prev. power of x * prev. coeff of x")/("prev. no. of exp")$

## Factorization

$x = (-b +- sqrt(b^2 - 4 * a * c))/(2 * a)$

## Complex Roots

- Fundamental theorem of algebra states **n degree polynomial will have n roots**
- root = Intersection of the curve when y = 0.
- Some times there will be no intersection when y = 0. In that case, the roots are complex roots.
- Complex roots always comes in **conjugate pairs**.

### Example

- Factorize $5x^2 + 6x + 5 = 0$
- $=> x = (-6 +- sqrt(6^2 - 4 * 5 * 5))/(2 * 5)$ $= (-6 +- sqrt(-64))/10$
- $ = (-6 +- 8i)/10 = -3/5 +- 4/5 i$ Pair of complex roots

# Trigonometry

## Ratios

![](https://cdn.kastatic.org/googleusercontent/jmY_4JbfbZhffU-tehV84DZIcmCKn1IfNAgSK8bkDRxBEd_mZNvhhaXQ2FaeUXqlQYi032pGsyF265nbejlrMD0C)

> **SOH-CAH-TOA** : an easy way to remember trig ratios

## Inverse trig functions

- Denoted by **arc** or $""^-1$
- $sin^-1("opp"/"adj") = θ$

### Misconception

- $sin^-1 != 1/sin$

## Pythagorean trig identity

- $hyp^2 = adj^2 + opp^2$

## Reciprocal trig ratios

| Trig ratio    | Reciprocal Trig tatio |
| ------------- | --------------------- |
| sine (sin)    | cosecant (csc)        |
| cosine (cos)  | secant (sec)          |
| tangent (tan) | cotangent (cot)       |

## The law of sines

![](https://www.onlinemathlearning.com/image-files/xlaw-of-sines.png.pagespeed.ic.fbZNTNAs6j.png)

## The law of cosines

![](https://www.onlinemathlearning.com/image-files/xlaw-of-cosines.png.pagespeed.ic.xmYFXUz4Xc.png)

## Radians

- Radians is the SI standards

![](https://jarnowouda.com/wp-content/uploads/elementor/thumbs/05_Dividing-a-circle-in-radians-nww2awice6dh1j57cboqso2fdcsegqnkxlqekgy2vg.png)

### Conversions

- Degree $=>$ Radian $= ** pi/180$
- Radian $=>$ Degree $= ** 180/pi$

## Unit Circle (cos, sin)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Unit_circle_angles_color.svg/1024px-Unit_circle_angles_color.svg.png)

## Range of inverse trig functions

- wkt a function is inverse $iff$ the function is **one to one relation**.
- And in a unit circle, multiple θ leads to same value. So in order to be inverse the **θ's range must be limited** so that it won't map to same value again.

### Range

| Trig ratio | Radians           | Degree           |
| ---------- | ----------------- | ---------------- |
| arcsin (θ) | $-pi/2$ to $pi/2$ | $-90°$ to $+90°$ |
| arccos (θ) | $0$ to $pi$       | $0°$ to $180°$   |
| arctan (θ) | $-pi/2$ to $pi/2$ | $-90°$ to $+90°$ |

## sinusoidal function

 - Functions that can be produced by shifting, stretching or compressing the **sine function**

## unit circle symmetry

![](https://www.analyzemath.com/high_school_math/grade_11/trigo/unit_circle_symmetry.gif)

- This gives us the relations of trig ratios over θ, such as $sin θ = sin (pi - θ)$ while $cos θ = -cos (pi - θ)$
- Since **cos is symmetry along x-axis, sin along y-axis and tan along xy diagonal**

## Angle addition identities

![](https://www.cut-the-knot.org/triangle/SinCosAddition.gif)

### Sin 

- $sin(α + β) = sin α cos β + cos α sin β$
- $sin(α - β) = sin α cos β - cos α sin β$

### Cos

- $cos(α + β) = cos α cos β - sin α sin β$
- $cos(α - β) = cos α cos β + sin α sin β$

### Tan

- $tan(α + β) = (tan α + tan β)/(1 - tan α tan β)$
- $tan(α - β) = (tan α - tan β)/(1 + tan α tan β)$

## Pythagorean formula

- $sin^2 θ + cos^2 θ = 1$
- $tan^2 θ + 1 = sec^2 θ$
- $cot^2 θ + 1 = csc^2 θ$

## Double angle formulas

- $sin 2θ = 2 sin θ cos θ$
- $cos 2θ = {(cos^2 θ - sin^2 θ), (2 cos^2 θ -1) ,(1 -2 sin^2 θ):}$
- $tan 2θ = (2 tan θ) / (1 - tan^2 θ) $

## Half angle identities

- $sin (θ/2) = +- sqrt((1 -cos θ)/2)$
- $cos (θ/2) = +- sqrt((1 +cos θ)/2)$
- $tan (θ/2) = (sin θ)/(1 + cos θ)$

## Periodicity of trig functions

- $sin(2 pi + θ) = sin θ$
- $cos(2 pi + θ) = cos θ$
- $tan(pi + θ) = tan θ$

## Symmetry identities

- $sin(-θ) = - sin θ$
- $cos(-θ) = cos θ$
- $tan(-θ) = - tan θ$

##  Co-function identities

- $cos θ = sin(pi/2 - θ)$
- $sin θ = cos(pi/2 - θ)$
- $tan θ = cot(pi/2 - θ)$
- $cot θ = tan(pi/2 - θ)$
- $csc θ = sec(pi/2 - θ)$
- $sec θ = csc(pi/2 - θ)$

# Sequences & Series

## Sequences

- Ordered lists / progression of numbers
- Some sequences follow a specific pattern that can be used to extend them indefinitely
- Most of sequences can be represented by formulas

### 2 Types

- Finite ${a_k}_(k=1)^4 = {1,3,5,7}$
- Infinite ${a_k}_(k=1)^∞ = {1,3,5,7,...}$

### Explicit Function Definition

- ${a_k}_(k=1)^4$ with $a_k = 1 + 2(k-1)$

### Recursive Function Definition

- ${a_k}_(k=1)^4$ with $a_k = a_(k-1) + 2$

## Arithmetic sequences

- Each terms after first is found by **adding a constant** to the previous term
- It is a **linear function**, Instead of $y=mx+b$, we write $a(n)=dn+c$

| Recursive Function  | Explicit Function     |
| ------------------- | --------------------- |
| $a_k = a_(k-1) + d$ | $a_k = a_1 + d*(k-1)$ |

## Geometric sequences

- Each terms after first is found by **multiplying a constant** to the previous term
- It is an **exponential function**, and can expressed in $a(n)=d^n * c$

| Recursive Function  | Explicit Function     |
| ------------------- | --------------------- |
| $a_k = a_(k-1) * d$ | $a_k = a_1 * d^(k-1)$ |

## Series

- **Sum of sequences**
- $sum_(i=1)^n a_i$

## Finite Geometric series

- Let $S_n = a + a r +... + a r^(n-1) -> (1)$
- $(1)*-r =>$ $-r S_n = -a r - a r^2 - ... - a r^n -> (2)$
- $(1)+(2) =>$ $S_n - r S_n = a - a r^n$
- $:. S_n = (a(1 - r^n))/(1-r)$

### sigma notation

- $sum_(i=1)^n a r^i = a + a r +... + a r^n$

## Finite Arithmetic Series

- Let $S_n = a + (a + r) +... + (a + r(n-1)) -> (1)$
- $reversed (1) =>$ $S_n = (a + r(n-1)) + ... + a -> (2)$
- $(1)+(2) =>$ $2S_n = (2a + r(n-1)) + ... + (2a + r(n-1))$
- $:. S_n = (n(2a + r(n-1)))/2$ $= (n( a + (a + r(n-1))))/2= n(a_1 + a_n)/2$

### sigma notation

- $sum_(i=1)^n a + r * i = a + (a + r) +... + (a + r * n)$

# Conic sections

## Introduction

![](https://www.cliffsnotes.com/assets/256137.png)

- Sections formed from **intersecting a plane and a cone**

## Standard equation of a circle

![](https://www.mathsisfun.com/algebra/images/graph-circle-b.svg)

- $(x-h)^2 + (y-k)^2 = r^2$ where center $= (h,k)$

## Ellipse

![](https://dr282zn36sxxg.cloudfront.net/datastreams/f-d%3A259f07ca71fee9c2e5c937d11c42402c481c5751b5c1422720a2c936%2BIMAGE_TINY%2BIMAGE_TINY.1)

- A circle is a special case of ellipse
- Ellipse in center $x^2/a^2 + y^2/b^2 = 1$ where a = x-axis radius, b = y-axis radius
- General ellipse $(x-h)^2/a^2 + (y-k)^2/b^2 = 1$

### Focus

- The distance between each focus and the center is called the **focal length** of the ellipse
- **Sum of the distances from the foci** to each point on the ellipse is always the **same**.
- $f_1 + f_2 = 2 a$ and $f^2 = a^2 - b^2$

## Parabola

![](https://usercontent1.hubstatic.com/14702916_f1024.jpg)

- Parabolas are commonly known as the graphs of **quadratic functions**
- Focus = a point $(a, b)$
- Directrix = a line $y = k$
- For any point on the parabola, **distance from focus = distance from directrix**
- $(y-k)^2 = (x-a)^2 + (y-b)^2$ where (a,b) = focus, k = directrix and (x,y) = point on parabola

## Hyperbola

![](https://ugc.futurelearn.com/uploads/images/c5/b5/hero_c5b54066-737a-462b-b470-21e7ea552e4d.png)

- It more like inverted ellipses where one the vertex would be negative in ellipse equation. $x^2/a^2 - y^2/b^2 = 1$ or $ - x^2/a^2 + y^2/b^2 = 1$

### Opens in the +ve axis of the equation

- Let $x^2/a^2 - y^2/b^2 = 1$
- for $y = 0$ $=> x=sqrt(a^2) = +- a$ curve intersects at +a and -a
- but for $x = 0$ $=> y=sqrt(-(b^2))$ leads to complex roots
- so there will be no intersection in the y axis, which means it opens along **x-axis which is +ve**

### Focus

- **Difference of the distances from the foci** to each point on the hyperbola is always the **same**.
- $|f_1 - f_2| = 2 a$ and $f^2 = a^2 + b^2$

# Probability and combinatorics

## Probability

- Probability is simply **how likely something is to happen**.
- $"# of possibility met by condition"/"# of all possibilities"$
- **Sample space** = set of all possible outcomes

![](https://www.wikihow.com/images/thumb/f/fa/Calculate-Probability-Step-3-Version-5.jpg/aid1345372-v4-728px-Calculate-Probability-Step-3-Version-5.jpg.webp)

## Addition rule

- The probability of getting a **jack or hearts** in a deck with out joker.
- Since there is a **jack of hearts** overlapping both set, we have to **subtract the overlap** part once.
- $= ("# of jacks " + " # of hearts " - " # of jack of hearts")/"# of cards" $
- **P(A *or* B) = P(A) + P(B) - P(A *and* B)**

## Compound independent events

### Getting 2 sides same in a die

![](https://www.edcollins.com/backgammon/diceposs.gif)

- In the first roll anything i get can be considered desirable $:. P(A)=6/6$ and the second roll i should be getting what i got in the first roll $:. P(B)=1/6$
- getting 2 sides same $ =  6/6 * 1/6 = 1/6$

### Getting THH in a coin flip

- Both H and T have equally likely events
- $P(THH) = P(T) * P(H) * P(H) $ $= 1/2 * 1/2 * 1/2 = 1/8$

## Dependent events

### Picking Marbles in a bag

- A bag has 3 green and 2 blue marbles.
- The probability of picking 2 green marbles P(G)
- $P(G)=P(1^(st)" marble") + P(2^(nd) " marble")$
- $P(1^(st) " marble") = 3/5$
- $P(2^(nd) " marble") = 2/4 = 1/2$ $ because $ first marble is already taken out, second is taken from the remains
- $P(G) = 3/5 * 1/2 = 3/10 = 33%$


## The Monty Hall problem

![](https://upload.wikimedia.org/wikipedia/en/3/32/Monty_Hall_Diagram.png)

- Choosing car in the first time $P("car") = 1/3$
- Choosing goat in the first time $P("goat") = 2/3$
- In $2^(nd)$ time, **always switching** = $P("car") = 2/3$ and **not switching** $P("car") = 1/3$

### **Intuition**

- The second time switching might look like a fifty fifty probability but its not because its a **dependent event** and in the previous event you had higher probability of losing.
