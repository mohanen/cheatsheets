# Vectors and spaces

## Vector

### Magnitude + Direction

| Dimension | Direction | Magnitude |
| --------- | --------- | --------- |
| **1D**    | sign      | Value     |
| **2D**    | angle     | Value     |

- In **2D** it can also be denoted by how much it goes in each Dimension
- $\vec v= \begin{bmatrix} x \\ y \end{bmatrix}$

### Example

- 1 meter + north (90°) Where 1 unit = 1 meter
- $\vec v= \begin{bmatrix} 0 \\ 1 \end{bmatrix}$

### **Intuition**

- Say you want to move something in a specific direction a _single value cannot represent that_ and you may need a vector.
- Applying a transformation to an Image like \_rotation, shear, resize, flip...

## Real coordinate space

- $\Reals^n$ = **nD** real coordinate space.

### Example

$\vec v \in \Reals^2$ - means its a **2D** vector

## Add & Scale Vectors

### Adding vectors

$$\begin{bmatrix} 1 \\ 2 \end{bmatrix} + \begin{bmatrix} 2 \\ -1 \end{bmatrix} = \begin{bmatrix} 1+2 \\ 2+(-1) \end{bmatrix} = \begin{bmatrix} 3 \\ 1 \end{bmatrix}$$

### Scalar x vector

$$2 \cdot \begin{bmatrix} 3 \\ 1 \end{bmatrix} = \begin{bmatrix} 2 \cdot 3 \\ 2 \cdot 1 \end{bmatrix} = \begin{bmatrix} 6 \\ 2 \end{bmatrix}$$

### Parametric representations of lines

$$\vec y = s \cdot \vec x + \vec t$$

### **Intuition**

> Lets assume we wanna **move an object 2 times**, you can actually calculate where it ends when moved 2 times and do it **in a single operation**

## linear combination

- Scaled sum of vectors

$$S = { \left \lbrace c_1 \cdot \vec v_1 + c_2 \cdot \vec v_2 | c_n \in \Reals \right \rbrace }$$

## span

- Area covered in Linear combination of vectors

$$Span(\vec v_1, \vec v_2) = \Reals^2 \iff \vec v_1 \not = c \cdot \vec v_2$$

$$\vec v_1 = c \cdot \vec v_2 \implies Span(\vec v_1, \vec v_2) = \Reals^1$$

## Linear independence

- Set of vectors that are not linear combinations of other in the set
- set of vectors with each vector adding new dimentionality to its span
- Such vectors are called **Basis of a Subspace**
- $S = \lbrace \vec v_1, \vec v_2, \cdots , \vec v_n \rbrace$ is linearly independent if
  $c_1 \cdot \vec v_1 + c_2 \cdot \vec v_2  +  \cdots+ c_n \cdot \vec v_n  = 0 \iff c_{0 \to n} = 0$

### **Intuition**

> Its like the prime number for vectors. In a set, all vectors should be unique and cannot be created from linear combinations of each other.

## Unit Vectors

- Vector with magnitude 1
- $hat$ denotes unit vector
- Unit vectors are **Basis of the Subspace** it is in.

### Example

$$\hat i = \begin{bmatrix} 1 \\ 0 \end{bmatrix}, \hat j = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$$

### Denoting vectors in terms of unit vectors

- Any vector can be denoted in terms of **linear combinations of the unit vectors**

$$\vec v = \begin{bmatrix} 1 \\ 2 \end{bmatrix} = 1 \hat i + 2 \hat j$$

### **Intuition**

> **Relative way** to denote a vector, and it holds true no matter what **linear transformation** is applied.

## Linear Transformations

- A function thats take in a vector and returns a transformed vector
- Can be represented using the position of unit vectors

### Rules

- **All lines must remain lines**
- **Origin should be fixed**

### Example

- Lets assume an operation - **Rotations on clockwise**
- Before rotation $\vec v = 1 \hat i + 2 \hat j = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$ from above
- After rotation $\hat i = \begin{bmatrix} 0 \\ -1 \end{bmatrix}$ and $\hat j = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$

$$\vec v = 1 \cdot \begin{bmatrix} 0 \\ -1 \end{bmatrix} + 2 \cdot \begin{bmatrix} 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 0+2 \\ -1+0 \end{bmatrix} = \begin{bmatrix} 2 \\ -1 \end{bmatrix}$$

- This can be represented in a single matrix $\begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}$

### **Intuition**

> Applying transformation in images such as _rotation, flip, resize_

## Dot product

- Sum of the products of the corresponding entries
  $$\begin{bmatrix} a_1 \\ \vdots \\ a_2 \end{bmatrix} + \begin{bmatrix} b_1 \\ \vdots \\ b_2 \end{bmatrix} = a_1 \cdot b_1 + \cdots + a_n \cdot b_n$$
- Product of $\|\vec a\|$ projected on $\vec b$ and $\|\vec b\|$

$$\vec a \cdot \vec b = \|\vec a\|  \cos  \theta \cdot \|\vec b\|$$

![Projected image](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/dot_product.png)

### **Intuition**

> Allows us to find the angle between the vectors, like if dot product is zero that means they are perpendicular

## Dot product Properties

### Commutative

$$\vec a \cdot \vec b = \vec b \cdot \vec a$$

### Distributive

$$(\vec a + \vec b) \cdot \vec c = \vec a \cdot \vec c + \vec b \cdot \vec c$$

![Distributive image](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/dot_product_distributive.png)

### Associative

$$(c \cdot \vec a) \cdot \vec b = c \cdot (\vec a \cdot \vec b)$$

## Length of a Vector

$$\|\vec a\| =  \sqrt {(a_1^2 + a_2^2 + a_n^2)}$$

### Dot product and Length

$$\vec a \cdot \vec b = a_1^2 +  a_2^2 + .. + a_n^2 $$

$$\therefore \|\vec a\|^2 =\vec a \cdot \vec b $$

## Cauchy-Schwarz inequality

$$|\vec a \cdot \vec b| \le \|\vec a\| \cdot \|\vec b\|$$

$$|\vec a \cdot \vec b| = \|\vec a\| \cdot \|\vec b\| \iff \vec a = c \cdot \vec b$$

### **Intuition**

> Its just Exploiting the beauty of dot product nothing more

## Triangle inequality

$$\|\vec a + \vec b\| \le \|\vec a\| + \|\vec b\|$$

![Triangle inequality](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/triangle_inequality.png)

## Cross products

- Only in $\Reals^3$
- $\vec a * \vec b = \vec c$ where $\vec c$ is perpendicular to $\vec a, \vec b$
- $\|\vec a * \vec b\| = \|\vec a\| \cdot \|\vec b\|  \sin  \theta$ = area
- $\vec a * \vec b = 0 if \vec a = c \cdot \vec b$

![Cross Product](https://github.com/mohanen/cheatsheets/raw/master/math/linear_algebra/cross_product.png)

### **Intuition**

> It allows us to find the perpendicular vector and its length will give the area enclosed by the vector which denotes the angle between the vector implicitly

### Cofactor expansion

$$\vec a * \vec b = \begin{bmatrix} \hat i & \hat j & \hat k \\ a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \end{bmatrix}$$

$$ = \hat i \cdot \begin{vmatrix} a_2 & a_3 \\ b_2 & b_3 \end{vmatrix} - \hat j \cdot  \begin{vmatrix} a_1 & a_3 \\ b_1 & b_3 \end{vmatrix} + \hat k \cdot  \begin{vmatrix} a_1 & a_2 \\ b_1 & b_2 \end{vmatrix}$$

## Cross product Properties

### Anti-commutative

$\vec a * \vec b = - \vec b \cdot \vec a \not = \vec b \cdot \vec a$

### Distributive

$(\vec a + \vec b) * \vec c = \vec a * \vec c + \vec b * \vec c$

### Associative

$(c \cdot \vec a) * \vec b = c \cdot (\vec a * \vec b)$

## Planes in $\Reals^3$

### Equation

$Ax + by + cz = D$

### Normal Vector

$\vec n = \begin{bmatrix} A \\ B \\ C \end{bmatrix}$ is a vector perpendicular to the plane

### Normal Vector and Point on Plane

- Let $\vec n$, two points on plane $P_0 = (x_0, y_0, z_0)$, $P = (x, y, z)$
- $\vec v = P - P_0$ will be a vector on the plane
- $\therefore \vec n \cdot \vec v = 0 \because \vec n$ is perpendicular to $\vec v$
- $A(x - x_0) + B(y - y_0) + C(z - z_0) = 0$
- $Ax+By+Cz = Ax_0 + By_0 + Cz_0 = D$

### Distance from a point to plane

- Any Point on Plane $P_0$, Distance to be determined Point $P_1 = (x_1, y_1, z_1)$ and Point $P_2$ is perpendicularly projected $P_1$ on plane
- Let $\vec a = P_2 - P_1$ & $\vec f = P_0 - P_1$
- point to plane Distance = Distance between $P_1$ & $P_2$ = $\|\vec a\|$

$$\|\vec a\| = \|\vec f\| \cdot  \cos  \theta = (\|\vec n\| \cdot \|\vec f\|  \cos  \theta) / \|\vec n\| = \dfrac {(\vec n \cdot \vec f)} {|\vec n\|}$$
$$\|\vec a\| = \frac {A(x_0 - x_1) + B(y_0 - y_1) + C(z_0 - z_1)} {\sqrt(A^2 + B^2 + C^2)}$$

### Distance between two planes

- Shortest distance = **Perpendicular distance**
- If two Planes **Not parallel** then **distance = 0** since they will intersect at some point
- Distance between parallel planes = **Normalized difference of the $D$**

# Matrix transformations

## Matrices with vectors

Matrix $A_{m * n} \implies \vec v_{1 \to n} \in \Reals^m$

### **Intuition**

> Useful way to represent, manipulate and study linear maps between finite dimensional vector spaces

## Function

- $f(x)=y$ where x is **domain** and y is **co-domain**
- A **Relation** between member of one set with another
- $f: x \mapsto y$ **Mapping** from one set to another
- A Function is not changing a value its just **associating** to another value

## Vector Transformations

- Function that maps a set of vectors to another set.
- can also be denoted using T
- $T(\vec a) = \vec b$ or $T:\vec a \mapsto \vec b$

## Linear Transformations

### Rules

- $T(\vec a + \vec b)= T(\vec a) + T(\vec b)$
- $T(c \cdot \vec a)=c \cdot T(\vec a)$

## Matrix Multiplication

- Applying a transformation to a vector
- Clockwise Rotation Matrix = $\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}$ and $\vec v = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$

$$\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}  \cdot \begin{bmatrix} 1 \\ 2 \end{bmatrix}  = 1 \cdot \begin{bmatrix} 0 \\ 1 \end{bmatrix} + 2 \cdot \begin{bmatrix} -1 \\ 0 \end{bmatrix} = 1 \cdot \begin{bmatrix} -2 \\ 1 \end{bmatrix} $$

- Lets try Two operations Clockwise Rotation and shear
- Rotation $\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}$ and shear $\begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$
- Rotation(shear($\vec v$)) = Rotation_Shear($\vec v$)

$$\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} \cdot \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix} \cdot \begin{bmatrix} 1 \\ 2 \end{bmatrix} = \begin{bmatrix} -1 & -1 \\ 1 & 0 \end{bmatrix} \cdot \begin{bmatrix} 1 \\ 2 \end{bmatrix}$$

$$\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} \cdot \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} -1 \\ 1 \end{bmatrix}$$

$$\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} \cdot \begin{bmatrix} 0 \\ 1 \end{bmatrix} = \begin{bmatrix} -1 \\ 0 \end{bmatrix}$$

- Order matters but it is Associative

### **Intuition**

> we been told the shortcut about row x column but it is actually how $\hat i and \hat j$ get changes when transformed

## Determinant of Matrix

- Determinant of 2D Matrix = Area, 3D Matrix = Volume & so on
- Flipping = -ve determinant
- Determinant $\not = 0 \iff $ Columns of the matrix are linearly independent

$$det \left( \begin{bmatrix} a & b \\ c & d \end{bmatrix} \right) =  \begin{vmatrix} a & b \\ c & d \end{vmatrix} = ad - cb$$

- For $\hat i \& \hat j$ Determinant $ = \begin{vmatrix} 1 & 0 \\ 0 & 1 \end{vmatrix} = 1 \cdot 1 - 0 \cdot 0 = 1$

## Solving with Matrices

### Gaussian elimination

- solves linear equations by reducing them to row echelon form
- operation allowed
- multiply row by constant $-2r_1 \rarr r_1$
- switch rows $r_ 1 \harr r_2$
- add rows $r_1 + r_2 \rarr r_2$
- combination of above $-2r_1 + 3r_2 \rarr r_2$

### Row echelon form

$$\begin{bmatrix} 1 & 0 & 0 & : & x \\ 0 & 1 & 0 & : & y \\ 0 & 0 & 1 & : & z \end{bmatrix}$$

## Matrix Subspaces

### Null space of a matrix

- $N(A)= {A \cdot \vec x = \vec 0 | \vec x \in \Reals^n}$
- Valid subspace - has $\vec o$ & closed under addition & multiplication
- Linearly independent $\implies A * \vec x = \vec 0 \iff \vec x = \vec 0 \therefore N(A) = \vec 0$
- Can be Solved with **Gaussian elimination**

$$\begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \cdot \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$$

- **Nullity** = No. of **non pivot** columns in row echelon form

### Column space of a matrix

- $C(A) = Span(\vec v_1, \vec v_2, \cdots, \vec v_n) $
- Valid subspace - has $\vec o$ & closed under addition & multiplication
- Linearly independent vectors = **Basis** of Column space = No. of pivot entries in row echelon form = **Rank** of a matrix

### **Intuition**

> Its just the span of the vectors in the matrices
