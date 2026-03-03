(ch:differential-forms)=

# Differentials Forms



In the previous chapter, we defined vector field as a map from a smooth function on a manifold $M$ to $\mathbb{R}$.  More specifically, a map $v:\mathbb{C}^\infty(M) \rightarrow \mathbb{C}^\infty(M)$ is expressed on $\mathbb{R}^n$ via a chart $\phi: U \in M \rightarrow \mathbb{R}^n$ as

$$
v(f) = V^\mu(x) \partial_\mu f(x), \quad f \in \mathbb{C}^{\infty}
$$
where as usual we assume $f(x) = f \circ\phi^{-1}(x)$.

In the above expression, the essential part is the components of vector $V^\mu$.  The gradient $\partial_\mu f$ is a mathematical tool to extract $V^\mu$ from the manifold, more specifically from a crosssection of a fiber bundle $TM$.  In fact, for any function $f$,  $v(f)$  produces the same $V^{\mu}$.  A different vector field $w(f)$ produces different components $W^\mu$  even if the same $f$  is used.

In this chapter, we encounter the same directional derivative but our focus is on the gradient $\partial_\mu f$ rather than the components of a vector.  To do so, we introduce a new concept called `1-form` (also known as covector or dual vector.)  It turns out that 1-form is essential in physics.  For example, the electric field is 1-form instead of vector.

We construct other important concepts from the 1-forms, such as `cotangent vector`, `p-forms`, and `exterior derivative`.