## Integrals in Multivariate Calculus

In multivariate calculus, integrals extend the concept of integration from single-variable functions to functions of multiple variables. These integrals are used to compute quantities such as areas, volumes, and other measurements in higher dimensions.

### Definition

1. **Double Integrals**:
   - **Definition**: A double integral extends the concept of a single integral to functions of two variables. It is used to compute the volume under a surface defined by a function $f(x, y)$ over a region $D$ in the $xy$-plane.
   - **Notation**: 
   
     $$
     \iint_D f(x, y) \, dA
     $$
     
     where $dA$ is the differential area element, often represented as $dx \, dy$ or $dy \, dx$.
   - **Example**: To compute the volume under the surface $z = f(x, y) = x^2 + y^2$ over the unit square $D = [0,1] \times [0,1]$, we set up the double integral:
   
     $$
     \iint_{[0,1] \times [0,1]} (x^2 + y^2) \, dx \, dy
     $$
     
     Evaluating this integral:
     
     $$
     \int_0^1 \int_0^1 (x^2 + y^2) \, dx \, dy = \int_0^1 \left[ \frac{x^3}{3} + y^2 x \right]_0^1 \, dy = \int_0^1 \left( \frac{1}{3} + y^2 \right) \, dy = \frac{1}{3} + \frac{1}{3} = \frac{2}{3}
     $$

2. **Triple Integrals**:
   - **Definition**: A triple integral extends the concept of integration to functions of three variables. It is used to compute the volume of a region in three-dimensional space or to find the mass of a solid with varying density.
   - **Notation**:
   
     $$
     \iiint_D f(x, y, z) \, dV
     $$
     
     where $dV$ is the differential volume element, often represented as $dx \, dy \, dz$.
   - **Example**: To compute the mass of a solid with density $\rho(x, y, z) = x + y + z$ over the unit cube $D = [0,1] \times [0,1] \times [0,1]$, we set up the triple integral:
   
     $$
     \iiint_{[0,1] \times [0,1] \times [0,1]} (x + y + z) \, dx \, dy \, dz
     $$
     
     Evaluating this integral:
     
     $$
     \int_0^1 \int_0^1 \int_0^1 (x + y + z) \, dx \, dy \, dz
     $$
     
     Compute the innermost integral:
     
     $$
     \int_0^1 (x + y + z) \, dx = \left[ \frac{x^2}{2} + xy + xz \right]_0^1 = \frac{1}{2} + y + z
     $$
     
     Now integrate with respect to $y$:
     
     $$
     \int_0^1 \left( \frac{1}{2} + y + z \right) \, dy = \left[ \frac{1}{2}y + \frac{y^2}{2} + yz \right]_0^1 = \frac{1}{2} + \frac{1}{2} + z = 1 + z
     $$
     
     Finally, integrate with respect to $z$:
     
     $$
     \int_0^1 (1 + z) \, dz = \left[ z + \frac{z^2}{2} \right]_0^1 = 1 + \frac{1}{2} = \frac{3}{2}
     $$

### Applications

1. **Finding Areas**: Double integrals are used to find the area of regions in the plane by integrating the constant function $f(x, y) = 1$ over the region.
2. **Finding Volumes**: Double and triple integrals are used to compute volumes under surfaces and within solids in three-dimensional space.
3. **Center of Mass**: Triple integrals can be used to compute the center of mass of a solid body by integrating the density function.

### Techniques

1. **Changing the Order of Integration**: Sometimes, changing the order of integration in double integrals can simplify the computation. For example, inverting the order of $dx$ and $dy$ in a double integral.
2. **Using Cylindrical and Spherical Coordinates**: For problems with symmetry, switching to cylindrical or spherical coordinates can simplify triple integrals.
   - **Cylindrical Coordinates**: Useful for problems with cylindrical symmetry, where $x = r \cos \theta$, $y = r \sin \theta$, and $z = z$.
   - **Spherical Coordinates**: Useful for spherical symmetry, where $x = \rho \sin \phi \cos \theta$, $y = \rho \sin \phi \sin \theta$, and $z = \rho \cos \phi$.

In summary, integrals in multivariate calculus extend the concept of integration to multiple dimensions, allowing for the computation of areas, volumes, and other quantities in higher-dimensional spaces.
