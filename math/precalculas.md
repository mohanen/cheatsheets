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