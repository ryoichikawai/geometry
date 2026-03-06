# Introduction

How do we mathematically describe physics? Physical quantities can be scalar, vector, or tensor.  They are often functions.  In classical mechanics, a phase space trajectory of particles   $\{q_i(t), p_i(t)\}$ is a function of time $t$.  A potential $V(\bold{x})$ is a scalar field, which is a function of position $\bold{x}$. In electromagnetism, electric field $\bold{E}(\bold{x},t)$ and magnetic filed $\bold{B}(\bold{x},t)$ are functions of spacetime.    A quantum mechanical wave function $\psi(\bold{x},t)$ is a complex scalar field. 

But what are $\bold{x}$ and $t$? Newton told us that they are prefixed and everyone in the universe sees the same $\bold{x}$ and $t$.  Then, the concept of coordinate systems is conveniently developed. Using a set of basis vectors $\{\hat{e}_1, \hat{e}_2, \hat{e}_3\}$, the position is expressed as $\bold{x}=x_1 \hat{e}_1+ x_2 \hat{e}_2 + x_3 \hat{e}_3$, where $\{x_1,x_2,x_3\}$ are coordinates.  The key point is that the basis vectors are the same everywhere in the universe.  Time increases uniformaly at the same rate for everyone. 

Since $x_1, x_2, x_3, t$ all take a value between $-\infty$ and $+\infty$, we write it mathematically $x_1, x_2, x_3, t \in \mathbb{R}$, and all together we live in the four-dimensional space $\mathbb{R}^4$.   It  is also known as 4-dimensional Euclidean space.  (There is a subtle difference between $\mathbb{R}^4$ and the 4-dimensional Euclidean space, which we will discuss later.)

Using the coordinate systems, we are able to define differentiation, smooth functions, vectors, ....., almost all mathematical objects defined in physics are based on the coordinate systems until Einstein said spacetime cannot be written with simple coordinate systems.  Actually, the spacetime changes dynamically according to the theory of general relativity.  There is no universal basis vectors to construct coordinates.

We no longer live in Euclidean space!  We need to construct physics without coordinates (coordinates free theory).   Now without the coordinates,  how can we define vectors and differentials?   It turns out that these are difficult questions even for mathematicians. It took a while for them to come up with new definitions of differentiations, smooth functions and vector fields.  That is the subject of this note.   

We shall discuss calculus on non-Euclidean (curved) space with physics applications in mind. Physical quantities are mathematically expressed with smooth functions, which are continuous and differentiable at any orders.  We are familiar with differentiation on Euclidean space but it is not well defined on curved space.  There is another mathematical object that cannot be directly defined on curved space.  That is vector.  Assigning an arrow to each point on the curved space does not work.

In order to discuss physics on curved space,  we need to define the following mathematical objects

1. Scalar fields
2. Vector fields
3. Vector calculus on scalar and vector fields.

The common approach is based on the concept of local coordinates.  We assume that a small area around a point on a curved space looks like a tiny Euclidean space and usual coordinates are well defined (but only the neighborhood of the point.)  Within the local Euclidean space, usual mathematics such as derivatives are well defined thanks to the local coordinates.  One of the problems is that the local coordinates at one point is different from the local coordinates at another point.  Hence, functions and vectors defined on one local Euclidean space may not be smoothly connected to those defined on another local Euclidean space. Making it sure that scalar fields and vector fields are smooth across the boundaries of the local coordinate systems is the key ingredient of differential manifolds.

```{tip}
Scalar fields and vector fileds must be smooth on curved space.
```

We need to keep it in our mind all time when we read a book on differential manifolds.  We are often lost in a book  because we are overwhelmed by complicated mathematical procedures without their obvious objectives.  In many cases, the book is just trying to make it sure that functions are smooth without telling us.  For the authors,  that is too obvious to mention but the readers are quite confused.  I hope I can fill the gap through this note.