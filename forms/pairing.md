(sec:duarity-pairing)=
# Duarity paring

Before going to define inner products on a manifold, we review traditional  inner products we have been using in the Euclidean space.   We often think of inner product (dot product) between two vectors.  For two vectors $\vec{a} = \sum_i a^i \mathbb{e}^i$ and $\vec{b} = \sum_i b^i \mathbb{e}^i$ where $\{\mathbb{e}_i\}$ is orthonormal basis vectors,  their inner product is simply $\vec{a} \cdot \vec{b} =\sum_i a^i b^i$ as seen in freshman physics courses.  The orthonormality  $\mathbb{e}_i \cdot \mathbb{e}_j = \delta_{ij}$ is essential.   This inner product between two Euclidean vectors is actually a rather special case. It is a map from a product space $V \times V$ to $\mathbf{R}$ where $V$ is a vector space spanned by an orthonormal basis set $\{\mathbb{e}_i\}$.

However, in many cases, inner product is actually between a vector and a dual vector.   In other words, it is a map from $V^\dagger \times V$ to $\mathbb{R}$ where $V^\dagger$ is another vector space dual to $V$.   For example, if  vectors $A, B \in V$ are expressed as column matrices, the inner product is $A^T B$ where $A^T$ is a transpose of $A$.  The transposed vector $A^T \in V^\dagger$ is a dual vector to $A$.  In quantum mechanics, inner product is defined between a ket vector $|\psi\rangle$ and a bra vector $\langle \phi|$ where the bra vector $\langle \phi|$ is dual to the ket vector $|\phi\rangle$.

The use of dual vectors becomes essential when the basis vectors are not orthogonal to each other.  Let $\qquad g_{ij} \equiv \mathbb{e}_i \cdot \mathbb{e}_j$.  The inner product becomes 

```{math}
:label: eq:inner-product
\vec{a}\cdot\vec{b} = \sum_{i,j} g_{ij} a^i b^j
```

where $g_{ij}$ is called metric tensor which we will discus later.

If we define a dual vector 

```{math}
:label: eq:dual-vector
a_j = g_{ij} a^i
```

Notice that the location of the index moved from top to bottom.   With this transformation  then the expression of the product is much simpler, $\vec{a} \cdot \vec{b} = \sum_j a_jb^j$ or just $a_j b^j$ if the Einstein's convention is used.  The use of dual vectors indeed simplifies the expression of inner product because the metric information is hidden in the dual vectors.  A similar situation can be seen in solid state physics.  The  lattice vectors are expressed with basis vectors $\mathbb{e}_i$ defined with a unit cell of the crystal.  Unless the unit cell is cubic,  the basis vectors are not orthonormal to each other .  In order to avoid  the complicated expression of inner products, reciprocal basis vectors $\hat{\mathbb{e}}^i$ is introduced such that $\hat{\mathbb{e}}^i \cdot \mathbb{e}_j = \delta_{j}^{i}$.

Now we look at 1-form again. In the Euclidean space, the directional derivative $v(f) = v^\mu(x) \partial_\mu f(x)$ is an inner product between vector field $v(x)$ and  gradient $\nabla f(x)$,  The gradient on a manifold corresponds to a 1-form.  Furthermore, Eq. {eq}`eq:omega-v-orthogonality` suggests that the basis of vector and the basis of 1-form looks like orthogonal similar to lattice-vs-reciprocal relation in a crystal.   So, it is natural to think of  inner product between vector field $v$ and 1-form $\omega$.    In fact, \omega(v)$  likes like an inner product as you can see in the following expression:

```{math}
:label: eq:duarity-pair
\omega(v) = \omega_\mu dx^\mu(v^\nu \partial_\nu) = \omega_\mu v^\nu \delta^\mu_\nu = \omega_\mu v^\mu
```

But is this an inner product?  Actually it is not a true inner product because $\omega$ is not dual to $v$.  There is no relation between $\omega$ and $v$ .  More precisely, no metric tensor is defined at the present stage and thus we cannot construct a dual of $v$ like {eq}`eq:dual-vector`.  We need to wait for  metric tensor defined in a later chapter.

Instead we call {eq}`eq:duarity-pair` `duality pair` or `contraction` and denote it as $\langle \omega,v\rangle \equiv \omega (v)$. We will come back to this issue later.

