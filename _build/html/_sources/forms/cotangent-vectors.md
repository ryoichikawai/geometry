(sec:cotangent-vectors)=

# Cotangent Vectors

## Cotangent vectors

In {numref}`sec:def-vector-fields` we define vector fields and in {numref}`sec:tangent-vectors`, tangent vectors at a particular point $p$.   Similarly, we define a 1-form evaluated at a point $p$ as

```{math}
:label: eq:cotangent-vector
\omega_p(v_p) = \omega(v)(p)
```

where $v$ is a vector field and $v_p$ is a tangent vector at $p$.  $\omega_p$ is called cotangent vector and the set of all cotangent vectors at $p$ form a cotangent vector space $T^*_p M$.

Notice that the output of $\omega_p$ is just a number in $\mathbb{R}$.  While a 1-form is a map $\omega : \text{Vect(M)} \rightarrow \mathbb{C}^\infty(M)$, $\omega_p$ is a map a tanngent vector to a real number, that is $\omega_p: T_p M \rightarrow \mathbb{R}$.


As an example, consider a differential $df$ which is a 1-form.  On a chart $\phi: U \subseteq M \quad \\mathcal{R}$, the point $p$ is mapped to a corresponding point $x_p = \phi(p)$ on $\mathbb{R}$.  Then, $df$ at $p$ is evaluated on the chart as

```{math}
:label: eq:cotangent-vector-on-a-chart
df_p = v^\mu_p \partial_\mu f\Big|_{x_p}
```

which is a directional derivative evaluated at $x_p$ in the direction of the tangent vector $v_p$.  It is clear that $df_p$ is just a number.  The number indicates a "slope"  of the function $f$ in the direction of the tangent vector.

We we define 1-forms, we say that 1-form is not a vector.  But here we are saying that a 1-form evaluated at a point is a vector.  We saw a similar relation between vector fields and tangent vectors. Where as the output of a 1-form is a smooth function, the output of cotangent vectors are numbers which satisfies the axioms of vector {prf:ref}`axiom:vector-space`.  Therefore, cotangent vectors are genuine vectors.