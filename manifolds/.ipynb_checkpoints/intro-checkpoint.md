# Smooth Manifolds

**Introduction**

In {numref}`ch:topological-space`, we define topological spaces based on open sets, which is a necessary mathematical step to construct spaces that physics needs, namely curved spaces discussed in {numref}`ch:what-are-curved-spaces`.   Our understanding of physics is deeply dependent upon mathematics on Euclidean spaces. That is because we feel we are in a flat surface.  Constructing physics on curved space from scratch won't be very attractive since our universe seems not very far from a flat space.  We seek an approach in which Euclidean space is a good approximation inside a small area and the curved space are covered by many patches of flat spaces so that space looks like flat in a neighborhood of  each point. 

Based on the above idea, we imagine a topological space in which every point has a neighborhood that looks like a flat space. Such a topological space is called a `manifold`.  For example, a circle is a manifold.  You can imagine a circle approximated by a regular polygon. As the number of edges increases, the polygon approaches a sphere.  In other words, a circle can be approximated with  piecewise straight lines and the straight lines are flat spaces $\mathbb{R}$.

In this chapter, we learn how to map a subspace of a curved space to a Euclidean space.  A small open subset in a topological space is mapped to a $n$-dimensional Euclidean space or $\mathbb{R}^n$. Such a map is called a `chart`. Another small open subset in the topological space is mapped to another $n$-dimensional space.  By repeating this process, The entire topological space is covered by many small open subsets each of which is mapped to its own $\mathbb{R}^n$ through a chart.  The set of charts that covers the whole space is called `atlas`. A amnifold equipped with charts to $\mathbb{n}$is called $n$-dimensional manifold or simply $n$-manifold.  A circle is a 1-manifold.

Now, we want to calculate something on a small open subset but we don't know how because the space is not flat.  Thanks to a chart, we can move to a Euclidean space and use the usual mathematics to calculate it.  Then, we can take back the result to the original manifold using the inverse of the chart.  In this lecture, we will be doing this all time.  We move back and forth between a manifold and a Euclidean space through a chart because we know how to calculate only on a Euclidean space.

The idea of chart is nice but we need to be careful.  The result of calculation done on a chart is valid only within the small open subset where the chart originated.  The calculations on two adjacent charts are not directly related.  However, physical quantities are continuous and mostly smooth.   Hence, the result of a calculation on a chart must be smoothly connected to the result of the same calculation on next chart.  The smoothness is essential for physics. Therefore, we need a `smooth manifold`.    You will see in later chapters that the smoothness across charts is essential for physics on curved space.


 ```{admonition} Objectives
 
Key points are:

1. What is a chart and an atlas?
1. How do we transfer a function on the manifold to a Euclidean space specified by a chart?
2. How do we transfer back the result obtained on a chart to a manifold?
3. How can we make it sure that a function evaluated on two adjacent charts are continuous across the charts?

```
  