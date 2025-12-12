#  Topology and open sets

In this section, mathematical concepts, _topology_ and _open sets_ are introduced.  We begin with open intervals, which we are already familiar with.  In the following subsection, we extend the concepts to abstract spaces and redefine open sets without invoking coordinates.   At the end, we come back to $\mathbb{R}$ and demonstrate that the new definitions are consistent with old ones.

## Open intervals in $\mathbb{R}$
The concept  of open sets plays a key role in mathematics and so does in physics.  An example is  open interval $(a,b)$ in real number $\mathbb{R}$, which is a set of all real number between two given end points $a$ and $b$, but not including the endpoints themselves.  It formally defined as

```{prf:definition}
:label: open-interval

$$
(a,b) =\{x \in \mathbb{R}~|~ a < x < b\}
$$

where $a, b \in \mathbb{R}$ and $ a < b$.
```
_Neighborhood_ is a mathematical concept closely related to the concept of open sets. 

```{prf:definition}
:label: neighborhood-as-interval-in-R

A set $𝑁 \subseteq \mathbb{R}$ is called a neighborhood of $x \in \mathbb{R}$ if there exists a real number $\epsilon > 0$ such that

$$
(x-\epsilon, x+\epsilon) \subseteq N
$$
```
Knowing the definition of open intervals and neighborhood, we can describe open sets with the neighborhoods.

```{prf:proposition}
:label: open-interval-in-R-by-neighborhood

An interval $(a,b) \in \mathbb{R}$ is open if and only if for each $x \in (a,b)$, the neighborhood of $x$ is completely inside the interval $(a,b)$.

```
In summary, we define open interval first.  Then, we define neighborhoods using the open interval.  At the end, we showed the relation between open interval and neighborhood.  This logical steps are important when we extend these mathematical concepts beyond $\mathbb{R}$.

There is another approach in which we define neighborhoods first. Then, open interval is defined with neighborhoods. We call it the neighborhood-first-approach and the previous approach the open-set-first approach.  In physics, the open-set-first approach is much more popular than the other and we as physicists follow this tradition.  When we read literature, in particular math books, we must be careful about these two approaches.  When you mix  them, you can be trapped in circular arguments.  For example, you will find the following definitions in literature.

* A set $U$ is open if every point in $U$ has a neighborhood contained in $U$.
* A set $N$ is a neighborhood of $x \in X$ if it contains an open set $U$ such that $U$ contains $x$.

The first statement defines open sets using neighborhoods. The second statement defines neighborhoods using open sets.  Nothing seems wrong with each statement.  However, if  these statements are simultaneously used,  the definitions of open sets and neighborhoods are circular.  The former is based on the neighborhood-first approach and the latter on the open-set-first approach.  We should not mix these approaches.


The above definition is obviously using a coordinate system.  We want to develop a definition that does not depend on coordinate systems. 



## Topological space

In this section, we first introduce _topology_ which defines open sets without using the concept of neighborhoods.  The neighborhoods and other fundamental concepts will follow.

### Power set

Let $X$ be a set.  Elements of $X$ are called _points_.   The collection of all possible subsets of $X$, $P(X) = \{U: U \subseteq X\}$, is called _power set_.

### Topology and open sets

In hte open-set-first approach, we define open sets based on the following _topology_:

```{prf:definition}
:label: topology
A topology $\mathcal{T}$ on a set $X$ is a collection $\mathcal{T} \subseteq P(X)$ such that

1. $\emptyset \in \mathcal{T}$ and $X \in \mathcal{T}$
2. If  $U_1, U_2, \cdots, U_k \subseteq \mathcal{T}$, then $(U_1 \bigcup U_2 \bigcup \cdots \bigcup U_k) \in \mathcal{T}$
3. If $U_1, U_2 \in \tau$ then $U_1 \bigcap U_2 \in \mathcal{T}$

The pair $(X,\mathcal{T})$ is called a _topological space_.
```

An element of $\mathcal{T}$ is called an _open set_. Note that $X$ can contain both open and closed sets but $\mathcal{T}$ contains only open sets.  A set $A \in X$ is closed if its complement $X \setminus A$ is open.  Since $\emptyset$ and $X$ are elements of $\mathcal{T}$, they must be open by definition.  However, $\emptyset$ is a complement of $X$ and thus must be closed.  Similarly, $X$ is a complement of $\emptyset$, it must be closed as well.  This is seemingly contradictory.  To remove the contradiction, we declare that $\emptyset$ and $X$ are simultaneously open and closed.  Such sets are said to be _clopen_.

Example.  For a finite set $X = \{a,b,c\}$,  several topologies can be defined.  You can show that each of the following $\mathcal{T}$ is a legitimate topology, defining open sets.*$\mathcal{T} = \{ \emptyset, X\}$  (This is called trivial topology.)

* $\mathcal{T} = \{ \emptyset, X, \{a\}\}$
* $\mathcal{T} = \{ \emptyset, X, \{a,b\}\}$
* $\mathcal{T}= \{ \emptyset, X, \{a\},\{b,c\}\}$
* $\mathcal{T} = \{ \emptyset, X, \{a\},\{b\},\{c\}.\{a,b\},\{a,c\},\{b,c\}\}$

Note that $\mathcal{T}^* = \{ \emptyset, X, \{a\}, \{b\}\}$ is not a topology since $\{a\} \bigcup \{b\} = \{a,b\}$ is not an element of $\mathcal{T}^*$.  Similarly, $\mathcal{T}^* = \{ \emptyset, X, \{a\}, \{a,b\},\{b,c\}\}$ is not a topology since $\{a,b\} \bigcap \{b,c\} = \{b\}$ is not in $\mathcal{T}^*$.

Finite sets like the above example is useful for a demonstration of the concept of topology.  In physics, however, we are interested in topology of infinite sets.  We will show an example of infinite topological space shortly.

### Neighborhoods

The definition of open sets  based on topology is not  intuitive.  Physicists always want to visualize ideas and concepts by drawing pictures. To do so, we introduce a set around a point  called neighborhood.

```{prf:definition}
:label: neighborhood

Let $(X,\mathcal{T})$ be a topological space.  For point $p \in X$, a subset $N_p \subseteq X$ is a neibour of $p$ if there exists $V \in \mathcal{T}$ such that $p \in V \subseteq N_p$.
```

A neighborhood is a set containing an open set containing a given point. 

```{prf:proposition}
:label: openset-by-neighborhood

A subset $U \subseteq X$ is open if and only if every point $p \in U$ has a neighborhood contained in $U$. 
```

 With this proposition, we  can easily visualize the concept of open set.  The question is if this statement is consistent with the definition of open sets based on topology.  As warned earlier, be aware of circular argument.  The proposition {prf:ref}`openset-by-neighborhood` is not the definition of open sets.  It follows from {prf:ref}`topology`.

If for every $p \in U$ has a neighborhood $N_p$ contained in $U$, there exists an open set $V_p $ such that $p \in V_p \subseteq N_p$.  Since $V_p$ is open, it must be an element of 


## The Euclidean Topology


Although we are already familiar with the Euclidean space, we want to redefine it as a topological space for consistency.   In many literature, $\mathbb{R}$ appears equivalent to the one-dimensional Euclidean space.  For higher dimensions, $\mathbb{R}^n$ is used.  However, $\mathbb{R}$ alone cannot be a topological space.  We need to define a topology on $\mathbb{R}$, which is called the Euclidean topology.  

```{prf:definition}
:label: Euclidean-topology

In a simple term, the Euclidean topology is a collection of all open intervals $\{(a, b): a, \, b \in \mathbb{R}, \; a \lt b\}$ including $\mathbb{R} = (-\infty,\infty)$ and the empty set.  
```

For a higher dimension, open intervals are replaced with open balls.  For $\mathbb{R}^2$,  the Euclidean topology is a collection of all open disks $\{\langle x,y\rangle: (x-a)^2+(y-b)^2 < c^2, a,b,c \in \mathbb{R}\}$ and $\emptyset$.  Similarly for $\mathbb{R}^3$, we can use a collection of all open balls.

In many literature $\mathbb{R}$ is meant to be the Euclidean topological space without specifying the topology since it  is the  topological space most commonly used in physics.
