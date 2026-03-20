chat i should probably read before 

# 2026-01-26
---
Wavelength $\lambda$ in a vaccum related to the speed of light $c$ and oscillation frequency $f$
$$ \huge\begin{aligned}
\lambda = \frac{c}{f}
\end{aligned}
$$
light is just one type of EM wave, which the speed is dependent on the medium and material properties

PAy attention to what material is EM being propagated in 

$U_p$ - Propogation Velocity


# 2026-01-28
--- 
## Waves in a lossless Medium 
#definition #equation
> [!help] **waves in aa lossless medium**
> - phi is just a phase shift
> direction of wave propogation 
> - \- is moving along the +x direction
> - \+ is moving along the -x direction
> $$ \begin{aligned}
> y(x,t) = A cos\left(  \frac{2\pi t}{T} - \frac{2\pi x}{\lambda} + \phi_0 \right)
> \end{aligned}
  $$

Considering $\phi_0 = 0$
$$\begin{aligned}
 y(x,t) &= A cos\left(  \frac{2\pi t}{T} - \frac{2\pi x}{\lambda} + \phi_0 \right)\\
 y(x,t) &= A cos\left(  2\pi ft  - \frac{2\pi }{\lambda}x\right)\\
 y(x,t) &= A cos\left(  \omega t  - \beta x\right) \\\\
\text{ assuming  } \\\omega = 2\pi f\\\beta = \frac {2\pi}{\lambda} 
\end{aligned}
$$

#definition #equation
> [!help] Propogation velocity
> - statement 
> $$ \begin{align*}
 U_p = \frac{\lambda}{T} =f \lambda = \frac{\lambda}{\beta}
 \end{align*} $$
>
> **Related Concepts**
> ^[ECEXXX-Equation-Definition]

#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260128133241.png]]
>^[ECEXXX-ProblemTitle-Prompt]
#Example #Solution #ECEXXX #DIrty 
###### Solution
>[!success] Example Problem: 
Red wave: $$
V_{red} (t)= 5cos(\frac{2\pi}{8}t) $$
green wave: $$V_{green}(t) = 5cos(\frac{2\pi}{8}t+2\pi\frac{1}{8})$$
Reminder wave form: $$V_{x}(t) = A(\frac{2\pi}{\omega}t+\phi)$$
in which A is the AMplitude 
$\omega$ is the period 
$\phi$ is the phase angle 
$$ \phi = 2pi \frac{\text{x offset from... need to find the wording for this}}{\omega}$$
BLue wave:$$
V_{blue}(t) = 5cos(\frac{2\pi}{8}t-2\pi\frac{2}{8})$$
>^[ECEXXX-ProblemTitle-Solution]

#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260128135007.png]]
>^[ECEXXX-ProblemTitle-Prompt]

#Example #Solution #ECEXXX #DIrty 
###### Solution
>[!success] Example Problem: 
>Direction: - z firection 
>wave frequency - 2pi/T - f = 1/T-> $\frac{2\pi t}{2 *10^7}$ -> $\frac{10^7}{2}$ = $\frac{2}{10^7}=2*10^{-7}$ **error** 6\*10$^6$
>$$omega = 2\pi f ; cos(\omega t)$$
>$$f = \omega/2pi= 5*10^7$$
>$$\frac{pi * 10^7}{2pi}$$PLEASE REVISE
>wavelength  - 2pi z/lamda -> $\frac{2\pi z} {30}$ = $30 =\lambda$
>phase velocity - > $$ \begin{align*}
 U_p = \frac{\lambda}{T} =f \lambda = \frac{\lambda}{\beta}
 \end{align*} $$
 $$lambda * f = \frac{2}{10^7} * 30m= \frac{60}{10^7}=60*10^{-7}$$
 >^[ECEXXX-ProblemTitle-Solution]


### Waves in a lossy medium
#definition #equation
> [!help] **Waves in a lossy medium**
> - statement 
> $$ \begin{align*}
 y(x,t) = Ae^{-ax}cos(\omega t = \beta x + \phi_0)
  \end{align*} $$
  alpha is a real number decided by the material of transmission line
> **Related Concepts**
> ^[ECEXXX-Equation-Definition]

#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260128141042.png]]
>^[ECEXXX-ProblemTitle-Prompt]


Complex numbers review is coming up

End of session

---
# 2026-02-02
---
a little late but right into Complex numbers

algebra review 
![[Pasted image 20260202130707.png]]

Complex Conjugate rview 
![[Pasted image 20260202131717.png]]

### Start of Ch2 
'intro to transmission lnes' pdf
### Transmission lines 
 #### Transmission Line Properties // wrong slide
 - Resistance 
 - Conductance
 -  inductance
 - Capacitance



# 2026-02-04
---
Lumped TL model 
models of component cluster that scales per $\Delta x$ 
$R'$ think about the prime as a way to say ohm per meter as a unit as we are multiplying by meter
$L'$ think of self inductance per meter it is neccesary in RF
$C'$ think 
$G'$ the conductance permeter ig 

Transmission line Table Eqs

---
# 2026-02-09
---
[[ECE 370 - 5 - Standing Waves.pdf]]

