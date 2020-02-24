# Vectors and spaces

## Vector

- Magnitude + Direction

$vec V= [[x], [y]]$

### Example

1 meter + north (90°) Where 1 unit = 1 meter
$vec V= [[0], [1]]$

### Real coordinate space

- $RR^n$ = nD real coordinate space.

Eg: $vec V in RR^2$

### **Intuition**

> Say you want to move something in a specific direction a single value cannot represent that and you may need a vector.

> Applying a transformation to an Image like rotation, shear, resize, flip..

## Add & Scale Vectors

### Adding vectors

$[[1], [2]] + [[2], [-1]] = [[1 + 2], [2 + (-1)]] = [[3], [1]]$

### Scalar x vector

$2 * [[3], [1]] = [[2 * 3], [2 * 1]] = [[6], [2]]$

### Parametric representations of lines

$vec y = s * vec x + vec t$

### **Intuition**

> Lets assume we wanna rotate an image clockwise 2 times, you can actually calculates where it ends when rotated 2 times and do it in a single operation

## Linear combinations & span

$vec v_1, vec v_2$

### linear combination

- Scaled sum of vectors

$S = {c_1 * vec v_1 + c_2 * vec v_2 | c_n in RR}$

### span

- Area covered in Linear combination of vectors

$Span(vec v_1, vec v_2) = R^2 <=> vec v_1 != c * vec v_2$

$vec v_1 = c * vec v_2 => Span(vec v_1, vec v_2) = R^1$

### **Intuition**

> This allows us to relatively specify one vector as a linear combination of other, so when the other vector changes, the definition will still hold true. So we don't have track or update everything when a vector changed due to some transformation.

## Subspaces

- Set of vectors

### Rules

1. Contains the 0 vector
2. Closed under scalar multiplication
3. Closed under vector addition.

## Linear independence

- Set of vectors that are not linear combinations of other in the set
- Set of vectors with each vector adding new dimensionality to its span
- Such vectors are called **Basis of a Subspace**

### Rules

- Members of set $!=$ any linear combination of the set

### Examples

- S is linearly independent if
  $S = {vec v_1, vec v_2,... vec v_n}$
  $c_1 * vec v_1 + c_2 * vec v_2 + c_n * vec v_n  = 0 <=> c_(0->n) = 0$

### **Intuition**

> Its like the prime number for vectors. In a set, all vectors should be unique and cannot be created from linear combinations of each other.

## Unit Vectors

- ^ denotes unit vector
- Often chose to form **Basis of the Subspace**, like ($hat i, hat j, hat k ...$).
- Normalization = $hat v = vec v/ ||vec v||$

### Rules

- Magnitude = 1

### Example

$hat i = [[1], [0]], hat j = [[0], [1]]$

- Represented in Identity Matrix $[[1, 0], [0, 1]]$

## Linear combinations of unit vectors

- Any vector is a **linear combinations of the unit vectors**
- $vec v = [[1], [2]]$
- $:. vec v = 1 hat i + 2 hat j$
- $= 1 [[1], [0]] + 2 [[0], [1]] = [[1], [0]] + [[0], [2]] = [[1], [2]]$

### **Intuition**

> **Relative way** to denote a vector, and it holds true no matter what **linear transformation** is applied.

## Linear Transformations

- A function thats take in a vector and returns a transformed vector
- Can be represented using the position of unit vectors

### Rules

- All lines must remain lines
- Origin should be fixed

### Example

- Lets assume an operation - Rotations on clockwise
- Before rotation $vec v = 1 hat i + 2 hat j = [[1], [2]]$ from above
- After rotation $hat i = [[0], [-1]]$ and $hat j = [[1], [0]]$
- $vec v = 1[[0], [-1]] + 2[[1], [0]] = [[0+2], [-1+0]] = [[2], [-1]]$
- This Transformation can be represented in a single matrix $[[0, 1], [-1, 0]]$

### **Intuition**

> Applying transformation in images such as rotation, flip, resize

## Dot product

- Sum of the products of the corresponding entries
- $[[a_1], [..], [a_n]] * [[b_1], [..], [b_n]] = a_1 * b_1 + .. + a_n * b_n$
- Product of $||vec a||$ projected on $vec b$ and $||vec b||$
- $vec a * vec b = ||vec a|| cos theta * ||vec b||$

![Projected image](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/dot_product.png)

### **Intuition**

> Allows us to find the angle between the vectors, like if dot product is zero that means they are perpendicular

## Dot product Properties

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

### **Intuition**

> Its just Exploiting the beauty of dot product nothing more

## Triangle inequality

$||vec a + vec b|| <= ||vec a|| + ||vec b||$

![Triangle inequality](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/triangle_inequality.png)

## Cross products

- Only in $RR^3$
- $vec a ** vec b = vec c$ where $vec c$ is perpendicular to $vec a, vec b$
- $||vec a ** vec b|| = ||vec a|| * ||vec b|| sin theta$ = area
- $vec a ** vec b = 0 if vec a = c * vec b$

![Cross Product](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/cross_product.png)

### **Intuition**

> It allows us to find the perpendicular vector and its length will give the area enclosed by the vector which denotes the angle between the vector implicitly

### Cofactor expansion

$vec a ** vec b = [[hat i, hat j, hat k], [a_1, a_2, a_3], [b_1, b_2, b_3]]$
$ = |[a_2 , a_3], [b_2, b_3]|hat i - |[a_1 , a_3], [b_1, b_3]|hat j + |[a_1 , a_2], [b_1, b_2]|hat k $

## Cross product Properties

### Anti-commutative

$vec a ** vec b = - vec b * vec a != vec b * vec a$

### Distributive

$(vec a + vec b) ** vec c = vec a ** vec c + vec b ** vec c$

### Associative

$(c * vec a) ** vec b = c * (vec a ** vec b)$

## Projections

- Projection of $vec x$ on $L = {c * vec v | c in RR}$
- $Proj_L(x)$ = some vector in $L$ where $vec x - Proj_L(x)$ is orthogonal to $L$
- WKT $Proj_L(x) = c * vec v$
- $(vec x - Proj_L(x)) * vec v = 0 because$ orthogonal
- $(vec x - c * vec v) * vec v => vec x * vec v - c * vec v * vec v = 0$
- $c = (vec x * vec v)  / (vec v * vec v) = (vec x * vec v)  / ||vec v||$
- $Proj_L(x) = c * vec v = ((vec x * vec v)  / ||vec v||) vec v$
- Normalized vector $Proj_L(x) = (vec x * hat v) hat v $

## Planes in $RR^3$

### Equation

$Ax + by + cz = D$

### Normal Vector

$vec n = [[A], [B], [C]]$ is a vector perpendicular to the plane

### Normal Vector and Point on Plane

Represent a Plane with a Normal vector and a Point on Plane

- Let $vec n$, two points on plane $P_0 = (x_0, y_0, z_0)$, $P = (x, y, z)$
- $vec v = P - P_0$ will be a vector on the plane
- $:. vec n . vec v = 0 because vec n$ is perpendicular to $vec v$
- $A(x - x_0) + B(y - y_0) + C(z - z_0) = 0$
- $Ax+By+Cz = Ax_0 + By_0 + Cz_0 = D$

## Distance from a point to plane

- Any Point on Plane $P_0$, Distance to be determined Point $P_1 = (x_1, y_1, z_1)$ and Point $P_2$ is perpendicularly projected $P_1$ on plane
- Let $vec a = P_2 - P_1$ & $vec f = P_0 - P_1$
- point to plane Distance = Distance between $P_1$ & $P_2$ = $||vec a||$
- $||vec a|| = ||vec f|| * cos theta = (||vec n|| * ||vec f|| cos theta) / ||vec n|| = (vec n * vec f) / ||vec n||$
- $||vec a|| = (A(x_0 - x_1) + B(y_0 - y_1) + C(z_0 - z_1))/(sqrt(A^2 + B^2 + C^2))$

## Distance between two planes

- Shortest distance = **Perpendicular distance**
- If two Planes **Not parallel** then **distance = 0** since they will intersect at some point
- Distance between || planes = **Normalized difference of the $D$**

# Matrix transformations

## Matrices with vectors

Matrix $A_(m ** n) => vec v_(1..n) in RR^m$

### **Intuition**

> Useful way to represent, manipulate and study linear maps between finite dimensional vector spaces

## Function

- $f(x)=y$ where x is **domain** and y is **co-domain**
- A **Relation** between member of one set with another
- $f: x |-> y$ **Mapping** from one set to another
- A Function is not changing a value its just **associating** to another value

## Vector Transformations

- Function that maps a set of vectors to another set.
- can also be denoted using T
- $T(vec a) = vec b$ or $T:vec a |-> vec b$

## Linear Transformations

- $T(vec x) = bb A_(m**n) * vec x$
- Any Linear transformation can be represented in a Matrix
- If V is subspace, T(V) is also a subspace

### Rules

- $T(vec a + vec b)= T(vec a) + T(vec b)$
- $T(c * vec a)=c * T(vec a)$

## Matrix vector products

- Linear Transformations as Matrix Vector products

### Example

- $bb A_(m ** n) = [[vec v_1, vec v_2, ..., vec v_n]]$ and $vec x = [[x_1], [x_2], [vdots], [x_n]] in RR^n $
- $T(vec x) = {bb A * vec x | x in RR^n } in RR^m$
- $bb A * vec x = x_1 * vec v_1 + x_2 * vec v_2 + ... +x_n * vec v_n$

### **Intuition**

- $bb A$ = resultant **unit vectors after Transformation**
- $vec x$ = linear combination of unit vector

## Identity Matrix

- $bb A$ = Identity Matrix $<=> bb A = [[hat i, hat j, hat k, ...]]$
- $:. T(vec x) = A_(m**n) * vec x = vec x$

### **Intuition**

- Mapping a set of vectors to itself.
- **domain = co-domain**

## im(T): Image of a transformation

- $T(S) = $ image of subset S under T
- $T(R^n) = {S | S in R^m}$
- $:. T(vec x) = A_(m**n) * vec x =$ col space of A $= im(T)$
- im(T) = image of T = co-domain (subset) $in RR^m$

### **Intuition**

Its more like applying limits(domain) to the matrix A to create a subset(image) in co-domain.

## Preimage of a set

- domain = $A sube X$ & co-domain = $S sube Y$
- $T(A) = B sube Y$ = image of subset A under T
- $S sube Y$ that maps to A = ${vec v in Y | T(A) in S}$
- ${vec v in Y | T(A) in S} = T^-1(S) sube A$
- $T^-1(S)$ = Preimage of S under T
- $T(T^-1(S)) sube S$ is because there can exist some elements of S that do not have a matching element in the Preimage A.

## Kernel of Transformation

- $ker(T) = {vec x | T(vec x) = vec 0}$
- Null space of A = N(A) = ${vec x | bb A * vec x = vec 0}$
- $ker(T) = N(A)$

## Scaling of Transformations

- $c* (T(vec x)) = (c*T)(vec x) = c * bb A * vec x$

## Sum of Transformations

- $T:RR^n->RR^m$ and $S:RR^n->RR^m$
- $T(vec x) + S(vec x) = (T+S)(vec x)$
- $bb A * vec x + bb B * vec x = (bb(A+B)) * vec x$
- Sum of Transformations = Sum of Matrices

## 2D Rotation

- Rotate Counter Clockwise by $theta$ in 2D
- $T(hat i) = [[cos theta * ||hat i||],[sin theta * ||hat i||]] = [[cos theta],[sin theta]]$
- $T(hat j) = [[-sin theta * ||hat i||],[cos theta * ||hat i||]] = [[-sin theta],[cos theta]]$
- Transformation Matrix $[[cos theta, -sin theta],[sin theta, cost theta]]$

## 3D Rotation

- Rotate Counter Clockwise by $theta$ in 3D along x-axis
- x-coordinate of all vector = no change, $hat i$ = no change but $hat j & hat k$ = rotated with $theta$
- Transformation Matrix $[[1, 0, 0], [0, cos theta, -sin theta],[0, sin theta, cost theta]]$

## Compositions of linear transformations

- 2 Transformations $S:x->y$ and $T:y->z$ where $x sube RR^n, y sube RR^m, z sube RR^l$
- Composition of T with S $T @ S:x->z$
- $T @ S = T(S(vec x)) = T(A_(m**n) * vec x) $
- $= B_(l**m) (A_(m**n) * vec x) = B * A * vec x = C_(l**n) * vec x$
- $=B [[vec a_1, ..., vec a_n]] vec x = [[B vec a_1, ..., B vec a_n]] vec x$

## Matrix Multiplication

- Applying a transformation to a vector
- Clockwise Rotation Matrix = $[[0, -1], [1, 0]]$ and $vec v = [[1], [2]]$

$[[0, -1], [1, 0]] * [[1], [2]] = 1[[0], [1]] + 2[[-1], [0]] = [[-2], [1]]$

- Lets try Two operations Clockwise Rotation and shear
- Rotation $[[0, -1], [1, 0]]$ and shear $[[1, 0], [1, 1]]$
- Rotation(shear($vec v$)) = Rotation_Shear($vec v$)

$[[0, -1], [1, 0]] [[1, 0], [1, 1]] [[1], [2]] = [[-1, -1],[1, 0]][[1], [2]]$
$[[0, -1], [1, 0]] [[1], [1]] = 1[[0], [1]] + 1[[-1], [0]] = [[-1], [1]]$
$[[0, -1], [1, 0]] [[0], [1]] = 1[[0], [1]] + 1[[-1], [0]] = [[-1], [0]]$

- Order matters but it is Associative

### **Intuition**

> we been told the shortcut about row x column but it is actually how $hat i and hat j$ get changes when transformed

## Matrix Multiplication Properties

### Anti-commutative

$A * B != B * A$

### Distributive

$A * (B + C) = A * B + A * C$

### Associative

$A * (B * C) = (A * B) * C = B * (A * C)$

## Inverse functions

- $f^-1:y->x$ where $f:x->y$
- Mapping from **co-domain to domain**
- Inverse functions are also **linear**

### Rules

- $<=> EE f^-1:y->x$ such that $f^-1 @ f = I_x$ & $f @ f^-1 = I_y$
- $<=> AA y in Y EE$ **a Unique solution** to $f(x)=y$ that is $AA y$ = **surjective** & Unique solution = **injective**
- $<=>$ f is **Bijective**
- $<=>$ Reduced row echelon form of A = $I_(n*n) => rref([A|I]) = [I|A^-1]$

## Surjective & Injective

![mapping](https://www.mathsisfun.com/sets/images/function-mapping.svg)

## Surjective

### Rules

- **onto** = Each element of the co-domain is mapped to by **at least one** element of the domain
- $AA vec y in Y, EE vec x in X$ such that $y = T(x)$
- co-domain = range = C(A) = span of A
- $=> T:RR^n->RR^m = A_(m**n) * vec x$ = surjective $<=> Rank(A) = m$ = No. of pivot entries in reduced row echelon form

## Injective

### Rules

- **1 to 1** = Each element of the co-domain is mapped to by **at most one** element of the domain
- $T(vec x_1) = T(vec x_2) => vec x_1 = vec x_2$ or $vec x_1 != vec x_2 => T(vec x_1) != T(vec x_2)$
- **1 to 1** $=> **N(A)** = {vec 0} =>$ A is **Linearly independent** & forms **basis of C(A)**
- $=> T:RR^n->RR^m = A_(m**n) * vec x$ = Injective $<=> Rank(A) = n$ = No. of pivot entries in reduced row echelon form

## Bijective

### Rules

- If each element of the co-domain is mapped to by **exactly one** element of the domain
- Both **Surjective & Injective**
- $:. T:RR^n->RR^m = A_(m**n) * vec x$ = Bijective $<=> Rank(A) = m = n$

## 2x2 Inverse

- $[A|I]$ = $[[a, b, |, 1, 0], [c, d, |, 0, 1]]$
- $T_1([[c_1],[c_2]]) = [[c_1],[a c_2 - c c_1]]$
- $T_1([A|I]) = [[a, b, |, 1, 0], [0, ad-bc, |, -c, a]]$
- $T_2([[c_1],[c_2]]) = [[(ad-bc)c_1 - b c_2],[c_2]]$
- $=> [[(ad-bc)a, 0, |, ad, -ab], [0, ad-bc, |, -c, a]]$
- $T_3([[c_1],[c_2]]) = [[c_1/((ad-bc)a)],[c_2/(ad-bc)]]$
- $=>[[1, 0, |, d/(ad-bc), -b/((ad-bc))], [0, 1, |, -c/(ad-bc), a/(ad-bc)]]$
- $=> A^-1 = 1/(ad-bc) [[d, -b], [-c, a]]$
- If $ad-bc = 0$ means $A^-1$ is undefined. where $ad-bc = Det(A)$

## Rank of a Matrix

- $A_(m**n)$ = n column vectors with m elements or m row vectors with n elements
- Maximum number of **linearly independent** column or row vectors
- The column rank and the row rank are always equal
- Rank denotes the span/dimension of im(T)
- $Rank(A)$ = No. of pivot entries in reduced row echelon form

## Determinant of a Matrix

- Determinant of 2D Matrix = Area, 3D Matrix = Volume & so on
- Flipping = -ve determinant
- Determinant $!= 0 <=> $ Columns of the matrix are linearly independent

## 2x2 Matrix Determinants

- 2x2 Matrix $det ([[a, c], [b, d]]) = ad - cb$
- For $hat i & hat j$ $det ([[1, 0], [0, 1]]) = 1 * 1 - 0 * 0 = 1$

## 3x3 Matrix Determinants

- $A_(3 ** 3) = [[a_11, a_12, a_13], [a_21, a_22, a_23], [a_31, a_32, a_33]]$

$det(A) = a_11 det(A_11) - a_12 det(A_12) + a_13 det(A_13)$

- $A_11 = [[ a_22, a_23], [a_32, a_33]]$ is the sub matrix formed by **ignoring the row and column it is in** and similarly it is found for $A_12 and A_13$

### Rule of Sarrus

![](https://i.stack.imgur.com/6xWGC.png)

- Memorization scheme for **3×3 determinant**
- Simplifying a 3x3 matrix will lead to a result of $det(A) = (a_1 b_2 c_3 + b_1 c_2 a_3 + c_1  a_2 _b_3 ) - (a_3 b_2 c_1 +  b_3 c_2 a_1 + c_3  a_2 _b_1 )$

## nxn Matrix Determinants

- As we did in 3x3, for nxn matrix also we have to **multiply element and its determinant sub matrix recursively** until it reduce down to 2x2 Matrix
- sign for a element $(i,j)= -1^((i+j))$ forms a checker board pattern
- Choose the row/column with more 0 (so the element multiplied by it sub matrix determinant will be 0) to simplify the calculation.

## Determinant of $k bb A_(n**n)$

### 1 row multiplied by scalar

$|[a, b], [kc, kd]| = kad - kbc = k (ad-bc) = k |[a, b], [c, d]|$

### All row multiplied by scalar

$|[ka, kb], [kc, kd]| = k^2 ad - k^2 bc = k^2 (ad-bc) = k^2 |[a, b], [c, d]|$

### nxn matrix

$det(kA_(n**n)) = k^n det(A_(n**n))$

## Determinant when row is added

- $A = B + C$ doesn't mean $|A| = |B| + |C|$
- $|A| = |B| + |C| iff $ In B and C, all rows except one should be same

### Example

$X = [[a , b], [x_1, x_2]], Y = [[a , b], [y_1, y_2]], Z = [[a , b], [x_1+y_1, x_2 + y_2]]$

- $|X| = ax_2 - bx_1, |Y| = ay_2 - by_1$
- $|Z| = a(x_2+y_2) - b(x_1+y_1)$
- $ = ax_2 - bx_1 + ay_2 - by_1 = |X| + |Y|$

## Duplicate row determinant

- Duplicate rows in $A => rref(A) != I :. A$ is not invertible $=> |A| = 0$

### **Intuition**

- $rref(A) != I$ means that the transformation is squishing the dimension, like a cube to a plane or plane to a line.

## Determinant after row operations

- As row vectors $A = [[vec a_1], [vec a_2]], B = [[vec a_1], [vec a_2 * 3 vec a_1]]$
- $|B| = |[vec a_1], [vec a_2]| + |[vec a_1], [3 vec a_1]| because $ Determinant sum
- $|B| = |A| + 0 because$ Duplicate row $ => det = 0$
- $:.$ Row operations = **No effect** on Determinant

## Triangular matrix determinant

![](https://mathonline.wdfiles.com/local--files/triangular-matrices/Screen%20Shot%202014-06-08%20at%2012.52.45%20PM.png)

- Determinant of Upper or Lower Triangular Matrix = **product of the diagonal elements**.
- Simplify any Matrix to Triangular Matrix using row operations to find determinants easily.

### Example

- $A_(3 ** 3) = [[a_11, a_12, a_13], [0, a_22, a_23], [0, 0, a_33]]$
- $|A| = a_11 |A_11| - 0 * |A_21| + 0 * |A_31|$
- $= a_11 |[a_22, a_23], [0, a_33]| = a_11 (a_22 a_33 - 0) = a_11 a_22 a_33$

## Solving with Matrices

### Gaussian elimination

- solves linear equations by reducing them to row echelon form
- operation allowed
- multiply row by constant $-2r_1 -> r_1$
- switch rows $r_ 1 harr r_2$
- add rows $r_1 + r_2 -> r_2$
- combination of above $-2r_1 + 3r_2 -> r_2$

## Row echelon form

| Row echelon form                                      | **Reduced** Row echelon form                    |
| ----------------------------------------------------- | ----------------------------------------------- |
| $[[1, a_1, a_2 : x], [0, 1, b_1 : y], [0, 0, 1 : z]]$ | $[[1, 0, 0 : x], [0, 1, 0 : y], [0, 0, 1 : z]]$ |

- Row operations on A = Linear Transformation on column vectors of A
- Applying Row operations on $[A|I] = [I|A^-1]$

## Matrix Subspaces

### Null space of a matrix

- $N(A)= {A * vec x = vec 0 | vec x in RR^n}$
- Valid subspace - has $vec o$ & closed under addition & multiplication
- Linearly independent $=> A ** vec x = vec 0 <=> vec x = vec 0 :. N(A) = vec 0$
- Can be Solved with **Gaussian elimination**
- $[[1, 0, 0], [0, 1, 0], [0, 0, 1]] [[x_1], [x_2], [x_3]] = [[0], [0], [0]]$
- **Nullity** = No. of **non pivot** columns in row echelon form

### Column space of a matrix

- $C(A) = Span(vec v_1, vec v_2,.. vec v_n) $
- Valid subspace - has $vec o$ & closed under addition & multiplication
- Linearly independent vectors = **Basis** of Column space = No. of pivot entries in reduced row echelon form = **Rank** of a matrix

### **Intuition**

> Its just the span of the vectors in the matrices
