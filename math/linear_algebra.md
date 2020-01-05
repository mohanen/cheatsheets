# Vectors and spaces

## Vector

- Magnitude + Direction

$vec V= [[x], [y]]$

### Example

1 meter + north (90°) Where 1 unit = 1 meter
$vec V= [[0], [1]]$

### Real coordinate space

- $RR^n$ - nD real coordinate space.

Eg: $vec V in RR^2$

### Unit vector

- Vector with magnitude 1
- $hat$ denotes unit vector

Eg: $hat i = [[0], [1]], hat j = [[1], [0]]$

## Add & Scale Vectors

### Adding vectors

$[[1], [2]] + [[2], [-1]] = [[1 + 2], [2 + (-1)]] = [[3], [1]]$

### Scalar x vector

$2 * [[3], [1]] = [[2 * 3], [2 * 1]] = [[6], [2]]$

### Parametric representations of lines

$vec y = s * vec x + vec t$

## Linear combinations & span

$vec v_1, vec v_2$

### linear combination

- Scaled sum of vectors

$S = {c_1 * vec v_1 + c_2 * vec v_2 | c_n in RR}$

### span

- Area covered in Linear combination of vectors

$Span(vec v_1, vec v_2) = R^2 <=> vec v_1 != c * vec v_2$

$vec v_1 = c * vec v_2 => Span(vec v_1, vec v_2) = R^1$

## Linear independence

- Set of vectors that are not linear combinations of other in the set
- set of vectors with each vector adding new dimentionality to its span
- S is linearly independent if
  $S = {vec v_1, vec v_2,... vec v_n}$
  $c_1 * vec v_1 + c_2 * vec v_2 + c_n * vec v_n  = 0 <=> c_(0->n) = 0$

## Dot product

$vec a = [[a_1], [a_2], [..], [a_n]], vec b [[b_1], [b_2], [..], [b_n]],.. in RR^n$

- Sum of the products of the corresponding entries

$vec a * vec b = a_1 * b_1 + a_2 * b_2 + .. + a_n * b_n$

- Multiplied length of $vec a$ projected on $vec b$ and $vec b$
- (projected $||vec a||$) x ($||vec b||$)
- $vec a * vec b = ||vec a|| cos theta * ||vec b||$

![Projected image](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/dot_product.png)

### Commutative

$vec a * vec b = vec b * vec a$

### Distributive

$(vec a + vec b) * vec c = vec a * vec c + vec b* vec c$

![Distributive image](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/dot_product_distributive.png)

### Associative

$(c * vec a) * vec b = c * (vec a * vec b)$

## Length of a Vector

$||vec a|| = sqrt (a_1^2 + a_2^2 + a_n^2)$

### Dot product and Length

$vec a * vec b = a_1^2 +  a_2^2 + .. + a_n^2 $

$:. ||vec a||^2 =vec a * vec b $

## Cauchy-Schwarz inequality

$|vec a * vec b| <= ||vec a|| * ||vec b||$

$|vec a * vec b| = ||vec a|| * ||vec b|| <=> vec a = c * vec b$

## Triangle inequality

$||vec a + vec b|| <= ||vec a|| + ||vec b||$

![Triangle inequality](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/triangle_inequality.png)

## Cross products

- Only in $RR^3$
- $vec a ** vec b = vec c$ where $vec c$ is perpendicular to $vec a, vec b$
- $||vec a ** vec b|| = ||vec a|| * ||vec b|| sin theta$ = area
- $vec a ** vec b = 0 if vec a = c * vec b$

![Cross Product](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/cross_product.png)

### Cofactor expansion

$vec a ** vec b = [[hat i, hat j, hat k], [a_1, a_2, a_3], [b_1, b_2, b_3]]$

$ = |[a_2 , a_3], [b_2, b_3]|hat i - |[a_1 , a_3], [b_1, b_3]|hat j + |[a_1 , a_2], [b_1, b_2]|hat k $

### Anti-commutative

$vec a ** vec b = - vec b * vec a != vec b * vec a$

### Distributive

$(vec a + vec b) ** vec c = vec a ** vec c + vec b ** vec c$

### Associative

$(c * vec a) ** vec b = c * (vec a ** vec b)$

## Planes in $RR^3$

### Equation

$Ax + by + cz = D$

### Normal Vector

$vec n = [[A], [B], [C]]$ is a vector ⟂ to the plane

### Normal Vector and Point on Plane

- Let $vec n$, two points on plane $P_0 = (x_0, y_0, z_0)$, $P = (x, y, z)$
- $vec v = P - P_0$ will be a vector on the plane
- $:. vec n . vec v = 0 because vec n$ is ⟂ to $vec v$
- $A(x - x_0) + B(y - y_0) + C(z - z_0) = 0$
- $Ax+By+Cz = Ax_0 + By_0 + Cz_0 = D$

### Distance from a point to plane

- Any Point on Plane $P_0$, Distance to be determined Point $P_1 = (x_1, y_1, z_1)$ and Point $P_2$ is ⟂ly projected $P_1$ on plane
- Let $vec a = P_2 - P_1$ & $vec f = P_0 - P_1$
- point to plane Distance = Distance between $P_1$ & $P_2$ = $||vec a||$
- $||vec a|| = ||vec f|| * cos theta = (||vec n|| * ||vec f|| cos theta) / ||vec n|| = (vec n * vec f) / ||vec n||$
- $||vec a|| = (A(x_0 - x_1) + B(y_0 - y_1) + C(z_0 - z_1))/(sqrt(A^2 + B^2 + C^2))$

### Distance between two planes

- Shortest distance = **Perpendicular distance**
- If two Planes **Not parallel** then **distance = 0** since they will intersect at some point
- Distance between || planes = **Normalized difference of the $D$**
