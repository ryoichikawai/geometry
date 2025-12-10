(ch:pullback-pushforward=)

# Covariant vs Contravariant

Whenever we want to calculate something on a manifold $M$, we move to a Euclidean geometry $\mathbb{R}^n$ with a chart and carry out the calculation there. However, the result is valid only small area on the Manifold.  Recall that a a chart is a map from an open subset $U \subseteq M$ to $\mathbb{R}^n$ where $U$ is a neighborhood of a point $p$ on $M$.  Hence the result is valid only inside of $U$.  When we move to another part of $M$, we have a different chart and 


To do so, we move mathematical objects such as functions and vectors from the manifold to $\mathbb{R}^n$.  We also want to take the results back from $\mathbb{R}^n$ to the manifold.  It turns out that there are two types of back-and-forth movements `pushforward` and `pullback`.  Mathematical objects that are transferred by the pushforward is said to be `covariant` and those by pullback is `contravariant`.  

The ability to copy back the results obtain on $\mathbb{R}^n$ to the manifold is essential to establish continuity and smoothness of mathematical objects through out the manifold.

One of the main reason with general manifolds is the lack of coordinates.  That is why we need a chart $\phi$ from a point $p$ in $M$ to $x$ $\mathbb{R}^n$.  Using the Cartesian coordinates the destination of a chart is expressed with coordinates $x = x^\mu$.  In turn, we can use the inverse of the chart to assign coordinates $x^\mu$ to the point $p = \phi^{-1}(x)$. Recall that a chart is bijective.  There is always a point on $M$ that corresponds to $x$ on $\mathbb{R}^n$.) In other words, $p$ is expressed with the same values $x^\mu$ as the coordinates on $\mathbb{R}^n$.   $x^\mu$ used in $M$ is called local coordinates on $M$.  More precisely, since a chart is a map from a open subset $U \subseteq M$ to $\mathbb{R}^n$, we have local coordinates $x^\mu$ only inside $U$.  The manifold is completely covered by an atlas, that is a collection of open sets $\{U_\alpha\}$.  Each open set $U_]\alpha$ has its own local coordinates copied from the corresponding $\mathbb{R}^n$ using a chart.

When we deal with curved space,  we often move from one manifold to another manifold.  Then, we often look at the same mathematical object from different manifolds.   For example, consider a two manifolds $M$ and $N$. A map $\phi: M \rightarrow N$ connects point $p$  on $M$ to $q$ on $N$.  The direction of the map is important here.  Then, we ask how a function $f$, a tangent vector $v_p \in T_pM$,  and cotangent vector $\omega_p \in T^*_p M$ on $M$ look like on $N$, and vice versa.

Some objects can be transported in the same direction as $\phi$ but not in the other way.  Others can be transported only in the backward direction with respect to the map $\phi$.  The former transportation is called `pushforward` and the latter is known as `pullback`.  When objects are transported by pushforward, they are said to be `covariant` and those by pullback are `contravariant`. 

In the following sections, we will find that tangent vectors are covariant, and  functions and cotangent vectors are contravariant.





_Explain why these properties are important_

