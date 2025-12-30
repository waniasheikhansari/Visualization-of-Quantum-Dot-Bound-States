# Quantum Dots: Analytical Origin of a Qubit
### Particle in a 3D Infinite Potential Box

---

## 1. Physical Setup and Potential

Consider a particle of mass $m$ confined in a 3D rectangular box with infinitely high walls. Let the box dimensions be $L_x, L_y, L_z$:

$$
0 < x < L_x, \quad 0 < y < L_y, \quad 0 < z < L_z
$$

The potential energy is defined as:

$$
V(x,y,z) =
\begin{cases}
0, & 0 < x < L_x, 0 < y < L_y, 0 < z < L_z \\
\infty, & \text{otherwise}
\end{cases}
$$

**Physical meaning:** The particle cannot exist outside the box, so the wavefunction must vanish at the boundaries.

---

## 2. Time-Independent Schrödinger Equation (TISE)

Inside the box ($V=0$), the time-independent Schrödinger equation is:

$$
-\frac{\hbar^2}{2m} \nabla^2 \psi(x,y,z) = E \psi(x,y,z)
$$

or equivalently:

$$
\nabla^2 \psi + k^2 \psi = 0, \quad \text{where} \quad k^2 = \frac{2 m E}{\hbar^2}
$$

with the Laplacian operator:

$$
\nabla^2 = \frac{\partial^2}{\partial x^2} + 
            \frac{\partial^2}{\partial y^2} +
            \frac{\partial^2}{\partial z^2}
$$

---

## 3. Boundary Conditions

Since $V = \infty$ outside the box, the wavefunction must vanish at the walls:

$$
\psi(0,y,z) = \psi(L_x,y,z) = 0
$$
$$
\psi(x,0,z) = \psi(x,L_y,z) = 0
$$
$$
\psi(x,y,0) = \psi(x,y,L_z) = 0
$$

This ensures standing-wave solutions in each direction.

---

## 4. Separation of Variables

Assume a product solution:

$$
\psi(x,y,z) = X(x) \, Y(y) \, Z(z)
$$

Substituting into the TISE gives:

$$
\frac{X''(x)}{X(x)} + \frac{Y''(y)}{Y(y)} + \frac{Z''(z)}{Z(z)} + k^2 = 0
$$

Each term depends on only one variable, so we introduce separation constants:

$$
\frac{X''}{X} = -k_x^2, \quad
\frac{Y''}{Y} = -k_y^2, \quad
\frac{Z''}{Z} = -k_z^2
$$

with the constraint:

$$
k^2 = k_x^2 + k_y^2 + k_z^2
$$

This yields three 1D differential equations:

$$
X'' + k_x^2 X = 0, \quad
Y'' + k_y^2 Y = 0, \quad
Z'' + k_z^2 Z = 0
$$

---

## 5. One-Dimensional Solutions and Quantization

The general solution of each equation is:

$$
X(x) = A_x \sin(k_x x) + B_x \cos(k_x x)
$$
$$
Y(y) = A_y \sin(k_y y) + B_y \cos(k_y y)
$$
$$
Z(z) = A_z \sin(k_z z) + B_z \cos(k_z z)
$$

**Apply boundary conditions:**

- $X(0)=0 \implies B_x = 0 \implies X(x) = A_x \sin(k_x x)$
- $X(L_x)=0 \implies \sin(k_x L_x) = 0 \implies k_x = \frac{n_x \pi}{L_x}, \ n_x=1,2,3,\dots$
- Similarly:

$$
k_y = \frac{n_y \pi}{L_y}, \quad k_z = \frac{n_z \pi}{L_z}
$$

Thus, the wavefunctions in each direction are:

$$
X(x) = A_x \sin\left(\frac{n_x \pi x}{L_x}\right), \quad
Y(y) = A_y \sin\left(\frac{n_y \pi y}{L_y}\right), \quad
Z(z) = A_z \sin\left(\frac{n_z \pi z}{L_z}\right)
$$

---

## 6. Full 3D Wavefunction

Multiplying the separable solutions:

$$
\psi_{n_x n_y n_z}(x,y,z) = A \,
\sin\left(\frac{n_x \pi x}{L_x}\right) \,
\sin\left(\frac{n_y \pi y}{L_y}\right) \,
\sin\left(\frac{n_z \pi z}{L_z}\right)
$$

where $A = A_x A_y A_z$ is the normalization constant.

---

## 7. Quantized Energies

Using $k^2 = 2 m E / \hbar^2$:

$$
\frac{2 m E_{n_x n_y n_z}}{\hbar^2} = 
k_x^2 + k_y^2 + k_z^2
$$

Substitute the quantized $k$’s:

$$
E_{n_x n_y n_z} = \frac{\hbar^2 \pi^2}{2 m} 
\left( \frac{n_x^2}{L_x^2} + \frac{n_y^2}{L_y^2} + \frac{n_z^2}{L_z^2} \right)
$$

For a cubic box $L_x = L_y = L_z = L$:

$$
E_{n_x n_y n_z} = \frac{\hbar^2 \pi^2}{2 m L^2} ( n_x^2 + n_y^2 + n_z^2 )
$$

---

## 8. Normalization of the Wavefunction

Normalization requires:

$$
\int_0^{L_x} \int_0^{L_y} \int_0^{L_z} |\psi|^2 dx\,dy\,dz = 1
$$

Using separability and:

$$
\int_0^L \sin^2\left(\frac{n \pi x}{L}\right) dx = \frac{L}{2}
$$

We find:

$$
|A|^2 \frac{L_x L_y L_z}{8} = 1 \implies A = \sqrt{\frac{8}{L_x L_y L_z}}
$$

Thus, the **normalized wavefunction** is:

$$
\boxed{
\psi_{n_x n_y n_z}(x,y,z) =
\sqrt{\frac{8}{L_x L_y L_z}} \,
\sin\left(\frac{n_x \pi x}{L_x}\right) \,
\sin\left(\frac{n_y \pi y}{L_y}\right) \,
\sin\left(\frac{n_z \pi z}{L_z}\right)
}
$$

with $n_x, n_y, n_z = 1,2,3,\dots$

---

## 9. Time-Dependent Stationary States

A stationary energy eigenstate evolves in time as:

$$
\Psi_{n_x n_y n_z}(x,y,z,t) = \psi_{n_x n_y n_z}(x,y,z) 
\, e^{-i E_{n_x n_y n_z} t / \hbar}
$$

The **probability density** is:

$$
|\Psi(x,y,z,t)|^2 = |\psi(x,y,z)|^2
$$

Hence, these are **bound stationary states**.

---

## 10. Nodes and Visualization

- Nodes occur where any sine factor is zero:

$$
\sin\left(\frac{n_x \pi x}{L_x}\right) = 0 \implies x = 0, \frac{L_x}{n_x}, \dots, L_x
$$

- Ground state $(1,1,1)$: no internal nodes.
- Excited state $(2,1,1)$: one nodal plane at $x = L_x/2$.
- In 3D plots:
  - $\psi$ shows sign (positive/negative)
  - $|\psi|^2$ shows lobes of probability

---

## Code
```
import numpy as np
import plotly.graph_objects as go


L = 1.0
N = 50  # grid resolution
x = np.linspace(0, L, N)
y = np.linspace(0, L, N)
z = np.linspace(0, L, N)
X, Y, Z = np.meshgrid(x, y, z, indexing='ij')

nx, ny, nz = 2, 1, 1

psi = np.sqrt(8 / L**3) * np.sin(nx*np.pi*X/L) * np.sin(ny*np.pi*Y/L) * np.sin(nz*np.pi*Z/L)

fig = go.Figure()

# Positive lobes
fig.add_trace(go.Isosurface(
    x=X.flatten(),
    y=Y.flatten(),
    z=Z.flatten(),
    value=psi.flatten(),
    isomin=0.3*np.max(psi),
    isomax=np.max(psi),
    surface_count=1,
    colorscale='Reds',
    opacity=0.6,
    caps=dict(x_show=False, y_show=False, z_show=False),
    name='ψ > 0'
))

# Negative lobes
fig.add_trace(go.Isosurface(
    x=X.flatten(),
    y=Y.flatten(),
    z=Z.flatten(),
    value=psi.flatten(),
    isomin=np.min(psi),
    isomax=-0.3*np.max(psi),
    surface_count=1,
    colorscale='Blues',
    opacity=0.6,
    caps=dict(x_show=False, y_show=False, z_show=False),
    name='ψ < 0'
))

# Layout
fig.update_layout(
    title=f"3D Standing Wave ψ(x,y,z) for state ({nx},{ny},{nz})",
    scene=dict(
        xaxis_title='x',
        yaxis_title='y',
        zaxis_title='z',
        aspectratio=dict(x=1, y=1, z=1)
    )
)

fig.show()

```

## Output

```
[Interactive 3D Wavefunction](wavefunction_3D.html)
```
