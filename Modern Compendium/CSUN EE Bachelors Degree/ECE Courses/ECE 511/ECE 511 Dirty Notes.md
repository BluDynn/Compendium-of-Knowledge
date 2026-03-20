# 2026-01-26
--- 
introduction into microgrids 
## Lecture
> [!tip] **Microgrid** 
> - Interconnection of small modular generation o low voltage distribution systems
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE511-Microgrid-Definition]

> [!tip] **Distributed Energy Resources (DER)** 
> - Energy distribution sources
> - fuel cell
> - Photovoltaics 
> - etc
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE351-Distributed Energy Resources-Definition]

focus on transmission and distribution

central generation and self generation
central - supplied from a cenntral souorce
self - small self gen components

any powers engineer knows this one eq

Total generation = Total Demand 

depending on how much demand there is youre expected to produce that much power

Islanded microgrid - localized self sufficient system that operates on its own grid

system contains 
source
loads
protection
controls
a means to rapidly seperate from main grid

Studying **Distributed Generations** 

Converter technologies (AC - DC)

in this class we will model the gas turbine (source) and then connect it to a dc to ac connector to the grid an study the controls

note to self - please please please PLEASE familiarize yourself with different source generators... cause oh my fucking god I feel so lost 

non dispatchable DG - cant be turned on or off? or rather are naturally varying? - photovoltaics + wind

Micro gird controllers 
interfacing with MC and LC controllers

DELTA p = p_M - P_E 
= 0

**swing equation**


**Power Factor eq**

**Active Power**

*Review Phasors 240*

Power Factors
Purely Inductive - P =0 ; theta v - theta I = 90deg
purely Resistive - P =1 ; theta v - theta I = 0 deg - unity PD 
purely Capacitive - P = 0 ; theta v - theta I = -90deg

"higher the PF the higher the performance"

Reactive Power  - "imaginary power"
q  = vrms irms sin(phi)

q> 0  - consuming
q< 0 - supplying 

Complex Power
P and Q 
... wtf is a Vars 

"power triangle"

Power Factor definition: 

End of session

---

# 2026-01-28
--- 
## What Happened Last Session?

intro to power systems
## What to expect this session?
 further exploratioon into the study of power systems

## Lecture 
last time we talked of 
Reactive Power 
Complex Power 
Power Factor
Synchronous Generators
- generated at the stator 
- controlled in the rotor

### Synchronous Generators
SG frequency depneds on the rotors speed so through mechanical power it can be controlled
-pmec?

#definition #equation
> [!help] **Complex Power**
> - statement 
> $$ \begin{align*}
 S = P + j Q &= V_{rms}I_{rms}^* \\
 &=(|V|\angle \theta_v)(|I|\angle \theta_i)^*\\
 &=(|V|\angle \theta_v)(|I|\angle - \theta_i)\\
 &=(|V||I|\angle \theta v - \theta_i)\\
 \end{align*} $$
> **Related Concepts**
> ^[ECEXXX-Equation-Definition]

$$\begin{aligned}
P = Re \{S\} = Re\{VI^*\}\\
Q = Im\{s\} =Im\{VI^*\}
\end{aligned}
$$
Stability - Swing Equation 

refer to power system into as a refresher for 410/411

### Three phase circuits
Three phase gens driven by constant fprce or toque
Generate a constant power iutput

> [!tip] **Three phase sources** 
> - three lines, a, b, and c
> Ideal Case 
> - ![[Pasted image 20260128104050.png]]
> Real 
> - ![[Pasted image 20260128104153.png]]
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

#### Balanced THree Phase Voltages
three sinusoidal voltages differed by 120deg phase difference of one another
**Two possible sequences**
1. abc (positive sequence) vb lags va by 12
2. acb (negatice) vb leads va by 120
Analysis of a three phase load may be transformed to a y configuration
or a one phase circuit

### Power calculations
P_A = VI cos theta
![[Pasted image 20260128110526.png]]
reactives+ Complex
![[Pasted image 20260128110555.png]]
![[Pasted image 20260128110654.png]]

THis weekend please please please review what we went over and the extras 

one more concept from a background - 
next lecture is more background

---
# 2026-02-02
---
AAAAAAAAAAA
I FORGOT TO DOWNLOAD THE MATLAB SPECIALIZED POWER SYSTEMS TOOLBOX

reviewing the three phase slides
 
three phase calculating amps is vvery easy if you know one, if you know one phase you cna off set the other two by 120 or -120 to get the other two

line voltages
will be quized next wednesday 
if you sse delta value node convert to the small one form repaet 

FUCK ON SIMULINK

generally matlab is meant for the practice of theory and models

fuck fuck fuck
linear system -> laplace -> out put input relation /transfer function 

power system dynamics is non linear! -> you have to linearize

WHAT THE FUCK 
how do we linearize it? - //ece 480 concept learned later in the sem// Taylor series
to approximize into a linear function 
UH WHA AHHHHHHHHHHHHHHHHHHHHHHHHH
WHAT THE FUCK IS THAT

TAYLOR SERIES

when you linearize the power system it wll only be gaurenteed to work aroumd the operationg point

in this class we consider MIMO systems
how do we express this as a transfer funciton
WHAT THE FUCK ARE STATE VARIABLES
"represent by State Space Equations"

//ECE 455 mathmatical models // -> //ECE 582 State space//

back to the swing equation 
google lmao

easier fromm the prof
$$J\frac{d\omega}{dt}=T_m - T_e$$
to this
$$\frac{d\omega}{dt}=\frac{T_m - T_e}{J}$$

next lec gon give
 omega0 =2lambda pi 60hz or something= omega =1pu 
 1pu = 100%
 1.1 -> 110%
 etc

omg that was an overload
quiz next monday

 --- 
# 2026-02-08 - ext notes catch up day
 ---
 DAWG I AM COOKED!!! 
 two pdfs to cover 
 work backwards for quiz #1 
 missed wednesday but thats somewhat fine I can catch up 

PDFs to cover 
Lecture 1.1 - Conceptual - review last
Power Systems_ intro - Fundamentals focusing on AC power calculations and Synchronous Generator control
Three_Phase_Systems - Main Concept (probably this is my assumption)

## Three_Phase_Systems.pdf 
#### Conceptual 
- Three Phase Gens are driven by constant force or torque 
- Devices that utilize three phase systems have a constant power output. 
#### Consider the following
as you review the lecture please consider these questions 
- What is a three-phase circuit (source, line, load)?
-  Why a balanced three-phase circuit can be analyzed by an equivalent one-phase circuit?
-  How to get all the unknowns (e.g. line voltage of the load) by the result of one-phase circuit analysis?
-  Why the total instantaneous power of a balanced three-phase circuit is a constant?
### Section 11.1 - 11.2 Three Phase Systems 
#### Three Phase Sources 
The main identifier of a three phase source and how its different from a elementary one phase source is the fact that there are now three ac generators within one rotor assembly. 
Consider that one ac source has an output voltage of $v(t) = V_m cos(\omega t)$ , now compare this to the new three phase voltage source of ... 
$$\begin{aligned}\left.
\begin{matrix}
v_a(t) \\ v_b(t) \\ v_c(t) 
\end{matrix}
\right\}\text{where v(t) } = V_mcos(\omega t); \\\text{each source with a phase difference of 120deg from each other} 
\end{aligned}
$$

There seems to be two seperate models for ideal Y- and $\Delta$ voltage sources... what are the differences
##### Y- and $\Delta$- Three phase Sources 
IDEAL
Y(wye) and $\Delta$ (delta) are connection configs 
They describe how the phase windings are connected to each other within the generator and the load. Both have difference Voltage and Current Configs
d- consider the two models shown:
**![[Pasted image 20260208165753.png]]**
Are they equivalent? If we are solely considering power output, yes.  however the behavior of voltages and currents are different. 

Voltage Relationships 

Y
V_L = sqrt3 (V_phi )
Line voltage is higher than phase voltage
each winding individually has less voltage 
good for high voltage system

$\Delta$
V_L = V_phi
Line Voltage is equal to phase voltage 
common for low voltag high current applicaitons

Current Relationships 
Y
I_L = I_phi

$\Delta$
I_L sqrt3 I_phi

Power (same for  both )
P_3 = sqrt 3 * V_L I_L cos(theta)
they  can deliver the same power but the currents and voltages vary

TLDR - Y sqrt3V /// $\Delta$ sqrt3I

REAL
real sources contain an internal impedence and resistance due to the use of coils in generators
![[Pasted image 20260209090948.png]]

Balaned three phase voltages 
so for both currentt and voltage there would be three sinusoids of the same amplitude freqency but differ by a 120 deg phase difference
2 possible squences in which 
abc - positive. vb lags va by 120 
acb - negative. vb leads va by 120 // or T/3 


#### Three Phase Systems

Source - load can be connected in four fiff configs
//it appears sources an loads can by Y or Delta
Y-Y , Y-$\Delta$, $\Delta$-Y, $\Delta-\Delta$ 

#### Analyzing Y-Y 
![[Pasted image 20260209091405.png]]

When sooving there would be these unknowns to be solved

- line voltage
	- Voltage across any pair of lines 
- Phase voltage 
	- Voltage across a single phase 
keep in mind for a y connected oad the **line current is equal to the phase current**
Solution to the general three phase circuit
**KCL LEADs TO THE ONE EQUATION**

$$I_0 = I_{aA} + I_{bB} + I{cC} \rightarrow $$
![[Pasted image 20260209091831.png]]

// balanced refers to the ymmetric poperties through all three pahses

for balanced 3phase circs
1. V across all lines have equal maf and 120 relative phases 
2. total impedence across any line is the same
utilizing kcl and solving for  V_N we get 

![[Pasted image 20260209092132.png]]
Funny nough this leads to the conept of transdertin this to a equivalent one way circuit since V_N = 0 there is no V diff between n and N which relays as a short. 
![[Pasted image 20260209092243.png]]


utilizing this model we can use our 240 knowledge to solve for line current and line voltaage
zphi = imedence total
solving for one phase leads to a determination of the other two phases due to sequence relation

![[Pasted image 20260209092409.png]]

revist line vs pase voltage

phase is the voltage across one phase // ;ine -> neutral
line is between two lines // phzse -> a - b 

**ANALYSIS OF Y-$\Delta$ CONFIG**
![[Pasted image 20260209093028.png]]

this is wa load in the delta config... where does it all go?

![[Pasted image 20260209093208.png]] 
its important to consider this as the what if we were to transform the delta to the Y
and vise versa 

$$Z_Y = \frac{Z_\Delta}{3}$$

the equivalent one phase circuit would work the same if Z_A - three phase load impedence - were to be replaced by Z_Delta /3 
![[Pasted image 20260209093415.png]]

The phase currents of the load in abc seq **THIS IS LITERALLY JUST KCL**

![[Pasted image 20260209093524.png]]

### Power calcs in balanced three phase circuits

avg pwer 
![[Pasted image 20260209093700.png]]

total power to the Y load
![[Pasted image 20260209093715.png]]

Complex power of a balanced Y-Load 
Wtf is reactive and complex powers 

reactive 
power that oscillates back and forth 
stored in inductos and caps 
Q = VI sin theta  // VAR volt amp reactive

Real power 
V I cos theta 
Complex power 
S = P + jQ 
P = real power 
Q - reactive
 j 


instantaneous piwer 
independent on time 
P tot = 3vi cos theta

torque is constant 

---
---
# 2026-02-09
---
Quiz day ... T^T bro i feel so cooked


yeah i got cooked...

quiz covered -
line current 
power factor 
complex power 
phase diagrams
.... 
 i got none of those 


what we were suppoesd to do, 
convert delta to y load 
quiz covered in midterm
![[Quiz 1_SP26_solution.pdf]]

PLECS to be covered next lec

#### ![[DG_rotating Machine_based.pdf|DG Rotating Machine]]

Any kind of turbine that creates a rotating shaft can be connected to a synchronous generator connected to a load. This is a definition of a **Distrubted generator** other wise low as a microturbine or gas turbine etc. 

Other wise known as ROtating Machine Base Distributed Generator

other kinds of gens are a DC -AC inverter // Inverter Based DGS 
- can come from fuel cell, photo voltaics, batteries - to be covered in the next topic

PDF notes
recap synchronous gen ahs two parts
stator and rotor 
with the rotation of the rotor the magnests creates a changing electromagnetic field inducing a current

Exciter Systems for Large Generators

![[Pasted image 20260209104539.png]]

![[Pasted image 20260209104606.png]]

we need to contol to thing, the speed of the rotor and the exciter voltage


**Grid connected mircogrid**
essentially its the idea that the microgrids source is from an external source usualy coming from a larger grid .

