(sec:vectors-in-euclidean-spaces)=
# Vectors in the Euclidean spaces

The old concepts of vectors and vector fields defined in the Euclidean space $\mathbb{R}^3$ are briefly reviewed in this section. We are already familiar with since high school.  

##  What are vectors?

In freshman physics courses, a vector $\vec{v}$  in the 3-dimensional Euclidean space is introduced as $\vec{v}=v_x \vec{i} + v_y \vec{j} + v_z \vec{k}$ where $\vec{i}$, $\vec{j}$, $\vec{k}$  are basis vectors.  It is often written as a set of three numbers like $(v_x, v_y,v_z)$.  This expression is confusing since any set of three numbers look like a vector.  In a linear algebra course, we are told that a vector is an element of a vector space $\mathcal{V}$ which satisfy {prf:ref}`axiom:vector-space`.

```{prf:axiom}
:label: axiom:vector-space

A set $\mathcal{V}$ is a vector space if the following axioms are all satisfied for $\vec{u}, \vec{v}, \vec{w} \in \mathcal{V}$ and $a, b$  a field of scalar $\mathcal{F}$.

**addition axims**

1. closure:  $\vec{u}+\vec{v} \in \mathcal{V}$
2. comutativity: $\vec{u} + \vec{v} = \vec{v} + \vec{u}$
3. Associativity: $(\vec{u}+\vec{v}) + \vec{w} = \vec{u} + (\vec{v}+\vec{w})$
4. Additive identity:  There exists a zero vector $\mathbb{0}$ such that $\vec{u}+\mathbb{0} = \mathbb{0}+\vec{u} = \vec{u}$.
5. Additive inverse:  For every $\vec{u}$, there exist a vector $-\vec{u}$ such that $\vec{u} + )-\vec{u}) = \mathbb{0}$.

**scallar multiprication axioms**

1. Closure: $a \vec{u} \in \mathcal{V}$
2. Vector distributivity: $a (\vec{u}+\vec{v}) = a \vec{u} + a \vec{v}$
3. Scalar distributivity: $(a+b) \vec{u} = a \vec{u} + b \vec{u}$
4. Associativity: $(ab) \vec{u} = a (b \vec{u})$

Elements of $\mathcal{V}$ are called vector.
```
Addition and scalar multiplication used in the axiom are not defined in arbitrary topological spaces.  Thus, we need a different definition.

## What are vector fields?


For $n$-dimensional space $\mathbb{R}^n$, a vector field assigns a vector at each point $x \in \mathbb{R}^n$.  The vector at each point is an element of the vector space defined in {prf:ref}`axiom:vector-space`.

In modern physics, vector fields are defined  with coordinate transformations.  

```{prf:definition}
:label: vector-field-by-transformation

For a field $V(x)=\{V_1(x),V_2(x),V_3(x)\} \in \mathbb{R}^3$ where $x=\{x_1,x_2,x_3\} \in \mathbb{R}^3$ is coordiantes. The field $V(x)$ is a vector field if when the coordiates are transformed to new coordinates $x^\prime = \{x^\prime_1,x^\prime_2,x^\prime_3\}$, the field is transformed as

$$
V^\prime_i(x^\prime) = \sum_{i=1}^{3} \frac{\partial x^\prime_i}{\partial x_j} V_j(x)
$$
```

This definition ensures that a vector field is independent of a choice of the coordinate axes.  A scalar field is invariant under the  coordinate transformation.  Hence, the vector field and scalar filed are clearly distinguished by this definition.  

While the above definition of vector fields is very successful in physics, it works only when standard coordinates can be defined. We need a new definition suitable for arbitrary  topological spaces without coordinates.

