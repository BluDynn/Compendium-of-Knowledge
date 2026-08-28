#Clean
[[Electrical Computer Engineering]]
[[ECE 455 - Dirty Notes]]

# ECE 455 — Mathematical Models in Electrical Engineering
## Lecture 1 — Complex Variables

---

## Complex Numbers

### Rectangular Form

A complex number in rectangular (Cartesian) form is written as:

$$z = x + iy$$

where $x$ is the real part and $y$ is the imaginary part. This can be plotted on the complex plane with Re on the horizontal axis and Im on the vertical axis.

### Polar Form

In polar form, a complex number is expressed using Euler's Identity:

$$z = r \cdot e^{i\theta}$$

or equivalently:

$$z = r(\cos\theta + i\sin\theta)$$

where:

$$r = |z|, \qquad \theta = \tan^{-1}\left(\frac{y}{x}\right)$$

> [!tip] Prof. Valdi prefers radians. Note that $\theta$ (the Argument) is defined on $(-\pi, \pi]$ — capital A matters.

---

## Complex Conjugate

For any complex number $z = x + iy$, its conjugate $\bar{z}$ flips the sign of the imaginary part:

$$\bar{z} = x - iy$$

### Key Conjugate Identities

$$z + \bar{z} = 2x$$

$$z - \bar{z} = 2iy$$

$$z \cdot \bar{z} = x^2 + y^2$$

In polar form, the conjugate inverts the phase angle:

$$\overline{re^{i\theta}} = re^{-i\theta}$$

---

## Algebraic Operations — Rectangular Form

Let $z_1 = x_1 + iy_1$ and $z_2 = x_2 + iy_2$.

### Addition & Subtraction

$$z_1 \pm z_2 = (x_1 \pm x_2) + i(y_1 \pm y_2)$$

### Multiplication

$$z_1 \times z_2 = (x_1 x_2 - y_1 y_2) + i(x_1 y_2 + x_2 y_1)$$

### Division

$$\frac{z_1}{z_2} = \frac{x_1 x_2 + y_1 y_2}{x_2^2 + y_2^2} + i\,\frac{x_2 y_1 - x_1 y_2}{x_2^2 + y_2^2}$$

> [!note] Complex numbers obey the same fundamental algebraic laws as real numbers (commutativity, associativity, distributivity).

---

## Algebraic Operations — Polar Form

Let $z_1 = r_1 e^{i\theta_1}$ and $z_2 = r_2 e^{i\theta_2}$.

### Multiplication

$$z_1 z_2 = r_1 r_2\,e^{i(\theta_1 + \theta_2)}$$

Multiply magnitudes, **add** angles.

### Division

$$\frac{z_1}{z_2} = \frac{r_1}{r_2}\,e^{i(\theta_1 - \theta_2)}$$

Divide magnitudes, **subtract** angles.

### Integer Powers — De Moivre's Theorem

$$z^n = r^n\,e^{in\theta} = r^n(\cos n\theta + i\sin n\theta)$$

### Addition/Subtraction in Polar Form

Polar form does **not** simplify addition. Convert to rectangular form first, add real and imaginary parts separately, then convert back if needed.

### Equality

$z_1 = z_2$ if and only if $r_1 = r_2$ and $\theta_1 = \theta_2 + 2k\pi$ for some $k \in \mathbb{Z}$.

---

## Roots of Complex Numbers

Given $w^n = z$, the $n$ distinct $n$th roots are:

$$w_k = r^{1/n}\left(\cos\left(\frac{\theta + 2k\pi}{n}\right) + i\sin\left(\frac{\theta + 2k\pi}{n}\right)\right), \quad k = 0, 1, \dots, n-1$$

These roots are equally spaced around a circle of radius $r^{1/n}$ in the complex plane.

---

## Triangle Inequality

$$|z_1 + z_2| \leq |z_1| + |z_2|$$

> [!warning] This comes up frequently in integration proofs. Keep it in mind.

---

## Sets and Topology in the Complex Plane

| Term | Definition |
|---|---|
| **Neighborhood of $z_0$** | All $z$ satisfying $\|z - z_0\| < \varepsilon$ for some $\varepsilon > 0$ |
| **Interior Point** | There exists a neighborhood of $z_0$ entirely within the set |
| **Boundary Point** | Every neighborhood of $z_0$ contains points both inside and outside the set |
| **Exterior Point** | There exists a neighborhood of $z_0$ entirely outside the set |
| **Connected Set** | Any two points in the set can be joined by line segments lying entirely within the set |

### Complex Function, Domain, and Range

A complex function $w = f(z)$ maps from a domain $D \subseteq \mathbb{C}$ to a range in $\mathbb{C}$. The concepts of domain, range, and mapping follow the same algebraic logic as real-valued functions — just extended to the complex plane.

---

## Lecture 2 — Complex Integration

---

## Line Integration

A line integral over a curve $C$ in the complex plane yields a complex-valued result.

### Notation

$$\int_C f(z)\,dz \approx \sum_{k=1}^{n} f(\zeta_k)\,\Delta z_k, \qquad \Delta z_k = \Delta x_k + i\Delta y_k$$

### Parametric Method (Preferred)

**Step 1 —** Represent path $C$ parametrically:

$$z(t) = x(t) + iy(t) \quad \text{or} \quad z(t) = r(t)e^{i\theta(t)}, \qquad a \leq t \leq b$$

**Step 2 —** Substitute $z(t)$ into the integrand: $f(z(t))$

**Step 3 —** Compute $dz = z'(t)\,dt$

**Step 4 —** Evaluate:

$$\int_C f(z)\,dz = \int_a^b f(z(t))\,z'(t)\,dt$$

---

## Standard Parametric Curves

### Line Segment from $(x_0, y_0)$ to $(x_1, y_1)$

$$x(t) = (1-t)x_0 + tx_1, \qquad y(t) = (1-t)y_0 + ty_1, \qquad 0 \leq t \leq 1$$

$$z(t) = x(t) + iy(t)$$

### Circle of Radius $r$ Centered at Origin

| Direction | Parametrization |
|---|---|
| Counterclockwise | $z(t) = re^{it},\quad 0 \leq t \leq 2\pi$ |
| Clockwise | $z(t) = re^{-it},\quad 0 \leq t \leq 2\pi$ |

### Ellipse $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$

| Direction | Parametrization |
|---|---|
| Counterclockwise | $z(t) = a\cos t + ib\sin t,\quad 0 \leq t \leq 2\pi$ |
| Clockwise | $z(t) = a\cos t - ib\sin t,\quad 0 \leq t \leq 2\pi$ |

---

## ML Inequality

$$\left|\int_C f(z)\,dz\right| \leq M \cdot L$$

where $M = \max|f(z)|$ along $C$ and $L$ is the arc length of $C$.

> [!tip] Useful for bounding integrals without computing them directly.

---

## Topics Ahead

> [!abstract] Upcoming
> - Cauchy–Goursat Integral Theorem
> - Applications of the Cauchy–Goursat Theorem
> - Cauchy's Integral Formula

---

*Linked from: [[ECE 455 - Dirty Notes]]*
