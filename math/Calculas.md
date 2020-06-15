# Limits and continuity

## Limits

![](https://calcworkshop.com/wp-content/uploads/understanding-limit-notation.png)

- Graphically, **L is the y-value** we approach when we **get closer & closer** to the point where **x = a**
- Limits **doesn't care** what f(x) = ? **when x = a**

### Examples

![](https://i.ytimg.com/vi/PZaI4P7QsaI/maxresdefault.jpg)

## Unbounded limits

- $lim_(x->0) 1/(x^2) = $ **unbounded** (no limit)
- while $lim_(x->0) 1/(x) = $ no limit

## Left & Right hand limits

- Defined by the sign denoted in the power of the approaching value

| Left hand limit     | Right hand limit    |
| ------------------- | ------------------- |
| $lim_(x->a^-) f(x)$ | $lim_(x->a^+) f(x)$ |

- If **Left hand limit $!=$ Right hand limit** then there is **no limit**

## (ε, δ)-definition of limit

![](https://upload.wikimedia.org/wikipedia/commons/d/d1/L%C3%ADmite_01.svg)

- we can make **f(x)** as close as we like to **L** by requiring that **x** be sufficiently close to **c**.
- $0 < |x-a| < delta$ $ => $ $|f(x)-L| < epsilon$

## Properties of limits

- Let $lim_(x->a) f(x) = L$ & $lim_(x->a) g(x) = M$

### Addition

$lim_(x->a) (f(x) + g(x)) = lim_(x->a) f(x) + lim_(x->a) g(x) = L + M$

### Subtraction

$lim_(x->a) (f(x) - g(x)) = lim_(x->a) f(x) - lim_(x->a) g(x) = L - M$

### Multiplication

$lim_(x->a) (f(x) * g(x)) = lim_(x->a) f(x) * lim_(x->a) g(x) = L * M$

### Division

$lim_(x->a) (f(x) / g(x)) = (lim_(x->a) f(x)) / (lim_(x->a) g(x)) = L / M$

### Power

$lim_(x->a) (f(x))^(r/s) = (lim_(x->a) f(x))^(r/s) = L^(r/s)$

### Composite functions

$lim_(x->a) f(g(x)) = lim_(x->a) f(lim_(x->a) g(x)) = lim_(x->a) f(M)$

## Limits by direct substitution

- $f(x)$ is **continuous** at $x = a$ $iff$ $lim_(x->a) f(x) = f(a)$

### Continuous function examples

- $lim_(x->pi) sin(x) = sin(pi) = 0$
- $lim_(x->pi) tan(x) = tan(pi)$ $= sin(pi)/cos(pi) = 0 / -1 = 0$
- $lim_(x->pi) tan(x) = tan(pi/2)$ $= sin(pi/2)/cos(pi/2) = 1 / 0$ = no limit

### Piecewise function examples

> $f(x) = {((x+2)/(x-1) " for " 0 < x <= 4),(sqrt(x) " for " 4 < x):}$

| $lim_(x->4^-) f(x)$ | $lim_(x->4^+) f(x)$ | $lim_(x->4) f(x)$ |
| ------------------- | ------------------- | ----------------- |
| $(4+2)/(4-1) = 2$   | $sqrt(4) = 2$       | $2$               |

> $g(x) = {(sin(x+1) " for " x < -1),(2^x " for " -1 <= x < 5):}$

| $lim_(x->-1^-) g(x)$ | $lim_(x->-1^+) g(x)$ | $lim_(x->-1) g(x)$ |
| -------------------- | -------------------- | ------------------ |
| $sin(-1+1) = 0$      | $2^(-1) = 1/2$       | no limit           |

## Limits using algebraic manipulation

- Let $f(x) = (x^2-x)/(x-1)$
- $lim_(x->1) f(x) = ((1-1)x)/(1-1) = 0/0$ = **undefined ??**
- **No** $f(1)$ is undefined not its limit

> $0/0$ indicates there is a **hole or discontinuity** at the $f(1)$, so we need to algebraic manipulate (factorize, rationalize,...) $f(x)$ for $x!=a$ (making $f(x)$ continuous) and find $f(a)$

- For $x != 1$ we can rewrite $f(x) = (x*(x-1))/(x-1)  = x$
- $:. lim_(x->1) f(x) = 1$


### **Intuition**

![](https://xaktly.com/Images/Mathematics/Continuity/WideDiscontinuityGraph.png)

- $0/0$ indicates there is a **hole or discontinuity**, which means **limits might exist**
- $a/0$ indicates there is an **asymptote**, which means the **limits doesn't exist**

## Strategy in finding limits

![](https://cdn.kastatic.org/ka-perseus-images/a193121287b64721de28fcbfaec9f5919a367dd2.png)