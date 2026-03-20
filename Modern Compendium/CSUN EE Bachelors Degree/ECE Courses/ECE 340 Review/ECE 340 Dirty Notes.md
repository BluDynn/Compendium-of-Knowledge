# 2026-03-10
--- 
## Bipolar Junction Transistors

![[Pasted image 20260310231907.png|]]

### Common Emitter Amplifier 
Properties: 
- Inverting Amplifier 
Design Requirements: 
- Desired Bias Supply Voltage 
- Desired Output Impedance 
- Desired Gain 
- Bandwidth???? - dawg wth  - update: its not that bad just not covered back jack ou
![[Pasted image 20260311072653.png|500]]

> [!task]  Output Impedance
> Considering the graph our output impedance ideally is equal to $R_3$

> [!task]  Input Impedance
> The input impedance of the common emitter amplifier is the resistance “seen” by the input signal when looking into the base terminal.
>
In a voltage-divider biased CE amplifier, the input signal sees:
>
> - The bias resistors R1R_1R1​ and R2R_2R2​
>    
>- The small-signal resistance looking into the base of the transistor  
>
Therefore, the total input impedance is approximately:

> [!task]  Gain
> Overall the gain by definition is $A_V = \frac{V_{out}}{V_{In}}$ however, this relationship can be simplified to the ratio between $R_{3}$ and $R_{4}$ as shown below... 
> $$ \text{Gain~} = -\frac{R_3}{R_4}$$ 
> The oversimplified explanation of the negative ratio is due to it being an  inverting amplifier

> [!error] DC Load Line
> The DC load line is a graph set by the analysis of the circuit, it is a graphical representation of the transistor behavior plotted on the axis of the collector current $(I_C)$ over the collector emitter voltage $(V_{CE})$ and can be described as the linear line from the saturated collector current  $I_{C(Sat)}$ to the Collector Emitter Voltage Cutoff $V_{Cutoff}$.
>  
> In the case of the Common Emitter Amplifier $V_{Cutoff} = V_{CC}$. While the $I_{C(sat)} = \frac{V_{CC}}{R_{3}+R_{4}}$ as it is the current through the transistor when it is active.  
> 
> Plotted on the same graph is the characteristic behavior of the transistor based on the Base Current ($I_B$). ==The intersection of the transistor behavior and the line from the saturation current and the voltage cutoff lies the Operating point also known as the Q - point. //need to double check//== At the Q point the collector current and the common emitter voltage  professors and textbooks will call this the $I_{cq}$ and the $V_{cq}$ which stand for the quiescent points. 
> 
> Additionally operating point/Q point should be placed in which there is "headroom" for the amplifer to operate at, often times this is.... 
> $$\begin{matrix}I_{CQ} = \frac{I_C}{2}&~~\text{or}~~&V_{CEQ} = \frac{V_{CE}}{2}\end{matrix}$$



> [!task] Solving for $V_{emitter}$ and $V_{base}$ 
> With the $I_q$ we are now able to solve the voltage across the emitter as we take the current while the amplifier is active with the set resistance. With this we can find the $V_b$ as it will have a difference of 0.65V from the emitter. 

> [!task] $R_1~ \&~ R_2$ the voltage divider 
> As a good rule of thumb the current of the $R_2$ should be around ten times as much as the current into the base, this is to ensure the voltage divider is not loaded by the transistor and can act ideally. $$\begin{aligned} I_{R2} &\ge 10~ I_b \\
> \text{when solving for resistor values overly simplifies to...}\\
>  R_2 &= \frac{\beta \times R_4}{10}
> \end{aligned}$$
> Lastly solving for $R_1$ is a simple use of circuit analysis and the voltage divider formula

 >[!task] Coupling Capacitors 
 >Design regarding the coupling capacitors is not emphasized in the class however it is important to note that this would determine the cut off frequency. 
 >
 >$C_1$ (input Capacitor) determines the lower $f_{cutoff}$ which is determined by the equation... 
 >$$f_{cuttoff} = \frac{1}{2 \pi ~*~ R_1~||~ R_2 ~*~ C_1}$$ 
 >
 > Likewise the output capacitor also determines the lower $f_{cutoff}$ which is determined by the equation...
 > $$f_{cuttoff} = \frac{1}{2 \pi ~*~ R_{unkown/load} ~*~ C_1}$$ 
 > 
 > This may seem odd at first but its important to note the higher frequency cut off will be taken into consideration. The earlier relationships can be simplified as...
 > $$
f_c = \frac{1}{2\pi R_{\text{seen}} C}  $$
>
>while the considered frequency cutoff can be described as $$ 
>f_L \approx \max(f_{c1}, f_{c2}, f_{c3}, \dots)
>$$
 
 
 





