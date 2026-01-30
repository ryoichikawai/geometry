#  Topology and open sets

In this section, mathematical concepts of _topology_ and _open sets_ are introduced.  We begin with open intervals, which we are already familiar with.  In the following subsection, we extend the open intervals to abstract spaces and redefine the open sets without invoking coordinates.   At the end, we come back to $\mathbb{R}$ and demonstrate that the new definitions are consistent with the old one.

## Open intervals in $\mathbb{R}$
The concept  of open sets plays a key role in mathematics and so does in physics.  An example is  open interval $(a,b)$ in real number $\mathbb{R}$, which is a set of all real number between two given end points $a$ and $b$, but not including the endpoints themselves.  It formally defined as

```{prf:definition}
:label: open-interval

$$
(a,b) =\{x \in \mathbb{R}~|~ a < x < b\}
$$

where $a, b \in \mathbb{R}$ and $ a < b$.
```
_Neighborhood_ is a mathematical concept closely related to the open sets. 

```{prf:definition}
:label: neighborhood-as-interval-in-R

A set $𝑁 \in \mathbb{R}$ is called a neighborhood of $x \in \mathbb{R}$ if there exists  $\epsilon > 0$ such that

$$
(x-\epsilon, x+\epsilon) \subseteq N
$$
```
Knowing the definition of open intervals and neighborhoods, we can describe open sets with the neighborhoods.

```{prf:proposition}
:label: open-interval-in-R-by-neighborhood

An interval $(a,b) \in \mathbb{R}$ is open if and only if for each $x \in (a,b)$, there exists a neighborhood of $x$ that is completely inside the interval $(a,b)$.

```
In summary, we define open interval first and the, we define neighborhoods using the open interval.  At the end, we showed the relation between open intervals and neighborhoods.  This logical steps are important when we extend these mathematical concepts beyond $\mathbb{R}$.

There is another approach in which we define neighborhoods first. Then, open interval is defined with the neighborhoods. We call it the neighborhood-first-approach and the previous approach the open-set-first approach.  In physics, the open-set-first approach is much more popular than the other and we as physicists follow this tradition.  When we read literature, in particular math books, we must be careful about these two approaches.  When you mix  them, you can be trapped in circular arguments.  For example, you will find the following definitions in literature.

* A set $U$ is open if every point in $U$ has a neighborhood contained in $U$.
* A set $N$ is a neighborhood of $x \in X$ if it contains an open set $U$ such that $U$ contains $x$.

The first statement defines open sets using neighborhoods. The second statement defines neighborhoods using open sets.  Nothing seems wrong with each statement.  However, if  these statements are simultaneously used,  the definitions of open sets and neighborhoods are circular.  The former is based on the neighborhood-first approach and the latter on the open-set-first approach.  We should not mix these approaches.

## Topological space

The above definitions of open sets and neighborhoods are obviously based on a coordinate system.  We want to develop definition that are independent of coordinates. 

In this section, we first introduce _topology_ which defines open sets without using the concept of neighborhoods.  The neighborhoods and other fundamental concepts will follow.

### Power set

Let $X$ be a set.  Elements of $X$ are called _points_.   The collection of all possible subsets of $X$, $P(X) = \{U: U \subseteq X\}$, is called _power set_.

### Topology and open sets

In the open-set-first approach, we define open sets based on the following _topology_:

```{prf:definition}
:label: topology
A topology $\mathcal{T}$ on a set $X$ is a collection $\mathcal{T} \subseteq P(X)$ such that

1. $\emptyset \in \mathcal{T}$ and $X \in \mathcal{T}$
2. If  $U_1, U_2, \cdots, U_k \subseteq \mathcal{T}$, then $(U_1 \bigcup U_2 \bigcup \cdots \bigcup U_k) \in \mathcal{T}$
3. If $U_1, U_2 \in \tau$ then $U_1 \bigcap U_2 \in \mathcal{T}$

The pair $(X,\mathcal{T})$ is called a _topological space_.
```

An element of $\mathcal{T}$ is called an _open set_. Note that $X$ can contain both open and closed sets but $\mathcal{T}$ contains only open sets.  A set $A \in X$ is closed if its complement $X \setminus A$ is open.  Since $\emptyset$ and $X$ are elements of $\mathcal{T}$, they must be open by definition,  which is seemingly contradictory.  $\emptyset$ is a complement of $X$ and thus must be closed.  Similarly, $X$ is a complement of $\emptyset$, it must be closed as well.   To remove the contradiction, we declare that $\emptyset$ and $X$ are simultaneously open and closed.  Such sets are said to be _clopen_.

Example.  For a finite set $X = \{a,b,c\}$,  several topologies can be defined.  You can show that each of the following sets is a legitimate topology, defining open sets.

* $\{ \emptyset, X\}$  (This is called trivial topology.)
* $\{ \emptyset, X, \{a\}\}$
* $\{ \emptyset, X, \{a,b\}\}$
* $\{ \emptyset, X, \{a\},\{b,c\}\}$
* $\{ \emptyset, X, \{a\},\{b\},\{c\}.\{a,b\},\{a,c\},\{b,c\}\}$

Note that $\{ \emptyset, X, \{a\}, \{b\}\}$ is not a topology since $\{a\} \bigcup \{b\} = \{a,b\}$ is not included.  Similarly, $\{ \emptyset, X, \{a\}, \{a,b\},\{b,c\}\}$ is not a topology since $\{a,b\} \bigcap \{b,c\} = \{b\}$ is absent.

Finite sets like the above example is useful for a demonstration of the concept of topology.  In physics, however, we are interested in topology of infinite sets.  Mathematically speaking, infinitely many topologies are possible. However, various physical conditions almost uniquely pick a particular topology.  Unfortunately, physicists never explicitly state it and implicitly assume a context-dependent topology, causing confusions among mathematically oriented students.  We shall be careful about it. 

### Neighborhoods

The definition of open sets  based on topology is not  intuitive.  Physicists always want to visualize ideas and concepts by drawing pictures. To do so, we introduce a set around a point  called neighborhood.

```{prf:definition}
:label: neighborhood

Let $(X,\mathcal{T})$ be a topological space.  For point $p \in \mathcal{T}$, a subset $N_p \subseteq X$ is a neighbor of $p$ if there exists $V \in \mathcal{T}$ such that $p \in V \subseteq N_p$.
```

In brief, a neighborhood is a set containing an open set containing a given point. Note that the neighborhood does not have to be open and thus is not necessarily a subset of $\mathcal{T}$.

```{prf:proposition}
:label: openset-by-neighborhood

A subset $U \subseteq X$ is open if and only if every point $p \in U$ has a neighborhood contained in $U$. 
```

 With this proposition, we  can easily visualize the concept of open set.  The question is if this statement is consistent with the definition of open sets based on topology.  As warned ealier, be aware of circular arguments.  The proposition {prf:ref}`openset-by-neighborhood` is not the definition of open sets.  It follows from {prf:ref}`neighborhood` that if for every $p \in U$ has a neighborhood $N_p$ contained in $U$, there exists an open set $V_p $ such that $p \in V_p \subseteq N_p$.

## The Euclidean Topology

Although we are already familiar with the Euclidean space, we want to redefine it as a topological space for consistency.   In many literature, $\mathbb{R}$ appears equivalent to the one-dimensional Euclidean space.  For higher dimensions, $\mathbb{R}^n$ is used.  However, $\mathbb{R}$ alone cannot be a topological space.  We need to define a topology on $\mathbb{R}$, which is called the Euclidean topology.  

```{prf:definition}
:label: Euclidean-topology

In a simple term, the Euclidean topology is the collection of all unions of open intervals $\{(a, b): a, \, b \in \mathbb{R}, \; a \lt b\}$ including $\mathbb{R} = (-\infty,\infty)$ and the empty set.  
```

For a higher dimension, open intervals are replaced with open balls.  For $\mathbb{R}^2$,  the Euclidean topology is a collection of all open disks $\{\langle x,y\rangle: (x-a)^2+(y-b)^2 < c^2, a,b,c \in \mathbb{R}\}$ and $\emptyset$.  Similarly for $\mathbb{R}^3$, we can use a collection of all open balls.

In many literature $\mathbb{R}$ is meant to be the Euclidean topological space without specifying the topology since it is the  topological space most commonly used in physics. The Euclidean topology is the smallest topology out of $\mathbb{R}$ that makes all linear functions, translations, and limits behave as expected and {prf:ref}`Euclidean-topology` guarantees that

* addition
* multiplication
* limits of sequences
* derivatives
* integrals

are well defined and continuous.

What topology on curved spaces guarantee the same mathematical structures?  That is the question the present lecture note tries to answer.