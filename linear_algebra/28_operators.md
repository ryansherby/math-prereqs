# Operators in Linear Algebra

In linear algebra, an **operator** is a function that maps vectors from one vector space to another (or to itself). Operators play a crucial role in various mathematical applications, including differential equations, quantum mechanics, and computer graphics. They are typically represented by matrices when dealing with finite-dimensional vector spaces.

## Definition

An **operator** $T$ is a function that maps vectors from a vector space $V$ to itself or another vector space $W$. If $T$ maps vectors from $V$ to $W$, it is denoted as:

$$
T: V \to W
$$

When $V = W$, the operator is called a **linear operator** or **linear transformation**. A linear operator $T$ is defined by the property that for any vectors $\mathbf{u}, \mathbf{v} \in V$ and any scalar $\alpha$, the following conditions hold:

$$
T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})
$$

$$
T(\alpha \mathbf{u}) = \alpha T(\mathbf{u})
$$

## Matrix Representation

When $V$ and $W$ are finite-dimensional vector spaces with dimensions $n$ and $m$, respectively, an operator $T$ can be represented by an $m \times n$ matrix $A$. For a vector $\mathbf{x} \in \mathbb{R}^n$, the action of $T$ on $\mathbf{x}$ is given by:

$$
T(\mathbf{x}) = A \mathbf{x}
$$

## Examples

### Example 1: Linear Operator in $\mathbb{R}^2$

Consider the operator $T$ defined by:

$$
T \begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}
= \begin{pmatrix}
2x_1 + 3x_2 \\
4x_1 - x_2
\end{pmatrix}
$$

**Matrix Representation:**

The matrix $A$ representing $T$ is:

$$
A = \begin{pmatrix}
2 & 3 \\
4 & -1
\end{pmatrix}
$$

So, the action of $T$ on a vector $\mathbf{x} \in \mathbb{R}^2$ is given by:

$$
T(\mathbf{x}) = A \mathbf{x}
$$

**Example Calculation:**

For $\mathbf{x} = \begin{pmatrix}
1 \\
2
\end{pmatrix}$:

$$
T \begin{pmatrix}
1 \\
2
\end{pmatrix}
= \begin{pmatrix}
2 \cdot 1 + 3 \cdot 2 \\
4 \cdot 1 - 1 \cdot 2
\end{pmatrix}
= \begin{pmatrix}
8 \\
2
\end{pmatrix}
$$

### Example 2: Rotation Operator in $\mathbb{R}^2$

Consider the operator $R$ that rotates vectors in $\mathbb{R}^2$ by an angle $\theta$. The matrix representing a counterclockwise rotation by $\theta$ is:

$$
R = \begin{pmatrix}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{pmatrix}
$$

**Example Calculation:**

For $\theta = 90^\circ$ (or $\frac{\pi}{2}$ radians):

$$
R = \begin{pmatrix}
\cos \frac{\pi}{2} & -\sin \frac{\pi}{2} \\
\sin \frac{\pi}{2} & \cos \frac{\pi}{2}
\end{pmatrix}
= \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
$$

For a vector $\mathbf{x} = \begin{pmatrix}
1 \\
0
\end{pmatrix}$:

$$
R \begin{pmatrix}
1 \\
0
\end{pmatrix}
= \begin{pmatrix}
0 \cdot 1 - 1 \cdot 0 \\
1 \cdot 1 + 0 \cdot 0
\end{pmatrix}
= \begin{pmatrix}
0 \\
1
\end{pmatrix}
$$

### Example 3: Projection Operator in $\mathbb{R}^3$

Consider the projection operator $P$ that projects vectors in $\mathbb{R}^3$ onto the $xy$-plane. The matrix representing this projection is:

$$
P = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix}
$$

**Example Calculation:**

For $\mathbf{x} = \begin{pmatrix}
2 \\
3 \\
4
\end{pmatrix}$:

$$
P \begin{pmatrix}
2 \\
3 \\
4
\end{pmatrix}
= \begin{pmatrix}
1 \cdot 2 + 0 \cdot 3 + 0 \cdot 4 \\
0 \cdot 2 + 1 \cdot 3 + 0 \cdot 4 \\
0 \cdot 2 + 0 \cdot 3 + 0 \cdot 4
\end{pmatrix}
= \begin{pmatrix}
2 \\
3 \\
0
\end{pmatrix}
$$

## Summary

Operators in linear algebra are functions that map vectors from one vector space to another (or to itself). They are represented by matrices when dealing with finite-dimensional spaces. Operators can perform various transformations, including rotations, projections, and scalings. Understanding operators is fundamental for analyzing linear systems and their properties.
