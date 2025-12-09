(ch:vector-fields)=
# Vector Fields

**Introduction**

The concept of vector fields has changed dramatically as we comprehend the Einstein's theory of general  relativity.  Electric fields are no longer considered as vector fields .  They are 1-form fields and magnetic fields are 2-form fields.  To reach this results, we need to go through a lengthy abstract mathematics.  In fact, even mathematicians struggled to develop a rigorous theory now known as differential manifolds.

We encounter vector fields in various undergraduate physics courses and we also learn vector calculus required to mathematically understand the vector fields.  A naive definition of vector fields just assign a vector at each point in a space, where a vector is an element of a vector space.  It turns out that such definition cannot be used for vector fields on curved spaces.  In the Euclidean space, vectors assigned to two different points can be directly compared since the basis vectors are same everywhere.  The unit vectors in the $x$ direction is same at every point. Hence, we need only one vector space for the whole space.  This is a very powerful property of the Euclidean space.  Vector fields must be smooth function over the whole space.  Due to the homogeneous structure, it is easy to construct smooth functions.

On curved spaces, the simple definition of vector fields fails since we cannot compare two vectors at different points in the space.  Since there is no universal coordinates, $x$ direction at $p$ and $x$ direction at $q$ are not related.  In other words, we need define a vector space at each point.  The vector spaces at different points do not have to be the same.  We need to assign a vector at each point from the particular vector space at that point.  How do we define an appropriate vector space at a given point?  We will see that tangent vector spaces serve as such local vector spaces.

There are further difficulty, the vector fields must be continuous and smooth throughout the space. That means as we move through a space, a vector assigned to a point must change smoothly. How can we do that when we cannot compare vectors at different points.  Because of this requirement, it is not a good idea to start with the local vector space.  Arrow-at-point approach does not work on curved space.

The modern approach first define a vector field as a smooth function.  This itself requires a deep thought and its mathematical realization is rather abstract.   We recall that smoothness was a key element of topological spaces.   So, we will be using properties of topological space or more precisely manifolds.

From the vector fields, we construct a vector space known as tangent space at each point using the concept of tangent vectors.   The tangent space is a usual vector space we are familiar with  and the actual vector assigned to each point is  selected from the tangent space.



