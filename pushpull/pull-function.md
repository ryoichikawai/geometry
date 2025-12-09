(sec:pullback-function)=

# Pullback of Functions

In literature of differential geometry, it is often said that a function on a manifold is "transported" or "transferred" from a manifold to another manifold.  We wonder what it means.

Consider a smooth function $f_M$ on a manifold $M$.  At a point $p$ on $M$, the function produces a real value $f_M(p)$.  Now we consider a function $f_N$ defined on a different manifold $N$. It produces a real value $f_N(q)$ at $q$ on $N$.   We want to make these functions "equivalent" despite that they are on two different  manifolds. But what does "equivalent" mean?  We say they are equivalent if  the following two conditions is satisfied:

1. The two points $p$ and $q$ are connected by a map $\phi: M \rightarrow N$.  That means $q = \phi(p)$.
2. The two functions must produces the same real value if they are evaluated at points $p$ on $M$ and the corresponding point $q=\phi(p)$ on $N$.  That means $f_M(p) = f_N(\phi(p))$.  The right hand side is often expressed as $f_N \circ \phi (p)$.

Then, we say that $f_N$ becomes $f_M$ when it is transported from $N$ to $M$.  We introduce a new symbol $\phi^*$ to express the transport operation as $f_M = \phi^* f_N = f_N \circ \phi$.  Here we are transporting the function from $N$ to $M$ by $\phi^*$.  We say that function $f_N$ is pulled back from $N$ to $M$.    Notice that the direction of the map $\phi$ and the direction of function transport are opposite to each other. Hence the transportation $\phi^*$ is called pullback.  (Note the location of "\*".  We will be using another symbol $\phi_*$ later.  Do not get confused. ) 

You can also transport function from $M$ to $N$ as $f_N(q) = F_M(\phi^{-1}(q)) = F_M \circ \phi^{-1} (q)$.  We used the inverse map $\phi^{-1}$.   That means the function transport from $M$ to $N$ needs inverse map from $N$ to $M$.  Again the direction of function transportation is opposite to the direction of the map $\phi^{-1}$. Let $\eta \equiv \phi^{-1}$ which is a map from $N$ to $M$.  Then, the pullback from $M$ to $N$ is expressed as $f_N = \eta^* f_M$. 

Mathematical objects that are transported in the opposite direction to the direction of a point-to-point map is said to be contravarient.


**Example in the Euclidean manifolds** 

We consider two 2-dimensional Euclidean manifolds $M, N \in \mathbb{R}^2$.   On $N$, a function is defined as $f_N(q) = x y$  where a point is expressed by coordinates $q=(x,y)$.  On $M$, we use polar coordinates $p=(r,\theta)$. The map $\phi:(r,\theta) \rightarrow (x,y)$ is given by the usual coordinate transformation $x(r,\theta) = r \cos\theta$ and $y=r \sin\theta$.  I want to find an equivalent function on $M$. 

```{math}
f_M = \phi^* f_N = f_N \circ \phi = f_N(\phi) =f_N(x(r,\theta), y(r,\theta)) = x(r,\theta) y(r,\theta) = r^2 \cos\theta \sin\theta
```


This is a trivial coordinate transformation and the use of pullback concept is overkill. However, when the manifolds are not Euclidean,  we rely on abstract mathematical procedures.

