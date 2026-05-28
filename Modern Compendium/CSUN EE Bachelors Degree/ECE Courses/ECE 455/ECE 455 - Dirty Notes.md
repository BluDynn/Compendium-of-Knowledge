[[Electrical Computer Engineering]]

# Lec 1  [[L1-ComplexVariables.pdf]]


"Complex plane Calculus"

![[Complex Numbers]]

![[Complex Conjugate]]

## Algebraic Operations - Rectangular Form 

$$\begin{aligned}
\text{let $z_1$ = ... and $z_2$ = ...}\\\\\text{Sum}&\\
z_1 + z_2 &= (x_1+iy_1)+(x_2+iy_2) &&=  (x_1+x_2 )+ i(y_1+y_2 )\\
z_1 - z_2 &= (x_1+iy_1)-(x_2+iy_2) &&=  (x_1-x_2 )+ i(y_1-y_2 )\\
\\\text{Product and Division}&\\
z_1 \times z_2& = (x_1+iy_1)(x_2+iy_2) &&=  (x_1x_2)+ i(x_1y_2+x_2y_1 )+i^2y_1y_2\\
\frac{z_1}{z_2} &= \text{refer to red book purple text - involves CC.}




\end{aligned}
$$

## Applications of Complex Conjugate


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

>

```tikz
\usepackage{circuitikz}
\begin{document}

\begin{circuitikz}[american, voltage shift=0.5]
\draw (0,0)
to[isource, l=$I_0$, v=$V_0$] (0,3)
to[short, -*, i=$I_0$] (2,3)
to[R=$R_1$, i>_=$i_1$] (2,0) -- (0,0);
\draw (2,3) -- (4,3)
to[R=$R_2$, i>_=$i_2$]
(4,0) to[short, -*] (2,0);
\end{circuitikz}

\end{document}
```

```tikz
\usepackage{circuitikz}
\begin{document}

\begin{circuitikz}[american, voltage shift=0.5]

\draw (0,0)
to[V, l=$V_s$] (0,4)
to[short, -*] (2,4);

\draw (2,4)
to[R=$R_1$, i>_=$i_1$] (2,0);

\draw (2,4) -- (4,4)
to[R=$R_2$, i>_=$i_2$] (4,0);

\draw (4,4) -- (6,4)
to[R=$R_3$, i>_=$i_3$] (6,0);

\draw (0,0) -- (6,0);

\end{circuitikz}

\end{document}
```
