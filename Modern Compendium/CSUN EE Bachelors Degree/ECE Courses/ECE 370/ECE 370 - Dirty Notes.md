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

# 2026-03-23
---  
## The Smith Chart
// YT smiths - the smith chart is a versatile tool that we olnly cover a tip of it. 
 
 > graphical tool for analyzation and design for transmission line circuits
 
- Lies in the complex $\Gamma$ plane
	- x axis real $\Gamma$ 
	- y axis im $\Gamma$
1. Normalize Impedance 
2. $$\Gamma = \frac{Z_1/Z_0 -1}{Z_1/Z_0 +1}= \frac{z_L -1}{z_L+1}$$
3. $$z_L = r_L +j\omega_L$$
4. Fuck ass derivations
5. Open circuit - RHS
6. Short Circuit - LHS 
7. Matched case - $\Gamma$ = 


**We will be utilzing THE COMPLETE SMITH CHART**

positive - inducatnces - toop part
negative - capacitance - bottom part

Practice - for GAMMA reflection coefficient

step 1 - normalize (divide by Z_0)
Z_0 = 50 OHMS || z_L = Z_L/Z_0 = 100 -j50)/50
comes out to be ... r_L + jX_L

step 2 
This found value will be a dot
- r_L is the resistive component for the value of 2
	- but 2 isnt just the point it is the circle at 2
to find thedot you must find the imaginary component
- jX_L is on the numbers next to the edge of the chart, below is minus, above is positive.

step 3 ... DRAW A LINE WTH
- draw the line from the point to the matched case or center point and then the through line should be your theta r - This is the anlge

Magnitude calcs - 
Method 1 - ruler and measure from center to Z_L point  from this make it relative to the smith chart as d1 /d2 

Method 2 - bottom rule - measure and go left with the same distance as d 1 

--- 
if you draw a circle on that Z_L the value of d1 would be the same 
"the magnitudde of the reflection coeffifcient is the same " but the angle is differnet
 