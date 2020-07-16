# Image formation

## Geometric primitives

- **Basic building blocks** used to describes 3D shapes

### 2D points

- **pixel coordinates** in an image
- Denoted using a **pair of values**
- $x= (x,y) in RR^2$ or $x = [[x],[y]]$
- **Homogeneous coordinates** $x = (x,y,w) in P^2$ where $P^2 = RR^3 - (0,0,0)$ is **2D projective space**
- **Homogeneous to InHomogeneous** $x = (x,y,w) = w (x,y,1) = w * bar x$ where $bar x$ is **augmented vector**
- $w = 0$ is called **ideal points** or **points at infinity** and do not have an equivalent inhomogeneous
  representation.

## Sources

### Main References

- [Richard Szeliski's Book](http://szeliski.org/Book/drafts/SzeliskiBook_20100903_draft.pdf)

### Side References

- [Wikipedia](https://www.wikipedia.org)
- [Geogebra](https://www.geogebra.org)
