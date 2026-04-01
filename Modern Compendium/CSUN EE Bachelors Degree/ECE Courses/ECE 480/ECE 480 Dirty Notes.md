# 2026-01-22
---
---
#ECEXXX #Dirty #PreLec 
## What Happened Last Session?
Syllabus
## What to expect this session?
Mathmatical Models of both Mechanical and Electrical Systems - ODes

## Lecture start 
---
### Electrical Systems
#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260122175311.png]]
^[ECE480-MeshCurrentODE-Prompt]

#Example #Solution #ECEXXX #DIrty 
###### Solution
>[!success] Example Problem: 
>{Prompt}
>{Solution Steps + Explaination} - notability
^[ECE480-MeshCurrentODE-Solution] test

"generally easier to consider the circuit with the s-domain(Laplace) to solve for desired voltages and currents"

Reminder Laplace is a mapping of the time domain within the space domain turning differentiation to algebra

#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260122180300.png]]
^[ECE480-OPampODE-Prompt]

// my bad i was slow and just listened as all the work is on the notes

### Mechanical Systems Fundamentals
---
#### Mechanical Translation^[MechanicalTranslation]
#definition #equation
> [!help] **Mechanical Translation**
> - sigma F = 0 or Sigma F applied = Signma F reactive 
> $$\huge \begin{align*} 
> \Sigma F &= 0  \\ \text{or} \\ \Sigma F_{\text{Applied}}&= \Sigma F_{\text{Reactive}} 
 \end{align*} $$
>
> **Related Concepts**
> \[\[Links here]]



"in engineering instead of primes they use dot" - newtons notation

#definition #equation
> [!help] **Elastance**
> - Spring stiffness and stuff
> $$ \huge \begin{align*}
 f(t) = k(y_2 - y_1)
 \end{align*} $$
>
> **Related Concepts**
> \[\[Links here]]
^[Elastance]

> [!help] **Damping**
> - Spring stiffness and stuff 
> - the more the velocity the more force you will have
> $$ \huge \begin{align*}
 f(t) = c(\dot y_2 - \dot y_1)
 \end{align*} $$
>
> **Related Concepts**
> \[\[Links here]]
^[Damping]

#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260122181831.png]]
^[ECE480-MechanicalODECart-Prompt]

#Example #Solution #ECEXXX #DIrty 
###### Solution
>[!success] Example Problem: 
>{Prompt}
>{Solution Steps + Explaination} - notability
>1. FBD
>2. Sum F = m a ; 
>3. simplify

^[ECE480-MechanicalODECart-Solution]

End of Session 

--- 

# 2026-01-27 
---
## Lecture

#definition #equation
> [!help] **Mechanical Rotation**
> - T = torque
> $$ \begin{align*}
 \Sigma T & = 0\\
 or \\
 \Sigma T_{Applied} &= \Sigma T_{Reactive} 
 \end{align*} $$
>
> **Related Concepts**
> ^[ECE480-MEchanical Rotation-Definition]

#definition #equation
> [!help] **Moment of Inertia (J)**
> - statement 
> $$ \begin{align*}
 T(t) &= J \ddot \theta (t)\\ 
 &= J \dot w(t)\\
 &= J \alpha (t)
 \end{align*} $$
 ![[Pasted image 20260127174452.png]]
>
> **Related Concepts**
> ^[ECE480-Moment of Inertia-Definition]


convert to definitions
![[Pasted image 20260127174524.png]]

## PDF 2
### Linear Approximation Physical Sysyems 
>[!question] for reference 
>x(t) = input
>y(t) = output


Necessary Conditions for Linearity:
Super Position and Homogeneity

#definition #equation
> [!help] **Super Position**
> - Sources combined is equal to the sum of the sources... no duh
> $$ \begin{align*}
 x_1 (t) &\rightarrow y_1(t)\\
 x_1 (t) &\rightarrow y_1(t)\\
 x_1 (t) + x_2(t) &\rightarrow y_1(t) + y_2(t)
 \end{align*} $$
>
> **Related Concepts**
> ECE 240 revisited
> ^[ECE480-SuperPosition-Definition]

#definition #equation
> [!help] **Homogeneity**
> - if you multiply the input by a scalar the output should be a multiple of the scalar
> $$ \begin{align*}
 x(t) \rightarrow y(t) \\
 a x(t) \rightarrow a y(t) \\
 \end{align*} $$
>
> **Related Concepts**
> ^[ECE480 -Homogeneity -Definition]


generally speaking y(t) = g(x(t)) can be linearized through Taylor Series expansion about $x_0$. 
![[Pasted image 20260127180330.png]]

IF the dependent variable depends on $n$ independent variables $x_1 , x_2 , ... , x_n$ then the linear approximation may be represented as ; ![[Pasted image 20260127180445.png]]

#### 2.4 Laplace Transform
bro im sure you already know this

#definition #equation
> [!help] **Laplace**
> $$ \begin{align*}
 L[f(t)] = F(s) = \int^\infty_{0^-} f(t) e^{-st} dt 
 \end{align*} $$
>
> **Related Concepts**
> ^[ECE480-Laplace-Definition]

properties of Laplace - i trust you already know this 
the rest of the class is examples and practice

## Lecture Recap
## What Happened this session?
wrapping up mechanical models of ODES + Linearity and Laplace review. Main review of 350. Laplace properties will not be provided in exam. but laplace transforms will 

## What to Expect Next Session: 

# 2026-01-29
---
Onto more Laplace and heaviside functiion

ALternate coverup method of partial fractions - never heard of it before 

Overall thus first section covers the many cases of the heaviside funciton and laplace

- distracted by other class + could not see
**the concept of signal flow charts should be reviewed**
-- oop he went in the wronog order


### Second Order System
$\zeta$  = Damping ratio 
$\omega_n$ = natural frequency


![[Pasted image 20260129182534.png]]

4 cases to consider
$$\huge\begin{aligned}
&&&\text{Case 1: Overdamped   .}&&\zeta > 1 \\
&&&\text{Case 2: Critically Damped   .}&&\zeta =1\\
&&&\text{Case 3: Undamped   .}&&\zeta = 0\\
&&&\text{Case 4: Underdamped   .}&&\zeta < 1 \\
\end{aligned}
$$

---

# 2026-02-05
---
missed a few 

flow graphs and mason's gain 


Masons Gain Formula
alternative method to obtain the system transfer funton using gblock or signal flow
forrm can be used to eval t f between sys and in..

# 2026-02-14 - Off study day 
--- 
im a failure omfg. 

## [(Intro to Block Diagrams)](https://www.youtube.com/watch?v=IqxJpaKuQGo)

![[Pasted image 20260214211157.png]]

### Elements of a Block Diagram
#### Summing Point 
The sum diagram of a block diagram, relatively straight forward just a sum function.

![[Pasted image 20260214211327.png]]

#### Take - off Point / Branch Point (Nodes)
I like to think of it similarly to a node in circuits where they share the same value 
![[Pasted image 20260214211551.png]]

#### Box ... (not covered in video.)
-CGPT
![[Pasted image 20260214211927.png]]
$$
C(s) = G(s) R(s)
$$
## [Block Diagram Reductions](https://www.youtube.com/watch?v=t_k7oRICmWo)
### Rules of Reducion
#### Rule 1: Representation of a closed loop system
![[Pasted image 20260214223351.png]]

#### Rule 2: Blocks in seires/cascade the gains are multiplied

#### Rule 3: Blocks in Parallel the gains are added

![[Pasted image 20260214223754.png]]


#### Rule 4: Shifting of take off point before a block 
#### Rule 5: shifting take off point after a block 

![[Pasted image 20260214224103.png]]

#### Rule 6: Shifting of a take off point before an adder 
![[Pasted image 20260214224439.png]]

#### Rule 7: Shifting take off point after adder
![[Pasted image 20260214224636.png]]

#### Rule 8: Rearrangement of adders
#### Rule 9: Shifting of added before a block

![[Pasted image 20260214224908.png]]
#### Rule 10: Shifting of adder after a block

![[Pasted image 20260214224943.png]]

## [Signal Flow Graphs](https://www.youtube.com/watch?v=10WwDd2QopQ&list=PLBlnK6fEyqRiiBFXtLOsvoAsPXqC8IBd8) 
- Graphical rep of block diagrams
- used o determine overall transfer function 
- easier method to determine transfer function compared to Block diagram as reduction is not required
- How to go from blocks to signal flow
### Elements of a signal Flow Graph 
Nodes - represents variables
Branches - lines connecting nodes
Input Node - nodes with only outgoing branches
Output Node - nodes with only incoming branches
Path - traversal of connected branches in the direction of arrows in which no node is traversed more than once
Forward Path - path from input node to output node
Forward Path Gain - product of branch gains encountered in traversing a forward path
Loop - a path which originates and terminates at the same node
Loop Gain - product of branch gains encountered in traversing a loop
Self Loop - loop with only one branch
Non-touching loops - loops not possesing any common node

#### Blocks to Signals
summing block -> node
Take off point -> node ?
block -> Branch
![[Pasted image 20260216142428.png]]

![[Pasted image 20260216142518.png]]



## [Mason's Gain Rule](https://youtu.be/k0zeegbCa38?si=xkAJfFhPHVg3CtXl)

When considering the signal flow chart 

$$\begin{align*}
&\frac{C(s)}{R(s)}=\sum^{n}_{k=1}{\frac{P_k \cdot \Delta_k}{\Delta}}
\\
\text{Where...}\\
& n = \text{Number of Forward Paths}\\
& P_k = \text{Forward Path gain of $k^{th}$ forward path}\\
& \Delta_k = \text{Associated Path Factor (cofactor)}\\
& \Delta = \text{Determinant of S.F.G. }\\
\end{align*}

$$
Determinant of SFG 
$$
\Delta = 
\large\begin{aligned}
1 &- \tiny{\text{Sum of gains of all the Indvidual loops}} \\ &\large+\tiny{\text{Sum of Products of gains of all possible combinations of two Non-touching loops}} \\&\large-\tiny{\text{Sum of Products of gains of all possible combinations of three Non-touching loops}} \large\\& + ~~... 
\end{aligned}
$$
Associated Path Factor
$$
\Delta_K =
\large\begin{aligned}
1 &- \tiny{\text{Sum of gains of all the Indvidual isolated loops}} \\ &\large+\tiny{\text{Sum of Products of gains of all possible combinations of two Non-touchingisoloated loops}} \\&\large-\tiny{\text{Sum of Products of gains of all possible combinations of three Non-touching isolated loops}} \large\\& + ~~... 
\end{aligned}
$$


# 2026-02-17 [[ECE480 P53-P66.pdf| Lecture PDF 53-66]]
---
behind but we still up

## Performace of Feedback Control System
 discussion on time domain performance specification ans system response for specific input signals.
### Test Input Signals
#### Impulse function
![[Pasted image 20260217173541.png]]
#### Step / Switching Function
![[Pasted image 20260217173615.png]]
#### Ramp Function
![[Pasted image 20260217173652.png]]
#### Parabolic function 
![[Pasted image 20260217173758.png]]

### First Order System - Step & Impulse Response
"impulse response" - response to a impulse input
"step response" - response to a step input 
"impulse response" - etc 
"impulse response" -etc 

k - dc gain 
$\tau$ - time constant

- open loop sysyem 
-![[Pasted image 20260217174549.png]]

after one time constant the plot reaches .632 of K
##### Q: How does the results show above change if input is R(s) = $\frac{A}{S}$
Due to it being linear system the output would be scaled by A as the input. This has no affect on the time constant or time to get to steady state. 

Notice how the response is \*s of the previous example has a response that is equal to the derivative of the previous one
![[Pasted image 20260217175338.png]]

##### Step Response for a the first order system with c(0)= c_0 == 0

![[Pasted image 20260217175713.png]]

Key take away from that mess is that ...you find the response with math... sigh im pretty sure its one of those things you learn by doing

looking at the finished response 
the first term is the zero input, and the second term is the zero state response 
![[Pasted image 20260217175942.png]]

dw you dont memorize this 
![[Pasted image 20260217180049.png]]

## Performance of Second Order System 
note - first order system response - should know for career
1 time constant = %63.2
4time constant = %98.16
or 5 time constant

funny enought its all diff eq review, like homo then general 
![[Pasted image 20260217180725.png]]

This term is the damped natural frequency 
$\Huge\omega_d$ = ![[Pasted image 20260217180929.png]] 

##### Step Response of an Underdamped System:
Pg 6-7 of pdf 
Notice how that the response is a damped sinusoid so it'll wobble back and forth for a bit then reach the k 
$\beta$ - damping factor
##### Step Response of an Overdamped System:
essentially itll take longer to get to steady state
##### Step Response of an Critically Damped System:
System would come to a rest efficiently 


#### Impulse responses in damped systems
Undamped - oscillates between positive and negative 
Underdamped - oscillates between positive and negative and rests at 0 
Over damped - slowly rests at 0 
critically damped - efficiently rests at 0 
![[Pasted image 20260217182841.png|500]]

![[Pasted image 20260217183140.png|500]]

![[Pasted image 20260217183201.png|500]]
![[Pasted image 20260217183228.png|500]]
![[Pasted image 20260217183313.png|500]]

I think this is the new stuff 
#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260217183545.png|500]]
>^[ECEXXX-ProblemTitle-Prompt]



# EXAM 1 - :(

# 2026-02-26 
---
## Performance Indices

ISE - integral square error
IAE - integral absolute error
ITAE - integral time absolute value - modulates error 
ITSE - Itegral time square error
ISTSE - integral square time square error
Linar tracking 
Terminal Control 
Minimum Control Effort


## Stability
"perputation theory"
it will want to stay where it is at 
car in valey = stabel - you push it it goes back 
car in hill = unstalble - you push it it wants to keep going a wau

other marginally stable or neutral - other 

o - zeros -roost of the denom of the transfer funticon
x - poles- of the transfer funciton


---
# 2026-03-05
---

## 7.1 - Root loctus intro

Evans 1948
Root locus of a ststem is a plot of the roots of the ststem characterisics 
the oles of the closed loop t func

## 7.2 root locus concept
to understand the concpept of Root locus consider the example in which he oles are able to be evaled as K varies from any pos num

to botain S_1,2 you can use quadratic or factor 

roots depend on K 

and if you wrer to plot on the im plane you can see that as you inccrease the poles they approach a break point 

Anoter method of considering system poles is setting 1+ GS = 0 
so that if S_1 is a pole with 1 + kgs  i need to change notes cause im not perofings

## 7.3 RL procedure

RL procedure


ruels to pot root locus 
is always symetrical with respoec to the real axis 
branches alwats start at ples nad K equals 
so at the location of the poles K becomes 0 and at the loaciton of the 0 k becomes infinitiy
 so as k caries for - to infi rL of Ts asrar of poels of transder and terminates a zeros of Fs Hs pole at 0 pole at 6 so now what 
 - 6 -w  ad kn dm lk

number of braneches is = ro piels , if poles > than mu,enr pf is greater thatn numebr of tanser

amad os equa o the numebr of zeros of GH if number pof zeros of is feathe ihtaskd jjsadpok


# 2026-03-24
---

What happened last time... Man idfk 

Exam date being finalized 
"most of the stuff you need to study is there"

design Root locus 

"final is cumulative but leaned towards the latter part"

Fuzzy control - taught by babak next time lmao
Graduate level controls "ECE 581 or sumthin" "ECE 580 digitial controls"

Quick 8 rules of the root locus
Rule 1 
each open loop pole creates one path 
n poles -> n branches

Rule 2 
start and end points 
starrts at open loop poles 
ends at open loop zeros or infinity

Rule 3 
Symmetry
root locus is symmetric about the real axis

Rule 4 
real axis segments 
a point is on the root locus if the number of real poles + zeros to the right is odd 

babak/alimini ""

Rule 5/6
Linear Asymptotes 
if poles > zeros, extra branches go to ininity along asymptoes

Branches can split off the real axis or merge back 

Rule 7 
imaginary axis crossing 
Routh Hurwitz - CPGT - to find when poles cross into instability 

Rule 8 
break away/ break in point

Rule 9
Angle of departure/arrival
to be considerd when GH has complex/imginart poles (angle of departure)
GH with complex/imaginary zeros  (angle of apporach )

"KGH" - closed loop gain


fuck i had to shit and i missed notes

read the textbook and have fun! 
PID CONTROL YES FINALLY
