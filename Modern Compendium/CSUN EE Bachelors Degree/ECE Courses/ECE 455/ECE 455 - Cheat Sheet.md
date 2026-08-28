#Clean #CheatSheet
[[ECE 455 - Dirty Notes]]

> [!info] Lecture PDFs
> [[L1-ComplexVariables.pdf]] — Complex Variables
> [[L2-ComplexIntegration.pdf]] — Complex Integration

# ECE 455 — Cheat Sheet

---

> [!abstract] Complex Number Forms
> **Rectangular**
> $$z = x + iy$$
> **Polar**
> $$z = r(\cos\theta + i\sin\theta) = re^{i\theta}$$
> **Magnitude**
> $$r = |z| = \sqrt{x^2 + y^2}$$
> **Argument**
> $$\theta = \tan^{-1}\left(\frac{y}{x}\right), \quad \theta \in (-\pi, \pi]$$

---

> [!abstract] Complex Conjugate
> $$\bar{z} = x - iy \qquad \text{(polar: } re^{-i\theta}\text{)}$$
>
> **Identities**
> $$z + \bar{z} = 2x$$
> $$z - \bar{z} = 2iy$$
> $$z \cdot \bar{z} = x^2 + y^2 = r^2$$

---

> [!abstract] Algebraic Operations — Rectangular
> $$z_1 \pm z_2 = (x_1 \pm x_2) + i(y_1 \pm y_2)$$
> $$z_1 z_2 = (x_1x_2 - y_1y_2) + i(x_1y_2 + x_2y_1)$$
> $$\frac{z_1}{z_2} = \frac{x_1x_2 + y_1y_2}{x_2^2+y_2^2} + i\frac{x_2y_1 - x_1y_2}{x_2^2+y_2^2}$$

---

> [!abstract] Algebraic Operations — Polar
> **Multiply** — multiply magnitudes, add angles
> $$z_1z_2 = r_1r_2\,e^{i(\theta_1+\theta_2)}$$
> **Divide** — divide magnitudes, subtract angles
> $$\frac{z_1}{z_2} = \frac{r_1}{r_2}\,e^{i(\theta_1-\theta_2)}$$
> **Power (De Moivre's Theorem)**
> $$z^n = r^n e^{in\theta} = r^n(\cos n\theta + i\sin n\theta)$$
> **Equality**
> $$r_1 = r_2 \quad \text{and} \quad \theta_1 = \theta_2 + 2k\pi$$
>
> > [!tip] Addition/subtraction in polar → convert to rectangular first

---

> [!abstract] nth Roots of z
> $$w_k = r^{1/n}\left(\cos\frac{\theta+2k\pi}{n} + i\sin\frac{\theta+2k\pi}{n}\right), \quad k=0,1,\dots,n-1$$
>
> Produces $n$ equally spaced roots on a circle of radius $r^{1/n}$

---

> [!tip] Triangle Inequality
> $$|z_1 + z_2| \leq |z_1| + |z_2|$$
> Comes up frequently in integration proofs.

---

> [!abstract] Sets in the Complex Plane
> **Neighborhood of $z_0$** — all $z$ with $|z - z_0| < \varepsilon$
>
> **Interior point** — neighborhood entirely inside the set
>
> **Boundary point** — every neighborhood has points inside AND outside
>
> **Exterior point** — neighborhood entirely outside the set
>
> **Connected set** — any two points joinable by line segments within the set

---

> [!abstract] Line Integration — Parametric Method
> $\int_C f(z)\,dz = \int_a^b f(z(t))\,z'(t)\,dt$
>
> **Steps**
> 1. Write $z(t) = x(t) + iy(t)$, $\quad a \leq t \leq b$
> 2. Find $f(z(t))$
> 3. Find $dz = z'(t)\,dt$
> 4. Compute and solve
>
> **Cartesian Method**
> ```tikz
> \begin{document}
> \begin{tikzpicture}[>=stealth, scale=1.2]
>     \draw[->, thick] (-3,-0.2) -- (5,0) node[right] {Re};
>     \draw[->, thick] (0,-1.2) -- (0,3) node[above] {Im};
>     \draw[thick]
>         (-1.4,1.2)
>         .. controls (-0.8,2.1) and (0.6,2.6) .. (1.4,2.4)
>         .. controls (2.3,2.1) and (2.8,1.0) .. (3.3,0.8)
>         .. controls (3.8,0.6) and (4.0,1.2) .. (4.5,1.5);
>     \draw[->, thick] (2.15,1.75) -- (2.45,1.45);
>     \fill (-1.4,1.2) circle (2pt) node[below] {$z_0$};
>     \fill (-1.0,1.65) circle (2pt) node[below] {$z_1$};
>     \fill (0.4,2.35) circle (2pt);
>     \fill (1.4,2.4) circle (2pt);
>     \fill (4.1,1.2) circle (2pt) node[below] {$z_{n-1}$};
>     \fill (4.5,1.5) circle (2pt) node[right] {$z_n$};
>     \node at (0.95,2.15) {$\Delta z$};
>     \node at (2.15,1.2) {$C$};
> \end{tikzpicture}
> \end{document}
> ```
>
> **Parametric Method**
> ```tikz
> \begin{document}
> \begin{tikzpicture}[>=stealth, scale=1.3]
>     \draw[->, thick] (-2.5,0) -- (4.8,0) node[right] {Re};
>     \draw[->, thick] (0,-1.2) -- (0,2.8) node[above] {Im};
>     \draw[thick]
>         (-0.9,1.2)
>         .. controls (-0.4,2.0) and (0.6,2.3) .. (1.0,2.1)
>         .. controls (1.7,1.8) and (2.2,0.9) .. (2.8,0.8)
>         .. controls (3.3,0.7) and (3.6,1.1) .. (4.0,1.3);
>     \draw[->, thick] (2.0,1.35) -- (2.35,1.0);
>     \fill (-0.9,1.2) circle (2pt);
>     \fill (4.0,1.3) circle (2pt);
>     \node[left] at (-0.9,1.2) {$z_0=x(a)+iy(a)$};
>     \node[right] at (4.0,1.3) {$z_n=x(b)+iy(b)$};
>     \node at (0.75,1.95) {$C$};
>     \node[right] at (1.35,1.8) {$z(t)=x(t)+iy(t)$};
> \end{tikzpicture}
> \end{document}
> ```

---

> [!abstract] Standard Parametric Curves
> **Line Segment** $(z_0 \to z_1)$
> $x(t) = (1-t)x_0 + tx_1$
> $y(t) = (1-t)y_0 + ty_1$
> $z(t) = x(t) + iy(t), \quad 0 \leq t \leq 1$
> ```tikz
> \begin{document}
> \begin{tikzpicture}[>=stealth, scale=0.45]
>     \draw[step=1, very thin, gray!35] (-14,-11) grid (14,11);
>     \draw[->, thick] (-14,0) -- (14.5,0);
>     \draw[->, thick] (0,-11) -- (0,11.5);
>     \draw[thick, ->] (0,0) -- (8,6);
>     \fill (0,0) circle (3pt);
>     \fill (8,6) circle (3pt);
>     \node[below left] at (0,0) {$0$};
>     \node[above right] at (8,6) {$z_1=x_1+iy_1$};
>     \node[right] at (14.5,0) {Re};
>     \node[above] at (0,11.5) {Im};
> \end{tikzpicture}
> \end{document}
> ```
>
> **Circle CCW/CW** (radius $r$)
> $x(t) = r\cos t$
> $y(t) = \pm r\sin t$ — $+$ CCW, $-$ CW
> $z(t) = re^{\pm it}, \quad 0 \leq t \leq 2\pi$
> ```tikz
> \begin{document}
> \begin{tikzpicture}[>=stealth, scale=0.45]
>     \draw[step=1, very thin, gray!35] (-14,-11) grid (14,11);
>     \draw[->, thick] (-14,0) -- (14.5,0);
>     \draw[->, thick] (0,-11) -- (0,11.5);
>     \draw[thick] (0,0) circle (6);
>     \draw[->, thick] (4.2,4.2) -- (3.2,5.0);
>     \draw[dashed] (0,0) -- (6,0);
>     \node[above] at (3,0) {$\rho$};
>     \fill (0,0) circle (3pt);
>     \node[below left] at (0,0) {$0$};
>     \node[right] at (14.5,0) {Re};
>     \node[above] at (0,11.5) {Im};
> \end{tikzpicture}
> \end{document}
> ```
>
> **Ellipse CCW/CW**
> $x(t) = a\cos t$
> $y(t) = \pm b\sin t$ — $+$ CCW, $-$ CW
> $z(t) = a\cos t \pm ib\sin t, \quad 0 \leq t \leq 2\pi$
> ```tikz
> \begin{document}
> \begin{tikzpicture}[>=stealth, scale=0.45]
>     \draw[step=1, very thin, gray!35] (-14,-11) grid (14,11);
>     \draw[->, thick] (-14,0) -- (14.5,0);
>     \draw[->, thick] (0,-11) -- (0,11.5);
>     \draw[thick] (0,0) ellipse (8 and 5);
>     \draw[->, thick] (4.8,4.0) -- (3.8,4.5);
>     \fill (0,0) circle (3pt);
>     \node[below left] at (0,0) {$0$};
>     \node[above right] at (8,0) {$a$};
>     \node[above right] at (0,5) {$b$};
>     \node[right] at (14.5,0) {Re};
>     \node[above] at (0,11.5) {Im};
> \end{tikzpicture}
> \end{document}
> ```

---

> [!tip] ML Inequality
> $$\left|\int_C f(z)\,dz\right| \leq M \cdot L$$
> $M = \max|f(z)|$ on $C$, $\quad L$ = arc length of $C$
> Useful for bounding integrals without solving them directly.

---

> [!warning] Coming Up
> - Cauchy–Goursat Integral Theorem
> - Applications of Cauchy–Goursat
> - Cauchy's Integral Formula
