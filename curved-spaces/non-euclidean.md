(sec:non-euclidean-spaces)=

# Non-Euclidean spaces

In this chapter, we introduce concepts of Euclidean space and non-Euclidean space in a naive way.  As a starting point of the this clecture note, we avoid abstract definitions used by mathematicians for now.


##  Euclidean spaces

An Euclidean space (also known as a flat space among physicists) is,  roughly speaking,  a space in which the axioms of Euclidean geometry ({prf:ref}`axiom-euclidean-geometry`)  are valid. It is directly based on what we experince in daily life. While this definition is outdated and modern mathematics defines it in a quite different way, the ancient definition is still useful to understand the concepts of the Euclicean spaces.  It is good enough for us at the present stage and we will introduce new definition as needed in later chapters.

In 300 BC, an ancient Greek mathemaicisn named Euclid wrote 13 volumes of books entitled _The Elements_, which discuss all about geometry.  In the first volume,  he listed the five axioms ({prf:ref}`axiom-euclidean-geometry`)  and attempted to derive all other properties of geometry in the book from the axioms .  IIt is known that he used unstated assumptions and unstated principles.   So, the five axioms are not enough.  Nevertheless, Learning them is a good starting point to learn geometry.

```{prf:axiom}
:label: axiom-euclidean-geometry

1. A straight line segment can be drawn between any two points.
2. A straight line segment can be extended indefinitely in a straight line.
3. A circle can be drawn with any center and any radius.
4. All right angles are equal to one another.
5. Given a line and a point not on that line, there is exactly one line through the point that is parallel to the given line. 
```
The 5th axiom is known as the parallel postulate. The most iconic concequence of the parallel postulate is this: " The interior angles of a triangle sum to exactly 180° " .  This property is a defining charactersitcs of the Euclidean geometry and its violation immediately means non- Eculidean geometry as shwon below.


## Breakdowns of Euclidean geometry

Rouchly speaking, if one or more of the above axioms breaks down, then you are in a non-Euclidean space.  Let us take a close look at each axiom.  As far as phyciscs concerns, the axiom one is unbreakable since we can alweays define a straight line even on a non-Euclidean space.  Similarly, axiom 2 can be satisifed by defining a straight line.  While distance (or metric which we will discuss in later chapters) not always can be defined,  in physics we always work on the spaces where distance is well defined.  Then, we can define circles even if the spaces are not Euclidean.  Therefore, axiom 3 can be satisfied.  Similarly, in the spaces physicists are working on, inner products are defined (metric allows it) and  we can define right angles. They are all equal to each other.  Then, axiom 4 is satisfied.

Now we turn to axiom 5.   We can define straight lines to satisify axiom 1 and 2.  However, two striaght lines look parallel at a certain location may cross to each other at other location.  We can see that on the surface of sphere.  A straight line is defined as a line on a great circle whose center coincides with the center of the sphere, satisfying axiom 1.  Such line can be extended indefnitely by circling arond the sphere.  Then,  on the equator, we draw a short segment of a straight line to the north.   Drow another line next to the first one, again to the north. Following axim 2, we extend the lines.  Eventually they cross each other at the north pole as well as at the south pole in violotion of axiom 5. (See {numref}`fig-parallel-on-sphere`)  Hence, the Euclidean geometry breaks down on the surface of a sphere.  That is wierd. Euclid developed the axioms on the surface of Earth where axiom 5 fails.  In 300 BC, Euclid did not know that he lives on a sphere.  Don't blame him.  We also feel standing on a flat surface.  If we draw two lines parallel to each other on our desk,  they won't cross each other even they are extended beyond my eye sight.  This suggest that a small area on a sphere can be treated as if it is flat.  The theorey of differential geometry strongly depend on this idea.  Such an area is said to be a local Euclidean space. 

```{figure} ./parallel-on-sphere.png
---
name: fig-parallel-on-sphere
height: 300px
---
When two parallel lines shown in red are extended, they cross at the north and south poles.

```

Now that the parallel postulate is violdated,  the inner angles of a triangle are not necessarily summed to 180$^\circ$.   You can see it easily on a sphere.  Observation of a triangle becomes a decisive method to determine if a space is non-Euclidean.  Measurement of astronomically large triangles suggest that the universe is pretty flat at the scale of the triangle tehy measured.  So, there is no direct measurement of the angles near large stars or black holes where the Euclidean geometry is broken.  However, there are plenty of indirect measurements including the famous Arthur Eddington's experiment in 1919.

```{figure} ./triangle-on-sphere.png
---
name: fig-triangle-on-sphere
height: 300px
---
When two lines perpendicular to the equator mearge at the north pole, forming a triangle as shown in red.  The agnle between the vertical line toward the north pole and the quator is 90$^\circ$.  The sum of all inner angles is larger than 180^\circ$, suggesting that the surface of the sphere is non-Euclidean.

```