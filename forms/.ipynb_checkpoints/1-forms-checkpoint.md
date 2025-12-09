(sec:1-forms)=
# 1-forms

(sec:gradient)=
## Gradient and differential

Gradient of scalar functions is an essential operation in vector calculus.  In the Euclidean space, it is defined as


```{math}
:label: eq:usual-gradient
\nabla f = \partial_x f\, \mathbb{e}_x + \partial_y f\, \mathbb{e}_y + \partial_z f\, \mathbb{e}_z
```


In math or physics course, we learned that the the gradient of scalar function is a "vector" field.  We want to generalize it to curved spaces or general manifolds.  After deep thought, mathematicians and theoretical physicists reached a conclusion that the gradient is not a vector field but something else.  You will see why it is not a vector when we investigate the properties of various physical quantities in later chapters.

For a smooth function $f$ on manifold $M$, mathematicians introduced a map $df: \text{Vect}(M) \rightarrow \mathbb{C}^\infty (M)$.  This expression is a bit confusing.  You can think of $d$ as an operator acting on $f$ and then $d$ and $f$  jointly form a map $df$.  The map takes a vector field $v \in \text{Vect}(M)$ and outputs a  smooth function $v(f)$:


```{math}
:label: eq:differential-on-manifold
df(v) = v(f)
```


which means that $df(v)$ and $v(f)$ outputs the same function.  Then, why do we need two maps?  While the vector field takes a function as an input, $df$ takes a vector field as an input.  In other words, in $v(f)$, $v$ is specifically given and $f$ is a "variable" and In $df$, $f$ is specifically given and $v$ is a "variable".  You will have a better  understanding by working on a chart. See {numref}`sec:differential-on-a-chart`.

In order to guarantee that the gradient does not depend on the choice of a vector field, we require that $df$ satisfies  te following linearity conditions:   for $v, w \in \text{Vect}(M)$ and $g \in \mathbb{C}^\infty(M)$ 

```{math}
:label: eq:differential-linearity
df(v+w) = df(v) + df(w), \qquad df(gv) = g df(v).
```

Do not get confused with the addition of two differentials  There is only one differential $df$ in the above relations.  

$df$ is called the `differential` of $f$, or the `exterior derivative` of $f$.  It is an example of `1-form` which we introduce below.

(sec:differential-on-a-chart)=
## Differential on a chart

Working on a chart provides with a better understanding of the differential. Evaluate it on $\mathbb{R}^n$ through a chart $\phi: U \in M \rightarrow \mathbb{R}^n$,    the differential is expressed as


```{math}
:label: eq:differential-on-chart
df(v) = v(f) = v^\mu(x) \partial_\mu f(x)
```


This is nothing but a directional derivative.  Are $v(f)$  and $df(v)$ the same thing?  They are not.  The vector field $v(f)$ tries to find the coordinate expression of the vector field $v_\mu(x)$.  Any function can be  used and $v^\mu(x)$ is independent from the choice of $f$.  On the other hand,  $df(v)$ tries to evaluate the gradient of a given function $f$ with help of a vector field $v^\mu(x)$.  Any vector field can be used and the gradient is independent of  a choice of vector field $v$.

The linearity conditions guarantees it.


```{math}
:label: eq:differential-linearity1
df(v+w) = (v+w)^\mu (\partial_\mu f)_{v+w} = (v^\mu + w^\mu) (\partial_\mu f)_{v+w}
```


where $(\partial_\mu f)_{v+w}$ indicates the gradient is evaluated with $v+w$.

```{math}
:label: eq:differential-linearity2
df(v)+df(w) = v^\mu (\partial_\mu f)_v + w^\mu (\partial_\mu f)_w
```


Since we can chose any $v$ and $w$, we conclude  that $(\partial_\mu f)_{v+w} = (\partial_\mu f)_v = (\partial_\mu f)_w$, indicating that the gradient does not depend on the choice of a vector field.

Working on a chart,  the above definition of $df$  agrees with the total differential of function,

```{math}
:label: eq:total-differential
df = \partial_\mu f dx^\mu
```

which we learned in a calculus curse.


````{prf:proof}

The differential  of $x^\mu$ is calculated as

```{math}
d x^\mu (v)  = v(x^\mu) = v^\nu \partial_\nu x^\mu = v^\nu \delta^\mu_\nu = v^\mu
```

Substituting it to the differential of $f$,

```{math}
d x^\mu (v)  = v(x^\mu) = v^\nu \partial_\nu x^\mu = v^\nu \delta^\mu_\nu = v^\mu
```
Since this equality holds for any $v$, we obtain {eq}`eq:total-differential`

````

It is natural to call $df$ on $M$ the differential of $f$.

Recall that $\partial_\nu$ is a basis of vector fields in $\mathbb{R}^n$.  That means $\partial_\nu$ is a vector filed and can be fed to the differential.

```{math}
:label: eq:omega-v-orthogonality
dx ^\mu(\partial_\nu) = \partial_\nu(x^\mu) = \delta^\mu_\nu
```

How can we find the partial derivative $\partial_\mu f$?   In the directional derivative, the vector field $v$ specifies the direction of the derivative.  If we want to know the derivative along a coordinate axis, the direction can be specified with a basis vector $\partial_\mu$.  So feed the vector field $v = \partial_\mu$ to the differential

```{math}
:label: eq:partial-derivative
df(\partial_\mu) = \partial_\mu f
```

Now, we are sure that $df$ generates the gradient of $f$.

(sec:1-form)=
## 1-forms

We generalize the above idea.  Consider a map $\omega: \text{Vect}(M) \rightarrow \mathbb{C}^\infty(M)$ such that for $v, w \in \text{Vect}(M)$ and $g \in \mathbb{C}^\infty(M)$

```{math}
:label: eq:1-form-linearity
\omega(v+w) = \omega(v) + \omega(w), \qquad \omega(gv) = g \omega(v)
```

We call $\omega$ a `1-form` and the set of all 1-forms on $M$ is denoted as $\Omega^1(M)$. The differential $df$ is clearly a 1-form.   The addition and scalar multiplication can be defined for $\omega, \mu \in \Omega^1(M)$, $v, w \in \text{Vect}(M)$ and $g \in \mathbb{C}^\infty$,

```{math}
:label: eq:1-form-addition
(\omega + \mu) (v) = \omega(v) + \mu(v), \qquad (g\omega)(v) = g \omega(v)
```

Since the addition and the scalar multiplication obey the axioms of vector, 1-forms behave like vectors.  Because of this,  some people call 1-form `covector` or `dual vector`.  Although 1-forms are indeed dual to vector fields, they have some distinct properties different from vector fields do not have.  Therefore, we shall call them 1-forms.

Notice that no function $f$ is used to define the 1-form.  Hence, $\omega$ does not look like a gradient anymore.  However, it is just a generalization of gradient.  Recall that the vector field is originally defined as $v(f) = V^\mu \partial_\mu f$ but we simply write the field as $v = V^\mu \partial_\mu$ without $f$.  Then we interpreted $\partial_\mu$ as the basis of the vector field.  It does make a sense since a vector field should not depend on $f$.  We are trying to do the same for 1-form.  You can think that we are trying to find a gradient operator like $\nabla$ on $M$.  When it acts on $f$, you get a gradient.

By analogy from {eq}`eq:partial-derivative`,  we define a component of 1-form by 

```{math}
:label: eq:1-form-component
\omega_\mu = \omega(\partial_\mu).
```

and based on {eq}`eq:total-differential`, 

```{math}
:label: eq:1-form-decomposition
\omega = \omega_\mu dx^\mu.
```

If $\omega = df$, then we recover {eq}`eq:total-differential` and {eq}`eq:partial-derivative`.   Equation {eq}`eq:1-form-decomposition` suggests that $\{ dx^\mu\}$ is a basis set spanning of 1-forms on $\mathbb{R}^n$ much like $\partial_\mu$ forms a basis set for vector fields.  Again, 1-forms look like vectors.
