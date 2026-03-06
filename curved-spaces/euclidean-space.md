# Euclidean Space




Euclidean space of $n$ dimensions ($\mathbb{R}^n$)  is defined as a set of all possible ordered $n$-tuples of real numbers, equipped with two specific operations: vector addition and scalar multiplication. In addition, the space must also have an inner product (dot product), which defines the geometry.

1. **Set**:   
  For any positive integer, the space consists of points $\bold{x} = (x_1,x_2,\cdots,x_n)$, where each $x_i$ is a real number.  The $n$-tuple $\bold{x}$ is called vector (see the remark below)..

2. **Vector addition**:  
  For two vectors $\bold{x} = (x_1,x_2,\cdots,x_n)$ and $\bold{y} = (y_1,y_2,\cdots,y_n)$, the addition is defined as  

  $$
  \bold{x}+ \bold{y} = (x_1+y_1,x_2+y_2, \cdots, x_n+y_n)
  $$



3. **Scalar multiplication**:  
  For a vetor $\bold{x}$ and a real number $\lambda$, the scalar multiplication is defined by
  $$
  \lambda \bold{x} = (\lambda x_1, \lambda x_2,  \cdots, \lambda x_n)
  $$


4. **Inner Product**:
  For two vectors $\bold{x} = (x_1,x_2,\cdots,x_n)$ and $\bold{y} = (y_1,y_2,\cdots,y_n)$, the inner product  is defined by 

  $$
  \bold{x}\cdot\bold{y} = x_1 y_1 + x_2 y_2 + \cdots x_n y_n = \sum_i x_i  y_i
  $$


5. **Metric (Distance)**:
  The distance   between two points $\bold{x} = (x_1,x_2,\cdots,x_n)$ and $\bold{y} = (y_1,y_2,\cdots,y_n)$, is given by

  $$
  d(\bold{x},\bold{y}) = \|\bold{x}-\bold{y}\| = \sqrt{\sum_i^n (x_i-y_i)^2}
  $$

Stating it simply,  the  Euclidean space of $n$ dimensions is the collection of all $n$-component vectors for which the operations of vector addition and multiplication by a scalar are permissible. Moreover, for any two vectors in the space, there is a non-negative number, called the Euclidean distance between the two vectors.


_Remarks:_

1. We just called the tuple vector. Is this the same kind of vector that we use in physics?  No!  For mathematicians, tuples are vector. You can draw an arrow from the coordinate origin $(0,0,\cdots,0)$ to $(x_1,x_2,\cdots,x_n)$.  Then, it is a position vector we are familiar with.  So, The origin of vectors based on tuples is fixed at  $(0,0,\cdots,0)$.   For physicists, $x_i$ are coordinates.  Let us introduce basis vectors $\mathbb{e}_1, \mathbb{e}_2, \cdots,\mathbb{e}_n$.  Then, $\bold{x}=x_1 \mathbb{e}_1 + x_2 \mathbb{e}_2 + \cdots x_n \mathbb{e}_n$, which makes a sense for us.  However, we need to define the orthonormal basis vectors.   They are just tuples such as $\mathbb{e}_1 = (1, 0,\cdots,0)$.  At the end, we go back to the original tuple. On the other hand, in physics a vector has magnitude and direction.  The origin of a vector can be anywhere in the space.  However, it must satisfy a specific transformation law. If you rotate your coordinate axes, the components of a physical vector must change in a specific way to ensure the direction still points in the same physical direction. We will define physical vectors later.

2. There is a way to avoid the use of the fixed origin.  A rigorous definition of Euclidean space as an 

   affine space, which decouples the "points" from the "vectors," treating the space as a collection of locations where no single point is inherently the center (the origin).  Consider a space $\mathcal{E}$ and a inner product vector space $\mathcal{V}$.   The space $\mathcal{E}$ is Euclidean if a map $f: \mathcal{E} \times \mathcal{E} \rightarrow \mathcal{V}$ satisifies the following conditions:

   1. For $p \in \mathcal{E}$ and $v \in \mathcal{V}$, there exits a unique point $q \in \mathcal{E}$ such that $\vec{qp}$ where $\vec{qp}$ is an arrow from $q$ to $p$.
   2. For $p, q, r \in \mathcal{E}$, the vectors satisfy $\vec{pq} + \vec{qr} = \vec{pr}$.
   3. The distance between $p,q \in\mathcal{E}$ is defined by $\|\vec{qp}\|=\sqrt{\vec{qp}\cdot\vec{qp}}$  
   
   This definition does not use the tuple.  There is no special point in the space. We can place a vector anywhere. However, we must define an appropriate inner product without using the tuple.  An inner product is a map $\langle \cdot,\cdot\rangle: \mathcal{V} \times \mathcal{V} \rightarrow \mathbb{R}$ defined by the following axioms.  For $u,v,w \in \mathcal{V}$,
   
   1. **Symmetry**: $\langle u, v \rangle = \langle v,u \rangle$.
   2. **Linearity:** $\langle a u + b v, w \rangle = a \langle u,w \rangle + b \langle v, w \rangle$
   3. **Positive Definiteness:** $\langle u, u \rangle \ge 0$ and $\langle u, u \rangle = 0$ if and only if $v = \bold{0}$. 

Using these axioms, we define the geometry of Euclidean space:

1. **Length (Norm):**  $\|v\| = \sqrt{\langle u,u\rangle}$.

   2.  **Angle:** $\cos(\theta) = \displaystyle\frac{\langle u,v \rangle}{\|u\| \|v\|}$

   3. **Orthogonality:**  $u$ and $v$ are orthogonal if $\langle u, v \rangle = 0$

   Using these definitions, we can construct basis vectors with which tuples (coordiates) are defined.




## Euclidean geometry

Inside the Euclidean space, we can construct a two dimensional subspace or a plane.  For two vectors $\bold{x}$ and $\bold{y}$,  we can construct vectors $\bold{q} = a \bold{x}+b\bold{y}$ where $a$ amd $b$ are real numbers. Expressing it as 2-tuple $(a,b)$,  $\bold{q}$ can be considered as 2-dimentional vector.  The subspace consisting of all $(a,b)$ forms a plane.  On any such a Euclidean plane, the following axioms hold.

1. A straight line can be drawn between any two points.
2. Any straight line segment can be extended indefinitely in a straight line.
3. A circle can be drawn with any center point and any radius.
4. All right angles are equal to one another.
5. Given a line and a point not on that line, there is exactly one line through that point that is parallel to the first line.

All other geometric properties can be derived from the above axioms.  For example,

1. The interior angles of any triangle always sum to exactly $2 \pi$.
2. The shortest distance between two points is a unique straight line.
3. Parallel lines stay the same distance apart and never intersect


On non-Euclidean spaces the axioms not necessarily hold  and thus the above geometric properties may not be true. On curved space, parallel lines can cross each other.  The sum of  interior angles of a triangle can be larger or smaller than $2\pi$.
