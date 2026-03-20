# 2026-01-26
---
---
#ECE351 #Dirty #PreLec
## What Happened Last Session?
Syllabus ^494cb5
## What to expect this session?

^910ee3

Course Introduction 
## Lecture

> [!tip] **Signal** 
> - A set of data (often a function over time) 
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE351-SIgnal-Definition]

As you may know there are two different types of signals **Discrete** and **Continuous** time Signals

> [!tip] **Continuous Time Signals** 
> - Signals in which the values are valid for all of time over some range
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE351-Continuous Time Signal-Definition]

> [!tip] **Discrete Time Signals** 
> - Signals in which the values are valid for a sampled set of time over some range
> - finite set of points
> - Uniformly spaced values
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE351-Discrete Time Signal-Definition]


ECE 350 has dealed wit hcontinuous time signals, ECE 351 focuses on the discrete case. Its important to consider how to consider signals in discrete. 

### Types of Signal
#### Analog vs Digital Signal
> [!tip] **Analog Vs Digital Signals** 
> - Analog Signals can hold a value over a continuous range (ex. 0-255)
> - Digital Signals can hold a binary value over a set range (Ex. 0 - 1)
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE351-Analog vs Digital Signals-Definition]

#### Converting Analog to Digital Signals
Quantization
#definition #equation #Dirty 
> [!help] **Quantization**
> - Analog to Digital process 
> - First take continous time analog and convert the signal to discrete time analog 
> - take the signal and utilize a quantizer to convert to a discrete time digital signal
>$$ \begin{align*}
 x[n] = x(nT) - \text{-> discrete-time analog}\\\\
 \text{Binary conversion utilizing quantizer}
 \end{align*} $$
>- please revise
> **Related Concepts**
> ^[ECE351-equation-Definition]

when we have L levels we can represent the total number of bits as n in which $L = 2^n$ in which n is round up to the nearest integer ^f59318

> [!tip] **Discrete signal representation** 
> - Functional Form
> 	- as a function
> - Explicit Sequence Form
> 	- as a direct sequence 
> - Graphic
> 	- Graph
> - Tabular Form
> 	- Table
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE351-Discrete Signal Representation-Definition]

### Introduction to Systems
#### Analog Vs Digital Systems
> [!tip] **Analog Systems** 
> - input and out put signals are both analog
> - more ECE 350 related
> - Analytical techniques
> - analog electronics
> **Related Concepts**
> #definition #concept 
> ^[ECE351-Analog System-Definition]

> [!tip] **Digital Systems** 
> - inputs and outputs are both represented digitally
> - numerical techniques
> - digital electronics
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE351-Digital System-Definition]

Mixed signals also exsist ofc

#### Digital Systems
Digitals signal processing techniques are powerful and would be difficult or impossible for analog signals to do the same. Digital Signals can be **regenerated** or cleaned up, with the binary storing of values with thresholds we can reduce the noise within a signal. "antipodal signals?" - add context here

**Advantages of Digital Systems**
- Better tolerances
- may be computer controlled with software
- can be more compact than analog
- errorcorrection code is possible
- DSP(digital signal processing) easy to modify systems
**Disadvantages of Digital Systems**
- high frequency cannot be processed digitally 

## Lecture Recap
 #ECEXXX #LecRecap
### What Happened this session?
Introduction to Digital Systems lecture
### Key Take Aways:
Analog to digital Conversion as a concept 

## What to Expect Next Session: 
Sampling, interpolation, alternate types of discrete signals

---
# 2026-02-02
--- 
miissed last lecture. 

last lectureL
interpolation - if we respect the micro sampling we apss this trhough a low pass filter does something with a sine function... I need to understand this

Last class covered lec 3 - sampling and inerpolation

## Partial Lec 3 
### Types of Discrete Time signals
#### Energy & power signals
#definition #equation



> [!help] **Energy Signal**
>- Let x\[n\] be a discrete time signal
> 	- mainly considering Finite -energy signals
> 	- $$ \huge \begin{align}\begin{matrix}E_x = \sum^{\infty}_{n=-\infty} |x[n]^2|    &; & 0< E < \infty \end{matrix}\end{align}$$
> consider the idea that within continuous time you would integrate the signal
> **Related Concepts**
> \[\[ECE 350]]
> ^[ECEXXX-Equation-Definition]


> [!help] **Power Signal**
> Generally Speaking the relationship between energy and power is Energy over Time
>- Let x\[n\] be a discrete time signal
> 	- mainly considering Finite -energy signals
> 	-  $$ \huge \begin{align}\begin{matrix}P_x = \lim_{n \rightarrow \infty} \frac{\sum^{\infty}_{n=-\infty}}{2n+1}    &  \\\small{\text{If Px is finite and not equal to 0 then x[n] is a power signal}} \\\small\text{ If periodic then find energy in one period and divide by N}\\ P_x = \lim_{n \rightarrow \text{period}} \frac{\sum^{\infty}_{n=-\infty}}{\text{period}}\end{matrix}\end{align}$$
> consider the idea that within continuous time you would integrate the signal
> **Related Concepts**
> \[\[ECE 350]]
> ^[ECEXXX-Equation-Definition]


#### Causal & Non-causal Signals
refer back to ece 350 
> [!tip] **Causal signal**
> - signals that start after t = 0
> 	- x(t) = 0 for t<0
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

> [!tip] **Non Causal Signals signal**
> - signals that start after t = 0
> 	- x(t) = 0 for t<0
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]


CHAT! THIS IS GENRALLY ECE 350 TOPICS I WILL REVISIT THIS WITH DEFINITIONS FROM MY OLD NOTES
#Dirty 

periodic vs aperiodic
symmetric and anti symmetric

### Questions for Review

1. Digital signals assume a finite number of levels on the
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ axis.
(==vertical==/horizontal)
2. Discrete signals assume a finite or countably infinite set of values on the \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ axis.
(vertical/==horizontal==)
3. Sampling a continuous-time analog signal yields a
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ signal.
(digital/==discrete==)

reading assignment Ch 1, 3, 8.

 **End of Lec 3 pdf**

## Lec 4 pdf
### Useful Discrete Time signal models
#definition #equation
> [!help] **Discrete Time Impulse finction**
> - $$\huge \delta[n] = \left\{ \begin{matrix}1, n=0 \\ 0, n = 0\end{matrix}\right.$$
>
> **Related Concepts**
> ^[ECEXXX-Equation-Definition]

> [!help] **Discrete Time Unit Step function**
> - $$\huge u[n] = \left\{ \begin{matrix}1, n>=0 \\ 0, n < 0\end{matrix}\right.$$
> - example
> - ![[Pasted image 20260202090640.png]]
#dirty
> **Related Concepts**
> ^[ECEXXX-Equation-Definition]
#definition #equation

> [!help] **Discrete-Time Sijusoidal Function**
> - statement 
> $$ \begin{align*}
 C cos[\Omega n + \theta]\\or\\ C cos[2\pi F n + \theta]
 \end{align*} $$
>$C$ = amplitude
>$\theta$ = phase offset, radians
>$\Omega$ = frequency (rad/sample)
> **Related Concepts**
> ^[ECEXXX-Equation-Definition]


#dirty 
![[Pasted image 20260202091827.png]]

#definition #equation
> [!help] **Discrete Time Complex Exponentials**
> - statement 
> $$ \begin{align*}
 \huge e^{j\Omega n }
 \end{align*} $$
>Recall Euler's 
>#dirty
>![[Pasted image 20260202092119.png]]
>![[Pasted image 20260202092159.png]]
> **Related Concepts**
> ^[ECEXXX-Equation-Definition]

more ece 350 concept
s

discrete graphical convolution

end of lec - graphical practivce pages
# 2026-02-23
--- 
caught up  taling z transforms - 

Why Laplace? 
to turn differentials to algebra in the S domain

Laplace vs Fourier ?
Laplace is used to convert to polynomials 
Fourier is used to decompose into different frequencies
## Z - transform 
essentially the Laplacein discrete

$$\huge z{x[n]}=X[z]=\sum^\infty_{n={-\infty}}x[n]z^{-n}$$

 Region of Convergence (ROC): The set R of values of z for
which the z-transform X(z) converges is called its region of
convergence (ROC).
➢ In general, the region of convergence


,but why do we need this - 

lowk fell asleep - but i need to try taking notes differently - if anything his class is proabably a take notes outside -listen in lecture type of class

next class ... ;-; 

