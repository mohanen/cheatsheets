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

# Polynomials

## Intro

- involves only the operations of **addition**, **subtraction**, **multiplication**, and **non-negative integer exponents** of variables
- Degree of a polynomial = max exponent

## Binomial Theorem

- Simplifies the algebraic expansion of powers of a binomial
- $(a+b)^2 = sum_(k=0)^n ((n),(k)) a^(n-k) b^k$ where $((n),(k))=(n!)/(k! (n-k)!)$

## Pascal's triangle

![](https://mathbitsnotebook.com/Algebra2/Polynomials/expanded2.png)

- Represents no. of ways a current value can be achieved, eg: $(a+b)^2 = a^2 + ab + ba + b^2$, since order doesn't matter $ab = ba$, therefore 2 ways to get that combination, which is defined by adding the parent values in the triangle.

![](https://www.sitesbay.com/program/images/pascals-triangle.png)

## Expansion vs Factorization

![](https://www.mathsisfun.com/algebra/images/expand-vs-factor-quadratic.svg)

## Polynomial Expansion

- $"Cur. coeff" = ("prev. power of x * prev. coeff of x")/("prev. no. of exp")$

## Factorization Methods

### Common Factor

- $6x^2 − 2x = 0 => 2x(3x − 1) = 0$
- $x= 0 and 1/3$

### Method for Simple Cases

- $ax^2 + bx + c = 0 $
- $ ax^2 + b_1 x + b_2 x + c = 0$ where $b_1 + b_2 = b$ and $b_1 * b_2 = a * c$

### Graphing

![](https://www.freemathhelp.com/images/parabola1.png)

### General Method

- $x = (-b +- sqrt(b^2 - 4 * a * c))/(2 * a)$

## Fundamental theorem of algebra

- n degree of polynomial will have **n roots**
- root = Intersection of the curve when y = 0.
- Some times there will be no intersection when y = 0. In that case, the roots are complex roots.
- Complex roots always comes in **conjugate pairs**.

### Example

- $5x^2 + 6x + 5 = 0$
- $ax^2 + bx + c$ wkt factors $x = (-b +- sqrt(b^2 - 4 * a * c))/(2 * a)$
- $=> x = (-6 +- sqrt(6^2 - 4 * 5 * 5))/(2 * 5)$ $= (-6 +- sqrt(-64))/10$ 
- $ = (-6 +- 8i)/10 = -3/5 +- 4/5 i$ Pair of complex roots

