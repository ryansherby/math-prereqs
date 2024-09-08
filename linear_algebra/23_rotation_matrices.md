# Rotation Matrices in Linear Algebra

In linear algebra, a **rotation matrix** is a special type of orthogonal matrix used to perform rotations in Euclidean space. Rotation matrices are widely used in computer graphics, robotics, and physics to describe rotations of objects in space.

## Definition

A matrix $R$ is called a **rotation matrix** if it is an orthogonal matrix with a determinant of 1. This means:

1. **Orthogonality**: The rows and columns of $R$ are orthonormal vectors.
2. **Determinant**: The determinant of $R$ is 1.

Mathematically, a rotation matrix satisfies:

$$
R R^T = R^T R = I
$$

$$
\text{det}(R) = 1
$$

where $R^T$ denotes the transpose of $R$, $I$ is the identity matrix, and $\text{det}(R)$ is the determinant of $R$.

### 2D Rotation Matrix

In 2-dimensional space, a rotation matrix that rotates a vector by an angle $\theta$ counterclockwise is given by:

$$
R(\theta) = \begin{pmatrix}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{pmatrix}
$$

### 3D Rotation Matrix

In 3-dimensional space, rotation matrices can be defined around the coordinate axes. For an angle $\theta$:

- **Rotation about the x-axis**:

  $$
  R_x(\theta) = \begin{pmatrix}
  1 & 0 & 0 \\
  0 & \cos \theta & -\sin \theta \\
  0 & \sin \theta & \cos \theta
  \end{pmatrix}
  $$

- **Rotation about the y-axis**:

  $$
  R_y(\theta) = \begin{pmatrix}
  \cos \theta & 0 & \sin \theta \\
  0 & 1 & 0 \\
  -\sin \theta & 0 & \cos \theta
  \end{pmatrix}
  $$

- **Rotation about the z-axis**:

  $$
  R_z(\theta) = \begin{pmatrix}
  \cos \theta & -\sin \theta & 0 \\
  \sin \theta & \cos \theta & 0 \\
  0 & 0 & 1
  \end{pmatrix}
  $$

## Examples

### Example 1: 2D Rotation

Consider rotating a vector by 45 degrees counterclockwise. The rotation matrix for $\theta = 45^\circ$ is:

$$
R(45^\circ) = \begin{pmatrix}
\cos 45^\circ & -\sin 45^\circ \\
\sin 45^\circ & \cos 45^\circ
\end{pmatrix}
= \begin{pmatrix}
\frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} \\
\frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2}
\end{pmatrix}
$$

**Step 1: Apply Rotation to a Vector**

Rotate the vector $v = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$:

$$
R(45^\circ) \begin{pmatrix}
1 \\
0
\end{pmatrix}
= \begin{pmatrix}
\frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} \\
\frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2}
\end{pmatrix}
\begin{pmatrix}
1 \\
0
\end{pmatrix}
= \begin{pmatrix}
\frac{\sqrt{2}}{2} \\
\frac{\sqrt{2}}{2}
\end{pmatrix}
$$

The result is the vector rotated by 45 degrees.

### Example 2: 3D Rotation

Consider a rotation about the z-axis by 90 degrees. The rotation matrix is:

$$
R_z(90^\circ) = \begin{pmatrix}
\cos 90^\circ & -\sin 90^\circ & 0 \\
\sin 90^\circ & \cos 90^\circ & 0 \\
0 & 0 & 1
\end{pmatrix}
= \begin{pmatrix}
0 & -1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$

**Step 1: Apply Rotation to a Vector**

Rotate the vector $v = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}$:

$$
R_z(90^\circ) \begin{pmatrix}
1 \\
1 \\
0
\end{pmatrix}
= \begin{pmatrix}
0 & -1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
1 \\
1 \\
0
\end{pmatrix}
= \begin{pmatrix}
-1 \\
1 \\
0
\end{pmatrix}
$$

The result is the vector rotated by 90 degrees around the z-axis.

## Summary

Rotation matrices are essential tools in linear algebra for performing rotations in Euclidean space. In 2D, the rotation matrix rotates vectors by a specified angle, while in 3D, rotation matrices rotate around the coordinate axes. They are orthogonal matrices with a determinant of 1 and preserve vector lengths and angles during transformations.
