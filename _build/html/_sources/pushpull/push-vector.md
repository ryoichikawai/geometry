(sec:pushforward-vector)=

# Pushforward of tangent vectors

We now try  to transport or transfer tangent vectors from one manifold to another.  First, we need to define  when a vector on a manifold is equivalent to a vector on another manifold.

Consider a tangent vector at $p$ on a manifold $M$ which is denoted as $v_M \in T_p M$ and a tangent vector at $q$ on a different manifold $N$ denoted $v_N \in T_q N$.  When can we say that the two tangent vectors are equivalent?  To answer the question, we need to go back to the definition of vector.  The vector is a map $v_M: \mathbb{C}^\infty(M) \rightarrow \mathbb{C}^\infty(M)$.  That means a vector takes a function and returns another function.  WE write is as $v_M(f_M)$ and similarly $v_N(f_N)$.  To evaluate its value, we need a pint and a function on the manifold. To shows the equivalence of the two vectors, we need to have equivalent points and equivalent functions.

1. The two points $p$ and $q$ are connected by a map $\phi: M \rightarrow N$.  That means $q = \phi(p)$.
2. The two functions $f_M$ and $f_N$ are connected by pullback as $f_M = \phi^* f_N$.
3. The two vectors $v_M(f_M)$ and $v_N(f_N)$ have the same value when the points are functions are connected as described above.  This means $v_N(f_N) = v_M (\phi^*f_N)$.

The last equality suggests that we are able to  express $v_N$ in terms of $v_M$, indicating that we transported the vector from $M$ to $N$.  Notice that the direction of transportation is the same as the direction of the map $\phi$.  That means it is opposite to the direction of function transport.  We say that the vector is pushed forward from $M$ to $N$. To express it mathematically, we introduce a symbol $\phi_*$ as 


$$
v_N (f_N) = \phi_* v_M (f_N) = v_M (\phi^*f_N)
$$


The transportation by $\phi_*$ is called pushforward. (Notice the location of "\*".)  Any mathematical object that are transported by pushforward is said to be covariant.



We can see the details of the transportation by going back to the directional derivative or derivation of curves.



We use the same map $\phi$ from $M$ to $N$.  Suppose that we have a tangent vector $v_M \in T_pM$.  We want to find the same tangent vector on $N$, that is $v_N \in T_q N$ where $q=\phi(p)$.  The "same" tangent vector means that $v_M$ and $v_N$ have the same components $v^\mu$.  More specifically, for functions $f_M \in \mathbb{C}^\infty(M)$ and $f_N \in \mathbb{C}^\infty(N)$, we want to make the following two tangent vectors equivalent.
$$
v_M(f_M) = v^\mu \partial_\mu f_M\Bigg|_p, \qquad v_N(f_N) = v^\mu \partial_\mu f_N \Bigg|_q
$$

Notice that both tangent vectors have the same component $v^\mu$.    The difference between two tangent vectors is the functions.   In other words, we need to transfer the function.  We learn that functions can be only pulled back.  So, $f_M = \phi^* f_N$.  Then, we have $v_N(f_N) = v_M(\phi^* f_N)$ .  Then, we say that $v_M$ is transfered from $M$ to $N$.  This operation is called pushforward and expressed with symbol $\phi_*$ (pay attention to the location of "\*") as

$$
\phi_* v_M (f_N) = v_M(\phi^* f_N)
$$

The left hand side states that the tangent vector $v$ on $M$ is pushed forward to $N$ and acts on function $f$ on $N$.  The right hand side tells that the tangent vector $v$ on $M$ acts on a function pulled back from $N$.  The two sides is doing exactly describing the same  tangent vector since they produces the same components. 

The pushforward operation can be obtained directly by calculating the derivative of a parametric curve. COnsider a curve $\gamma(t)$ on $M$.   Its derivative $\frac{d}{dt}\gamma(t)$ is a tangent vector.  The corresponding curve on $N$ is $\phi \circ \gamma (t)$ and thus the corresponding tangent vector is $\frac{d}{dt} \phi \circ \gamma(t)$.  We shall express it as  $\phi_* \frac{d}{dt} \gamma(t) \equiv \frac{d}{dt} \phi \circ \gamma(t)$, which is   pushforward of the tangent vector. It just tells that moving the tangent vector from $M$ to $N$ is done by mapping the curve from $M$ to $N$ using $\phi$.

In summary, to transfer a tangent vector from one manifold $M$ to another $N$, we must transfer the curve from $M$ to $N$.  Hence, the direction of tangent vector transfer is the same as the direction of map $\phi$.  WHen an object is transfered in the same direction as the map is said to be covariant.

