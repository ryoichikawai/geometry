# Continuous functions


## Continuous functions on the Euclidean space

In physics many physical quantities are a real function of position $x$ such as a temperature profile $T(x)$ or a mass density $\rho(x)$.   A real function on the one-dimensional Euclidean space, $f(x)$, is a map from an Euclidean space to  another Euclidean space.  It is expressed as $f: \mathbb{R} \rightarrow \mathbb{R}$.  It may be a bad practice but we  commonly use symbol $\mathbb{R}$ for the Euclidean topological space.  The necessity of the topology becomes clear below.

In the physical world, these functions are expected to be continuous  In a math class, we learned that the function $f(x)$ is continuous at a point $c \in \mathbb{R}$  if  for all $\epsilon > 0$, there exists $\delta > 0$ such that for all $x \in \mathbb{R}$ ,   $|x-c|<\delta$  implies $|f(x)-f(c)| < \epsilon$.   Our task is to extend the concept of continuous function to coordinate free topological spaces where subtraction and absolute value are not available.

Recall that the topology is a collection of open sets and for the Euclidean topology corresponding open sets are the collection of all open intervals.  Can we define continuous functions using open intervals?  If so, we can extend it to general topological space. In fact, the following definition  is equivalent to the above definition. A function $f(x)$ is continuous at  $c \in \mathbb{R}$  if and only if for each interval  $(f (c) − ε, f (c) + ε)$, there exists $δ > 0$ such that $f(x) \in (f(c)-\epsilon, f(c)+\epsilon)$ for all $x \in (c-\delta, c+\delta)$.  

Next we eliminate subtraction in the open intervals. Replace open interval  $(f (c) − ε, f (c) + ε)$ with an open set $U \in \mathbb{R}$ containing $f(c)$ and another open interval $(c-\delta, c+\delta)$ with $V \in \mathbb{R}$ containing $c$.  Then, the above statement is equivalent to the following: A map $f:\mathbb{R} \rightarrow \mathbb{R}$ is continuous at  $c \in \mathbb{R}$  if and only if for each open set $U \in \mathbb {R}$ containing $f(c)$, there exists an open set $V \in \mathbb{R}$ containing $c$ such that $f(V) \subseteq U$.  Since open sets are used in both source and target spaces,  strictly speaking, we need to specify a topology for both source and target.  If the topology is not big enough (recall that we can construct many different topologies), then we cannot construct a continuous function. If we require a topological space to allow continuous functions, the choice of a topology is limited and Euclidean topology is  minimally required to support continuous functions.

We can further simplify the definition.  A map $f:\mathbb{R} \rightarrow \mathbb{R}$ is continuous if for any open set $U \in \mathbb{R}$ the preimage $f^{-1}(U) \subseteq X$ is open where the preimage is defined by 

```{math}
:label: eq:preimage-on-R
f^{-1}(U) =   \{x \in \mathbb{R}: f(x) \in U\} =  [0,\infty)
```

This is amazingly simpler than the original definition based on the $\epsilon-\delta$ method. 

**Examples**

1. Constant function $f(x)=c$ for $x \in \mathbb{R}$.  Intuitively, we know it is continuous. We prove it based on the last definition. WE need to consider two groups of open sets.   If an open set $U$ contains $c$, then $f^{-1}(U) = \mathbb{R}$  which is open.  If an open set $U$ does not include $c$, then $f^{-1}(U) = \emptyset$ which is open as well.  Hence, by definition, the map is continuous.

2. A linear function $f(x) = x$ for $x \in \mathbb{R}$.  Again we intuitively know it continuous.  Since this is identity map, that is $x \rightarrow x$, for any open set $U \in \mathbb{R}$,  $f^{-1}(U) = U$.  Hence the preimage is open. This proves the function is continuous.

3. Consider the Heaviside function
  
   ```{math}
   f(x) = \begin{cases} 0 & \text{if } x < 0 \\ 1 & \text{if } x \ge 0\end{cases}
   ```  
   
   Our intuition says it is discontinuous since there is a jump at $x=0$.

   We consider four open sets:

   * $U$ containing neither 0 nor 1:  $f^{_1}(U) = \emptyset$, which is open.
   * $U$ containing both 0 and 1:  $f^{-1}(U) = (-\infty,\infty)=\mathbb{R}$, which is open
   * $U$ containing 0 but not 1: $f^{-1}(U)=(-\infty,0)$, which is open.
   * $U$ containing 1 but not 0: $f^{-1}(U) = [0,\infty)$, which is NOT open!

    The last case indicates that the function is discontinuous as we expected.  Notice that $[0,\infty)$ is a subset of $\mathbb{R}$ but not in the Euclidean topological space.

4. Consider a similar function

   ```{math}
   f(x) = \begin{cases} 0 & \text{if } x < 0 \\ 1 & \text{if } x > 0\end{cases}
   ```

    Note that the function is not defined at $x=0$. WE exclude any open interval containing $0$ from the Euclidean topology.  Hence, this is not a map from the Euclidean space to $\mathbb{R}$. 
  
    * $U$ containing neither 0 nor 1:  $f^{-1}(U) = \emptyset$, which is open.
    * $U$ containing both 0 and 1:  $f^{-1}(U)=\mathbb{R}\setminus 0$, which is open.
    * $U$ containing 0 but not 1: $f^{-1}(U)=(-\infty,0)$, which is open.
    * $U$ containing 1 but not 0: $f^{-1}(U) = (0,\infty)$, which is open.

    Since the preimage is always open, the map is continuous.  There is no jump at $x=0$ because $x=0$ is not in the topology. 

I hope these examples show you an important role of topology.


## General continuous maps 

We consider a map from one topological space $(X,\mathcal{T}_X)$ to another topological space $(Y,\mathcal{T}_Y)$.  In many literature, in particular in physics literature, a map is defined as $f: X \rightarrow Y$ without specifying topologies.    They are meant to be a map from one topological space to another.  When it is obvious or arbitrary a topology is not specified. In physics, topologies are uniquely fixed by various physical requirements in the most cases.  Physicists often  think it is obvious but only experienced theoreticians can say so.  In this lecture note,  we shall be more careful about the topology we work with.

A map $f: X \rightarrow Y$ means that if $U$ is an open set in $\mathcal{T}_X$, then $f(U)$ is an open set in $\mathcal{T}_Y$.  Simply stating it, if $U \in \mathcal{T_X}$, then $f(U) \in \mathcal{T_Y}$.   The inverse is defined for an open set $V \in \mathcal{T}_Y$,

```{math}
:label: eq:preimage-on-X
f^{-1}(V) = \{p \in \mathcal{T}_X ~|~ f(p) \in V\}
```

where we used a symbol $p$ for a point in in a general topological space$X$. In order to avoid confusion, we use symbol $x$ only for a coordinate point in $\mathbb{R}$ 

$f^{-1}(V)$ is also called preimage of $V$. As we discussed in the previous subsection, if $f^{-1}(V)$ is open, then the map is continuous.  This is a starting point of coordinate free approach.

A real function is a map from a topological space $(X,\mathcal{T})$ to $\mathbb{R}$, which can be considered   as a coordinate free description of a scalar field such as temperature distribution on a non-Euclidean space.

## Smooth maps



### $\mathbb{C}^\infty (\mathcal{M})$ Algebra 

In the algebra of $\mathbb{C}^\infty (\mathcal{M})$, there are three type of operation pointwise addition and multiplication, and multiplication by real numbers. They are They satisfy the following axioms:

```{prf:axiom}
:label: axiom-algebra-smooth-functions

For $f, g, h \in \mathbb{C}^\infty (\mathcal{M})$ and $\alpha, \beta \in \mathbb{R}$,

**Axtioms for addition and multiplication axioms**
|  types  | rules |
| ---: | :---: |
| closure | $f+g \in \mathbb{C}^\infty (\mathcal{M})$ |
| closure | $fg \in \mathbb{C}^\infty (\mathcal{M})$ |
| commutativity | $f + g = g + f$ |
| commutativity | $fg = gf$ |
| associativity | $f + (g+h) = (f+g) + h$ |
| associativity | $f (gh) = (fg) h$ |
| distributivity | $f (g+h) = fg + fh$ |
| distributivity | $(f+g) h = fh + gh$ |


**Axions for multiplication by real numbers**
|  types  | rules |
| ---: | :---: |
| closure | $\alpha f  \in \mathbb{C}^\infty (\mathcal{M})$ 
| identity | $1 f = f$ |
| associativity  | $\alpha (\beta f) = (\alpha \beta) f$ |
| distributivity | $\alpha(f+g) = \alpha g + \alpha h$ |
| distributivity | $(\alpha + \beta) f = \alpha f + \beta f$ |
```

```

```

