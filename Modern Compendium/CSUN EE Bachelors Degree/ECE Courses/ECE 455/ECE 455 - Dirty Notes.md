[[Electrical Computer Engineering]]

# Lec 1  [[L1-ComplexVariables.pdf]]
---
---

# Day 1 - Date

---




"Complex plane Calculus"

![[Complex Numbers]]

![[Complex Conjugate]]

## Algebraic Operations - Rectangular Form 

$$\begin{aligned}
\text{let $z_1$ = ... and $z_2$ = ...}\\\\\text{Sum}&\\
z_1 + z_2 &= (x_1+iy_1)+(x_2+iy_2) &&=  (x_1+x_2 )+ i(y_1+y_2 )\\
z_1 - z_2 &= (x_1+iy_1)-(x_2+iy_2) &&=  (x_1-x_2 )+ i(y_1-y_2 )\\
\\\text{Product and Division}&\\
z_1 \times z_2& = (x_1+iy_1)(x_2+iy_2) &&=  (x_1x_2-y_1y_2)+ i(x_1y_2+x_2y_1 )\\
\frac{z_1}{z_2} &= long~ass~derivation &&= \frac{x_{1}x_{2}+y_{1}y_{2}}{x_{2}^2+y_{2}^2} +i~\frac{x_{2}y_{1}-x_{1}y_{2}}{x_{2}^2+y_{2}^2}




\end{aligned}
$$

## Applications of Complex Conjugate

Algebraic Operations of the Complex Conjugate
$$ \begin{align}
z+\bar{z} &= 2x \\
z-\bar{z} &= 2y ~i \\
z*\bar{z} &= x^2 +y^2 \\

\end{align}
$$

## Examples

#Example #Prompt #ECEXXX
>[!warning]- Example Problem: 
>![[Pasted image 20260527135924.png]]
>![[Pasted image 20260527140002.png]]
>![[Pasted image 20260527140038.png]]
>![[Pasted image 20260527140054.png]]
>![[Pasted image 20260527140108.png]]

## Fundamental Laws 
![[Pasted image 20260527140537.png]]
I was gonna write it out but its just common algebra, you should just mentally keep it as "complex numbers act under the same laws as most functions" 

> [!Quote] At this point I went ahead of the class s notes are a bit odd 
 
## Graphical Representation 

| ![[Pasted image 20260527140741.png]] | ![[Pasted image 20260527140732.png\|312]] |     |
| ------------------------------------ | ----------------------------------------- | --- |
|                                      |                                           |     |
|                                      |                                           |     |
> [!Quote] Argument(z)
>  Argument(z)
 >  "emphasis on the capital A"
>  - just know that theta is between  $-\pi$  and $\pi$  


## Polar Forms
![[Pasted image 20260527140828.png|421]]


#Example #Prompt #ECEXXX
>[!warning]- Example Problem: 
>![[Pasted image 20260527140857.png]]
>![[Pasted image 20260527140904.png]]



[[Complex Conjugate]] - check the Polar form lmao my format is broken

### Triangle Inequality 
![[Pasted image 20260527141332.png]]
comes up when integrating :(


i asked chat and they did this ... 
![[Pasted image 20260527141601.png|350]]

> [!abstract]- Algebraic Operations - Polar Form
>
> Take
>
> $$
> z_1 = r_1(\cos\theta_1 + i\sin\theta_1)
> $$
>
> and
>
> $$
> z_2 = r_2(\cos\theta_2 + i\sin\theta_2)
> $$
>
> ---
>
> ### Equality
>
> If
>
> $$
> z_1 = z_2
> $$
>
> then:
>
> $$
> r_1 = r_2
> $$
>
> and
>
> $$
> \theta_1 = \theta_2 + 2k\pi
> \quad \text{for } k \in \mathbb{Z}
> $$
>
> because angles repeat every \(2\pi\).
>
> ---
>
> ### Addition
>
> Addition in polar form is NOT as clean as multiplication.
>
> Start by converting to rectangular form:
>
> $$
> z_1 = r_1\cos\theta_1 + i r_1\sin\theta_1
> $$
>
> $$
> z_2 = r_2\cos\theta_2 + i r_2\sin\theta_2
> $$
>
> Add real and imaginary parts separately:
>
> $$
> z_1 + z_2
> =
> (r_1\cos\theta_1 + r_2\cos\theta_2)
> +
> i(r_1\sin\theta_1 + r_2\sin\theta_2)
> $$
>
> ---
>
> ### Subtraction
>
> Similarly:
>
> $$
> z_1 - z_2
> =
> (r_1\cos\theta_1 - r_2\cos\theta_2)
> +
> i(r_1\sin\theta_1 - r_2\sin\theta_2)
> $$
>
> ---
>
> ### Multiplication
>
> This is where polar form becomes powerful.
>
> Start with:
>
> $$
> z_1z_2
> =
> r_1(\cos\theta_1+i\sin\theta_1)
> \cdot
> r_2(\cos\theta_2+i\sin\theta_2)
> $$
>
> Factor magnitudes:
>
> $$
> =
> r_1r_2
> (\cos\theta_1+i\sin\theta_1)
> (\cos\theta_2+i\sin\theta_2)
> $$
>
> Using trig identities:
>
> $$
> \cos(A+B)
> =
> \cos A \cos B - \sin A \sin B
> $$
>
> $$
> \sin(A+B)
> =
> \sin A \cos B + \cos A \sin B
> $$
>
> we get:
>
> $$
> z_1z_2
> =
> r_1r_2
> \left(
> \cos(\theta_1+\theta_2)
> +
> i\sin(\theta_1+\theta_2)
> \right)
> $$
>
> ---
>
> ### Integer Powers (De Moivre's Theorem)
>
> Let
>
> $$
> z = r(\cos\theta+i\sin\theta)
> $$
>
> Then:
>
> $$
> z^n
> =
> r^n
> \left(
> \cos(n\theta)
> +
> i\sin(n\theta)
> \right)
> $$
>
> This works because multiplication adds angles repeatedly.
>
> Example:
>
> $$
> z^3
> =
> r^3
> \left(
> \cos(3\theta)
> +
> i\sin(3\theta)
> \right)
> $$
>
> ---
>
> ### Division
>
> Start with:
>
> $$
> \frac{z_1}{z_2}
> =
> \frac{
> r_1(\cos\theta_1+i\sin\theta_1)
> }{
> r_2(\cos\theta_2+i\sin\theta_2)
> }
> $$
>
> Separate magnitudes:
>
> $$
> =
> \frac{r_1}{r_2}
> \cdot
> \frac{
> \cos\theta_1+i\sin\theta_1
> }{
> \cos\theta_2+i\sin\theta_2
> }
> $$
>
> Using angle subtraction identities:
>
> $$
> \frac{z_1}{z_2}
> =
> \frac{r_1}{r_2}
> \left(
> \cos(\theta_1-\theta_2)
> +
> i\sin(\theta_1-\theta_2)
> \right)
> $$
>
> ---
>
> ### Key Pattern to Remember
>
> Polar form turns:
>
> - multiplication → multiply magnitudes, add angles
> - division → divide magnitudes, subtract angles
> - powers → raise magnitude, multiply angle
>
> That’s why engineers LOVE polar form.


#Example #Prompt #ECEXXX
>[!warning]- Example Problem: 
>![[Pasted image 20260527144019.png]]
>![[Pasted image 20260527144031.png]]


## Root of Complex Numbers

> [!abstract] Root of Complex Numbers
>
> Given
>
> $$
> w^n = z
> $$
>
> then
>
> $$
> w = z^{\frac{1}{n}}
> $$
>
> is referred to as the \(n\)th root of \(z\).

now what does this mean ... 

utilizing chat i found this equation for calculations. 

---
## \(n\)th Root Formula

If

$$
z = r(\cos\theta+i\sin\theta)
$$

then the \(n\)th roots of \(z\) are:

$$
w_k
=
r^{1/n}
\left(
\cos\left(\frac{\theta+2k\pi}{n}\right)
+
i\sin\left(\frac{\theta+2k\pi}{n}\right)
\right)
$$

where

$$
k = 0,1,2,\dots,n-1
$$

---

These can be plotted as they contain a magnitude and angle btw


## Complex Set, Function, Domain and Range 

### Complex Set

> [!abstract]+ Neighborhoods and Sets in Complex Analysis
>
>
> ### Neighborhood of \(z_0\)
>
> All points \(z\) that satisfy:
>
> $$
 |z-z_0|<\varepsilon
 \quad \text{where } \varepsilon>0 $$
>
> ---
>
> ### Interior Points of a Set
>
> Points for which there exists at least a neighborhood of \(z_0\) all whose points belong to that set.
>
> ---
>
> ### Boundary Points of a Set
>
> Points for which every neighborhood of \(z_0\) contains points that belong to that set as well as points that do not belong to that set.
>
> ---
>
> ### Exterior Points of a Set
>
> Points for which there exists at least a neighborhood of \(z_0\) none of whose points belong to that set.
>
> ---
>
> ### Connected Set
>
> A set such that any two points of the set can be connected by a number of line segments all belonging to the set.
> ![[Pasted image 20260527150437.png]]
> ![[Pasted image 20260527150503.png]]

#### Complex Function 
![[Pasted image 20260527153717.png]]
#### Domain And Range 
![[Pasted image 20260527153754.png]]

### CSFDR - TL;DR
literally the same algebra concepts in complex context

--- 

END OF LECTURE - Study For Quiz $\uparrow$

---
# Self Notes Forward -- 
## Limit, Continuity, Derivative, and Analytic Function 
### Limit - // cur ahead wait for prof - 
first glance seems just like normal limits
nah nvm i go text book 

--- 
# Day 2
I fucking missed class -\_-

## Self notes mid lecture

>[!error]+ # Missed Conccepts cuz youre dummy stupid for missing class
> ### Limit
> ### Continuity 
> ### Derivative
> ### Analytic Function
> ## Cauchy-Riemann Equations and Laplace's Harmonic Functions
> ## Exponential and Logarithmic Functions
> ### Complex Power
> ## Trigonometric and Inverse Trigonometric Functions
> ## Hyperbolic and Inverse Hyperbolic Functions



---

# Lec 2 - [[L2-ComplexIntegration.pdf]]

---

# Day 3 
Algebra done and derivatives done moving onto integrals
## Line Integration
With the properties of line integrals, when given a curve in the complex plane the integral of the line will be given in a complex value.

### Notation and derivation
$$
\begin{align}
	 \int_{C} \to \text{Integral along curve C}  \\
	 
\underset{C}{\int_{z_{0}}^{ z_{n} }}f(z)dz \approx \sum^n_{k=1}f(\Delta z_{k}\cdot \Delta z_{k})
 \\ \text{knowing that ...} \\
 \Delta z_{k} = \Delta x_{k}+i\Delta y_{k} \\
  \\
 = \sum^n_{k=1}
\end{align}
	 
$$

### Cartesian Method of Line Integration 
```tikz
\begin{document}
\begin{tikzpicture}[>=stealth, scale=1.2]
    \draw[->, thick] (-3,-0.2) -- (5,0) node[right] {Re};
    \draw[->, thick] (0,-1.2) -- (0,3) node[above] {Im};

    \draw[thick]
        (-1.4,1.2)
        .. controls (-0.8,2.1) and (0.6,2.6) .. (1.4,2.4)
        .. controls (2.3,2.1) and (2.8,1.0) .. (3.3,0.8)
        .. controls (3.8,0.6) and (4.0,1.2) .. (4.5,1.5);

    \draw[->, thick] (2.15,1.75) -- (2.45,1.45);

    \fill (-1.4,1.2) circle (2pt) node[below] {$z_0$};
    \fill (-1.0,1.65) circle (2pt) node[below] {$z_1$};
    \fill (0.4,2.35) circle (2pt);
    \fill (1.4,2.4) circle (2pt);
    \fill (4.1,1.2) circle (2pt) node[below] {$z_{n-1}$};
    \fill (4.5,1.5) circle (2pt) node[right] {$z_n$};

    \node at (0.95,2.15) {$\Delta z$};
    \node at (2.15,1.2) {$C$};
\end{tikzpicture}
\end{document}
```
### Parametric Method of Line Integration
```tikz
\begin{document}
\begin{tikzpicture}[>=stealth, scale=1.3]

    % Axes
    \draw[->, thick] (-2.5,0) -- (4.8,0) node[right] {Re};
    \draw[->, thick] (0,-1.2) -- (0,2.8) node[above] {Im};

    % Parametric path
    \draw[thick]
        (-0.9,1.2)
        .. controls (-0.4,2.0) and (0.6,2.3) .. (1.0,2.1)
        .. controls (1.7,1.8) and (2.2,0.9) .. (2.8,0.8)
        .. controls (3.3,0.7) and (3.6,1.1) .. (4.0,1.3);

    % Direction arrow
    \draw[->, thick] (2.0,1.35) -- (2.35,1.0);

    % Endpoints
    \fill (-0.9,1.2) circle (2pt);
    \fill (4.0,1.3) circle (2pt);

    % Labels
    \node[left] at (-0.9,1.2) {$z_0=x(a)+iy(a)$};
    \node[right] at (4.0,1.3) {$z_n=x(b)+iy(b)$};

    \node at (0.75,1.95) {$C$};
    \node[right] at (1.35,1.8) {$z(t)=x(t)+iy(t)$};

\end{tikzpicture}
\end{document}
```
1. First Represent path C in a parametric form z(t)
   $$\begin{align}
    &z(t) = x(t)+ iy(t) &\text{ or }&&z(t)=r(t)e^{i\theta(t)} && a\leq t\leq b 
   \end{align}
   	
   $$
1. Substitute z(t) in the intergrand f(z(t)) and obtain dz

### Curves Defined by Parametric Equations

> [!example]- Line Segment
>
> **Start**
>
> $$
> (x_0,y_0)
> $$
>
> **End**
>
> $$
> (x_1,y_1)
> $$
>
> **Parametrization**
>
> $
> x(t)=(1-t)x_0+tx_1
> $
>
> $
> y(t)=(1-t)y_0+ty_1
> $
>
> $
> 0\le t\le1
> $
>
> $
> z(t)=x(t)+iy(t)
> $


> [!example]- Circle (Radius $r$)
>
> **Equation**
>
> $$
> x^2+y^2=r^2
> $$
>
> **Counterclockwise**
>
> $$
> x(t)=r\cos t
> $$
>
> $$
> y(t)=r\sin t
> $$
>
> $$
> z(t)=r(\cos t+i\sin t)=re^{it}
> $$
>
> $$
> 0\le t\le 2\pi
> $$
>
> **Clockwise**
>
> $$
> x(t)=r\cos t
> $$
>
> $$
> y(t)=-r\sin t
> $$
>
> $$
> z(t)=r(\cos t-i\sin t)=re^{-it}
> $$
>
> $$
> 0\le t\le 2\pi
> $$
>
> **Path**
>
> Whole circle traversed once.

> [!example]- Ellipse
>
> **Equation**
>
> $$
> \frac{x^2}{a^2}+\frac{y^2}{b^2}=1
> $$
>
> **Counterclockwise**
>
> $$
> x(t)=a\cos t
> $$
>
> $$
> y(t)=b\sin t
> $$
>
> $$
> z(t)=a\cos t+i\,b\sin t
> $$
>
> $$
> 0\le t\le 2\pi
> $$
>
> **Clockwise**
>
> $$
> x(t)=a\cos t
> $$
>
> $$
> y(t)=-b\sin t
> $$
>
> $$
> z(t)=a\cos t-i\,b\sin t
> $$
>
> $$
> 0\le t\le 2\pi
> $$
>
> **Start Point**
>
> $$
> (a,0)
> $$
>
> **End Point**
>
> $$
> (a,0)
> $$
>
> **Path**
>
> Entire ellipse traversed once.

Example - Parametric Curve 
Parametric Representation for a line from z=0 to z1 = x1+iy1
```tikz
\begin{document}
\begin{tikzpicture}[>=stealth, scale=0.45]

    % Grid
    \draw[step=1, very thin, gray!35] (-14,-11) grid (14,11);

    % Axes
    \draw[->, thick] (-14,0) -- (14.5,0);
    \draw[->, thick] (0,-11) -- (0,11.5);

    % Line from origin to z1 = x1 + iy1
    \draw[thick, ->] (0,0) -- (8,6);

    % Points
    \fill (0,0) circle (3pt);
    \fill (8,6) circle (3pt);

    % Labels
    \node[below left] at (0,0) {$0$};
    \node[above right] at (8,6) {$z_1=x_1+iy_1$};

    % Axis labels
    \node[right] at (14.5,0) {Re};
    \node[above] at (0,11.5) {Im};

\end{tikzpicture}
\end{document}
```


Example Circle centered at 0 with radius $\rho$ in counter clockwise
```tikz
\begin{document}
\begin{tikzpicture}[>=stealth, scale=0.45]

    % Grid
    \draw[step=1, very thin, gray!35] (-14,-11) grid (14,11);

    % Axes
    \draw[->, thick] (-14,0) -- (14.5,0);
    \draw[->, thick] (0,-11) -- (0,11.5);

    % Circle
    \draw[thick] (0,0) circle (6);

    % Direction arrow (counterclockwise)
    \draw[->, thick] (4.2,4.2) -- (3.2,5.0);

    % Radius
    \draw[dashed] (0,0) -- (6,0);
    \node[above] at (3,0) {$\rho$};

    % Center
    \fill (0,0) circle (3pt);
    \node[below left] at (0,0) {$0$};

    % Axis labels
    \node[right] at (14.5,0) {Re};
    \node[above] at (0,11.5) {Im};

\end{tikzpicture}
\end{document}
```

semi circle c. clockwise 
[enter here]

ellispe z=0 with cart eq ...
```tikz
\begin{document}
\begin{tikzpicture}[>=stealth, scale=0.45]

    % Grid
    \draw[step=1, very thin, gray!35] (-14,-11) grid (14,11);

    % Axes
    \draw[->, thick] (-14,0) -- (14.5,0);
    \draw[->, thick] (0,-11) -- (0,11.5);

    % Ellipse centered at origin
    \draw[thick] (0,0) ellipse (8 and 5);

    % Direction arrow counterclockwise
    \draw[->, thick] (4.8,4.0) -- (3.8,4.5);

    % Center
    \fill (0,0) circle (3pt);
    \node[below left] at (0,0) {$0$};

    % Labels
    \node[above right] at (8,0) {$a$};
    \node[above right] at (0,5) {$b$};

    % Axis labels
    \node[right] at (14.5,0) {Re};
    \node[above] at (0,11.5) {Im};

\end{tikzpicture}
\end{document}
```

#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260603141406.png]]
>^[ECEXXX-ProblemTitle-Prompt]
> Steps 
> 1) Find z(t)
> 2) find dz/dt
> 3) find f(z(t))
> 4) Compute and Solve

z![[Pasted image 20260603142534.png]]

### ML inequality

magnitude of the lenght n sum shit


## Cauchy - Goursat Integral Theorem /Hard part/
> [!example]- Simple Closed Contour
>
> ```tikz
> \begin{document}
> \begin{tikzpicture}[>=stealth, scale=1.0]
>
>     % Axes
>     \draw[->, thick] (-2.5,0) -- (4.5,0) node[right] {Re};
>     \draw[->, thick] (0,-2.5) -- (0,2.5) node[above] {Im};
>
>     % Curve
>     \draw[thick]
>     (-1.3,0.6)
>     .. controls (-2.0,1.3) and (-0.6,1.8) ..
>     (0.5,1.5)
>     .. controls (1.8,1.2) and (2.7,0.6) ..
>     (3.0,0.0)
>     .. controls (2.8,-0.8) and (1.7,-1.5) ..
>     (1.1,-1.2)
>     .. controls (0.6,-0.8) and (-0.1,-0.8) ..
>     (-0.6,-1.5)
>     .. controls (-1.2,-2.2) and (-1.8,-0.6) ..
>     (-1.3,0.6);
>
>     \node[right] at (2.4,0.35) {$C$};
>
> \end{tikzpicture}
> \end{document}
> ```
>
> **Definition**
>
> A contour that:
>
> - Begins and ends at the same point.
> - Does not intersect itself.
>
> **Properties**
>
> - Closed: starting point = ending point.
> - Simple: no self-intersections.
> - Separates the complex plane into an interior and exterior region.
>
> **Examples**
>
> - Circles
> - Ellipses
> - Simple polygons
> - Smooth closed loops

> [!example]- Non-Simple Closed Contour
>
> ```tikz
> \begin{document}
> \begin{tikzpicture}[>=stealth, scale=1.0]
>
>     % Axes
>     \draw[->, thick] (-3,0) -- (4.2,0) node[right] {Re};
>     \draw[->, thick] (0,-2.5) -- (0,2.5) node[above] {Im};
>
>     % Non-simple closed contour
>     \draw[thick]
>     (-1.2,0.8)
>     .. controls (-2.2,1.2) and (-1.8,-0.3) ..
>     (-0.8,-1.2)
>     .. controls (-0.2,-2.0) and (-0.4,0.5) ..
>     (0.6,0.9)
>     .. controls (1.6,1.3) and (2.5,0.3) ..
>     (2.2,-1.2)
>     .. controls (2.0,-2.0) and (0.7,-1.0) ..
>     (-0.2,0.3)
>     .. controls (-0.8,1.1) and (-0.4,1.2) ..
>     (-1.2,0.8);
>
>     % Label
>     \node[right] at (2.6,0.4) {$C$};
>
> \end{tikzpicture}
> \end{document}
> ```
>
> **Definition**
>
> A closed contour that intersects itself or retraces part of its path.
>
> **Properties**
>
> - Starting point equals ending point.
> - Contains one or more self-intersections or repeated points.
> - Not a simple contour.
> - Does not separate the plane into a single interior and exterior region in the same way as a simple closed contour.
>
> **Examples**
>
> - Figure-eight curves
> - Self-intersecting loops
> - Contours that retrace part of their path



> [!example]- Simply Connected Domain
>
> ```tikz
> \begin{document}
> \begin{tikzpicture}[scale=0.9]
>
>     % Axes
>     \draw[->] (-3,0) -- (3.5,0) node[right] {Re};
>     \draw[->] (0,-2.5) -- (0,2.5) node[above] {Im};
>
>     % Domain
>     \fill[blue!40]
>     (-2,0.8)
>     .. controls (-2.4,2.0) and (2.0,1.8) ..
>     (2.2,0.5)
>     .. controls (2.4,-1.4) and (-1.8,-1.8) ..
>     (-2,-0.6)
>     .. controls (-2.2,0.0) and (-2.1,0.5) ..
>     (-2,0.8);
>
>     \draw[thick]
>     (-2,0.8)
>     .. controls (-2.4,2.0) and (2.0,1.8) ..
>     (2.2,0.5)
>     .. controls (2.4,-1.4) and (-1.8,-1.8) ..
>     (-2,-0.6)
>     .. controls (-2.2,0.0) and (-2.1,0.5) ..
>     (-2,0.8);
>
> \end{tikzpicture}
> \end{document}
> ```
>
> A domain with **no holes**.
>
> Any simple closed contour can be contracted to a point while remaining in the domain.


> [!example]- Not Simply Connected Domain
>
> ```tikz
> \begin{document}
> \begin{tikzpicture}[scale=0.9]
>
>     % Axes
>     \draw[->] (-3,0) -- (3.5,0) node[right] {Re};
>     \draw[->] (0,-2.5) -- (0,2.5) node[above] {Im};
>
>     % Outer boundary
>     \fill[blue!40, even odd rule]
>     (-2,0.8)
>     .. controls (-2.4,2.0) and (2.0,1.8) ..
>     (2.2,0.5)
>     .. controls (2.4,-1.4) and (-1.8,-1.8) ..
>     (-2,-0.6)
>     .. controls (-2.2,0.0) and (-2.1,0.5) ..
>     (-2,0.8)
>
>     (1,1) circle (0.6);
>
>     \draw[thick]
>     (-2,0.8)
>     .. controls (-2.4,2.0) and (2.0,1.8) ..
>     (2.2,0.5)
>     .. controls (2.4,-1.4) and (-1.8,-1.8) ..
>     (-2,-0.6)
>     .. controls (-2.2,0.0) and (-2.1,0.5) ..
>     (-2,0.8);
>
>     \draw[thick] (1,1) circle (0.6);
>
> \end{tikzpicture}
> \end{document}
> ```
>
> A domain containing **one hole**.
>
> Not every simple closed contour can be contracted to a point.


- - - 
End of Lec 3 - $\uparrow$ Exam 1 Content
- - - - 
# Day 4 - Start 
- - -
"as long as the function is analytic within the curve, the Cauchy-Goursat Theorem is usuable "

but how do we integrate when there is "holes inside the curve"

complex variables and numbers are infinitely differentiable - interesting


## Applications of Cauchy–Goursat Integral Theorem

### Partitioned Closed Paths
```tikz
\begin{document}
\begin{tikzpicture}[scale=1.15, >=stealth]

% shaded region
\fill[blue!30, opacity=0.85]
  (-3.0,-1.25)
  .. controls (-3.45,-0.5) and (-2.65,0.9) .. (-1.4,0.85)
  .. controls (-0.35,0.8) and (0.1,0.65) .. (0.95,0.95)
  .. controls (2.1,1.35) and (3.4,0.25) .. (3.35,-0.15)
  .. controls (3.25,-0.95) and (2.1,-1.25) .. (0.6,-0.85)
  .. controls (-0.45,-0.55) and (-1.2,-1.0) .. (-2.1,-1.35)
  .. controls (-2.6,-1.55) and (-2.85,-1.45) .. cycle;

% axes
\draw[->] (-3.6,0) -- (3.8,0) node[right] {Re};
\draw[->] (0,-1.55) -- (0,1.35) node[above] {Im};

% contour C
\draw[thick]
  (-2.1,-0.55)
  .. controls (-2.25,0.15) and (-1.25,0.15) .. (-0.45,0.15)
  .. controls (0.45,0.15) and (0.55,0.15) .. (1.05,0.55)
  .. controls (1.45,0.9) and (1.75,0.75) .. (2.05,0.35)
  -- (2.45,0.15)
  .. controls (1.55,-0.05) and (0.55,-0.25) .. (-0.45,-0.5)
  .. controls (-1.25,-0.7) and (-1.8,-0.85) .. (-2.1,-0.55);

% partition arrows
\draw[thick, ->] (-1.0,0.16) -- (-0.65,0.16);
\node at (-1.35,0.35) {$C_1$};

\draw[thick, ->] (1.0,-0.22) -- (1.25,-0.17);
\node at (1.45,-0.38) {$C_3$};

% labels
\node at (-2.25,-0.38) {$z_1$};
\node at (2.65,0.25) {$z_2$};

% caption
\node at (0,-1.95) {Figure 2.21 Closed Path $C$ -- Partitioned};

\end{tikzpicture}
\end{document}
```

"for$f(z)$ being analytic and $C$ being a simple closed path"
$$
	\begin{align}
	\oint f(z)dz=0 \\
	\oint f(z)dz =  \oint_{C_{1}} f(z)dz+ \oint_{C_{2}} f(z)dz = 0  \\
	 \oint_{C_{1}} f(z)dz~~=~~- \oint_{C_{2}} f(z)dz \\
	 \text{Implies Path Independance}
	\end{align}
$$

If f(z) is an analytic function everywhere in a simply connected domain of $D$ then 

$$
	\oint^{z_{2}}_{{z_{1}}} f(z)dz = F(z_{2})-F(z_{1})
	 
$$
where F(z) is defined as the antiderivative of f(z)

> [!tip] IMPORTANT RECAP - CHECKING ANALYITCS
>  To check if a funciton is analytic the two conditions must be checked
>  
>  $$
\begin{align}
u_{x} =v_{y} \\
u_{y} = -v_{x}
\end{align}
  $$

>[!bug] Remember Trig Identities

### Multiply Connected Domain 

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.05, >=stealth]

% --------------------
% Doubly connected domain D
% --------------------
\fill[blue!32, opacity=0.9]
  (-3.15,-0.95)
  .. controls (-2.75,0.65) and (-1.70,2.00) .. (-0.15,1.92)
  .. controls (1.35,1.85) and (3.00,0.90) .. (3.45,-0.15)
  .. controls (3.95,-1.35) and (2.55,-1.88) .. (0.35,-1.78)
  .. controls (-1.15,-1.72) and (-2.65,-1.45) .. (-3.15,-0.95);

\draw[blue!45!black, thick]
  (-3.15,-0.95)
  .. controls (-2.75,0.65) and (-1.70,2.00) .. (-0.15,1.92)
  .. controls (1.35,1.85) and (3.00,0.90) .. (3.45,-0.15)
  .. controls (3.95,-1.35) and (2.55,-1.88) .. (0.35,-1.78)
  .. controls (-1.15,-1.72) and (-2.65,-1.45) .. (-3.15,-0.95);

% --------------------
% Outer contour C2
% --------------------
\draw[thick]
  (-0.05,-0.55) ellipse [x radius=2.00, y radius=1.15];

% arrow on C2, bottom direction
\draw[thick, ->]
  (-0.20,-1.70) -- (0.18,-1.70);

% --------------------
% Inner contour C3
% --------------------
\draw[thick]
  (0.00,-0.25) ellipse [x radius=0.92, y radius=0.72];

% arrow on C3, clockwise direction
\draw[thick, ->]
  (0.28,-0.97) -- (-0.08,-0.97);

% --------------------
% Hole
% --------------------
\fill[white]
  (0.00,-0.25) ellipse [x radius=0.40, y radius=0.25];

\draw[blue!45!black, thick]
  (0.00,-0.25) ellipse [x radius=0.40, y radius=0.25];

% --------------------
% Cuts C_A and C_B
% --------------------
\draw[thick, ->] (-0.03,0.45) -- (-0.03,0.92);
\draw[thick, ->] (0.13,0.92) -- (0.13,0.45);

% --------------------
% Labels
% --------------------
\node[blue!35!black] at (-2.55,-0.55) {$D$};

\node[blue!35!black] at (-1.72,0.95) {$C_2$};

\node[blue!35!black] at (-1.05,-0.25) {$C_3$};

\node[blue!35!black] at (-0.28,0.55) {$C_B$};
\node[blue!35!black] at (0.36,0.72) {$C_A$};

% --------------------
% Integral
% --------------------
\node[align=center] at (-3.85,2.35) {$\displaystyle \oint_C f(z)\,dz = 0$};

% small C underneath, like the reference
\node at (-4.10,1.92) {$C$};

% --------------------
% Caption
% --------------------
\node at (0,-2.25) {Figure 2.24 Doubly Connected Domain};

\end{tikzpicture}
\end{document}
```
$$
\oint_C f(z)\,dz
=
\oint_{C_2} f(z)\,dz
+
\oint_{C_A} f(z)\,dz
+
\oint_{C_3} f(z)\,dz
+
\oint_{C_B} f(z)\,dz
$$

$$
\oint_{C_A} f(z)\,dz
+
\oint_{C_B} f(z)\,dz
=
0
$$
$$
\oint_C f(z)\,dz
=
\oint_{C_2} f(z)\,dz
+
\oint_{C_3} f(z)\,dz
$$
$$
\oint_C f(z)\,dz = 0,
$$
$$
\oint_{C_2} f(z)\,dz
+
\oint_{C_3} f(z)\,dz
=
0
$$
$$
\oint_{C_2} f(z)\,dz
=
-\oint_{C_3} f(z)\,dz
$$


## Cauchy's Integral Formula

- - -
Dude we fucked up and missed a bit of lectures 

Recap post 6/15 and 6/17 
Lec 3 -- chapters 15.1-15.5 & 16.1-16.4 
- - -


 
# Lec 3 -
- - - 
# Text book notes page 
697-> notability
## Ch 15  Overview - Power Series, Taylor
Chapter 14 covered the evaluation of complex integrals using cauchy's integral formulas from the cauchy integral theorem. Chapter 15 takes a different approach of evaluating complex integrals through **residue integration.** This requires knoweldge of ***Power series, Taylor series, and the Cauchy integral theorem.***

- 15.1 - convergence tests 
- 15.2 - Power series 
- 15.3 - Functions given by power series 
- 15.4 - Taylor Series
- 15.5 - uniform convergence 
15.1 and 15.2 are review sections, 15.3 and 15.4 are the key take aways, and 15.5 is there. 

## 15.1 Sequences Series and Convergence Tests 

>[!summary] 
>Important contents of this sections include a recap of sequences and series in the context of complex numbers. Key information to rewrite include but is not limited to...
>> Sequence Definition
>>> Sequences of real and imaginary parts
>> Serries Definition
>>> Series aof real and imaginary parts
>> Convergence and Divergence definitions in respect to sequences and series
>> Tests for convergence and Divergence in series
>>>> Definition 
>>>Cauchy's Convergence Principle
>>>>Absolute vs Conditionally Convergent Series
>>>Comparison Test 
>>>Geometric Series
>> Ratio test
>> Root Test

## 15.2 


>> 
