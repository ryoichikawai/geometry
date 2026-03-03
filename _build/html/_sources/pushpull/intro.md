(ch:pullback-pushforward=)

# Pullback and pushfoward

**Introduction**

Whenever we want to calculate something on a manifold $M$, we move to a Euclidean geometry $\mathbb{R}^n$ with a chart and carry out the calculation there. However, the result is valid only small area on the Manifold.  Recall that a a chart is a map from an open subset $U \subseteq M$ to $\mathbb{R}^n$ where $U$ is a neighborhood of a point $p$ on $M$.  Hence the result is valid only inside of $U$.  When we move to another part of $M$, we have a different chart.  The results of calculation done through two different charts cannot be compared directly.  Then, how can make it sure that the result are smoothly connected across the charts.  We need to take the results back to the manifold and make it sure that they are consistent to each other.  In this chapter, we learn how to move mathematical objects back and forth between a manifold and a Euclidean space using a chart.


It turns out that there are two types of transfer operations,  `pushforward` and `pullback`.  Mathematical objects that are transferred by the pushforward is said to be `covariant` and those by pullback is `contravariant`.  


```{admonition} Objectives

1. Copying coordinates on the Eunclidean space to the manifold. What is the local coordinates on a manifold?  
2. Copying a function between the Euclidean space and the manifold  by pullback.
3. Copying a tangent vector between the Euclidean space and the manifold by pushfoward.
4. Copying a 1-form between the Euclidean space and the manifold  by pullback.
5. Copying a p-form between the Euclidean space and the manifold  by pullback/pushforward.

```


