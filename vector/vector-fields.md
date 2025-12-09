(sec:def-vector-fields)=
# Vector fields in general manifolds

Vectors in the Euclidean spaces are defined with coordinates.  In fact, neither direction nor magnitude can be defined without usual coordinate systems with the Euclidean metric.  Mathematicians were struggling to develop a definition of vector fields in general manifolds.  The final formalization  was completed about 80 years ago and universally accepted during 1960s.  Since then, there have been no major change.  Theoretical physicists have quickly adopted it.

Unfortunately, the general definition of vector fields is very abstract and it is difficult to connect it to physics until we learn advanced physics such as the Einstein's general theory of relativity and quantum field theory.  On the other hand, without the mathematical tools for curved spaces, it would be difficult to learn such physics.  We ave a chicken and egg situation.
In this section, we introduce the formal definition and try to understand it.

On a manifold $M$, a vector field $v$ is a map from $\mathbb{C}^\infty(M)$  to $\mathbb{C}^\infty(M)$.  That means the vector field $v$ takes a smooth function $f \in \mathbb{C}^\infty(M)$ as an input.  The output $v(f)$ is also a smooth function.  Recall that a function $f$ on $M$ is a map $f : M \rightarrow \mathbb{R}$.  That means $f$ take a point $p$ on $M$ and outputs a real number.  In words, $f$ is a real scalar field.  We can say that a vector field takes a scalar field and outputs a scalar field.  How come such a map is a vector field.  It is totally different from the vector field we  know of.  Does it have components like a vector in the Euclidean space?  Yes, it does but we cannot see it on the manifold since the components need coordinates. The connection between the abstract definition and actual components can be established through a chart.  We will do it later.

Not every map from $\mathbb{C}^\infty(M)$  to $\mathbb{C}^\infty(M)$ is a vector field.  WE need additional requirement.  Recall that functions in $\mathbb{C}^\infty(M)$ follows the algebra defined in {prf:ref}`axiom-algebra-smooth-functions`.  Vector fields must be consistent with the algebra, that means we must define how vector fields act on addition $f+g$, multiplication $fg$, and multiplication by real numbers $\alpha f$.

```{prf:definition}
:label: def-vector-field

A map $v: \mathbb{C}^\infty(\mathcal{M}) \rightarrow \mathbb{C}^\infty(\mathcal{M})$ is a vector field if the following properties are satisfied:

* $v(f+g) = v(f) + v(g)$
* $v(\alpha f) = \alpha v(f)$
* $v(fg) = v(f) g + f v(g)$
```

The three linearity conditions and Leibniz law make the map a vector field.  The linearity  essentially says that the vector field $v$ does not depend on the choice of the function $f$.  $v(f)$ and $v(g)$ represent the same vector field.  We will come back to this issue  later.

There must be addition and scalar multiplication. 

````{prf:definition} Addition and scalar multiplication of vector fields
:label: def-addition-scalar-muliplication
Let  $\mathcal{V}(M)$ denotes the set of all vector fields on $M$.
For $v, w \in \mathcal{V}$  and $f, g \in \mathbb{C}^\infty(M)$, addition and scalar multiplication are defined as follows:

**addition**

```{math}
:label: eq:vector-field-addition
(v+w)(f) = v(f) + w(f)
```

**scalar multiplication**

```{math}
:label: eq:vector-field-scalar-nultiple
(gv)(f) = g v(f)
```

````

Note that $v(f)$ and $w(f)$ are acting on the same function but they are different vector fields. 
Now, we can show that the vector fields defined above satify the axioms of vectors.

The output of $v(f)$ is a function in the same manifold as the input.  Hence, $v(f)$ follows the same algebra given in {prf:ref}`axiom-algebra-smooth-functions`.  Using it, the addition and the scalar multiplication satisfy the axiom of vectors given in {prf:ref}`axiom:vector-space`.


## Expressions of vector fields on a chart

We have just defined vector fields on manifolds but we don't know how to evaluate it.   Since we practically know calculus only on the Euclidean space, we must cast the vector field $v(f)$ on a Euclidean space through a chart.

### Definition

```{prf:definition}
:label: def-vector-field-as-derivation

Consider a chart $\phi: U \subseteq M \rightarrow \mathbb{R}^n$. The vector field is expressed with the local coordinates as follows:

```{math}
:label: eq:vector-field-on-chart
v(f) = v^\mu(x) \partial_\mu f(x)
```

where $x$ is a local coordinate and $v^\mu(x)$ is a component of the vector field.
(Note that the Einstein's summation convention is used)


### Uniqueness of the components

The right hand side of the above definition is nothing but a directional derivative in the direction of the vector field.  This definition looks a bit strange.  The resulting function depends on the choice of function $f$ and thus the components seems also depends on $f$.  However, the components are independent from $f$.  For any smooth function, we will get the same components as long as the same map $v$ is used.  This is guaranteed by the linearity condition $v(f+g) = v(f)+v(g)$.  Suppose that the components depend on the function, the left hand side of the linearity condition is

```{math}
:label: eq:vctor-field-linearity-on-chart1
v(f+g) = v^\mu_{f+g} \partial_\mu (f+g) =  v^\mu_{f+g} \partial_\mu f + v^\mu_{f+g} \partial_\mu g
```
but the right hand side is

```{math}
:label: eq:vctor-field-linearity-on-chart2
v(f)+v(g) = v^\mu_f \partial_\mu f + v^\mu_g \partial_\mu g
```

In order to satisfy the linearity for any $f$ ad $g$,  the necessary condition is $v^\mu_{f+g} = v^\mu_f = v^\mu_g$ , which can be satisfied if and only if $v^\mu$ does not depend on functions.  Now it is clear that $v(f)$ and $v(g)$ are the same vector fields since they share the same components.

### Zero vector

In order to satisfy the axioms of vectors, the zero vector must exist.  For constant function $f=c$, we have  $v(f) = 0$.  Is this the zero vector?  It is not!   This just says that the output function of $v$ happens to be constant zero.  The zero vector is defined as a vector field whose  components are all zero for any function $f$.  We can write is as $0(f) = 0, \quad \forall f \in \mathbb{C}^\infty(\mathbb{R})$ .

### Basis vectors

In the above definition of vector fields, the choice of a function $f$ is not important. Then, the vector field can be written  without $f$ as $v = \sum_\mu V^\mu(x) \partial_\mu$ which is an operator that acts on functions.   Comparing it with a regular expression of vector $V^\mu \hat{e}_\mu$ where $\hat{e}_\mu$ basis vectors,  $\partial_\mu$ is playing a role of a basis vector.   Formally, we consider $\partial_\mu$ as a basis of vector field.

