[[ECE 340 - Electronics I]]
Intro 
- hook: 
- use cases 
- relevance to course 
- segway 

> On the day to day basis electronics utilize small signals, from RF signals to sensor data. These small signals at times are hard to utilize and read, therefore the necessity of a signal amplifier becomes apparent. One of the most common and classical methods of signal amplification come from the use of the BJT transistor. The BJT while it may at times operate as a switch is also able to perform as an small signal amplifier. One common topology is the "common emitter" circuit. 

Theory 
- Common Emitter Amp 
	- Properties
	- Distortion

> The common emitter amplifier has several distinct properties. It provides high voltage gain and operates as an inverting amplifier, producing a 180° phase shift between the input and output. It also exhibits moderate input impedance and relatively high output impedance.

- Designing a common Emitter Amplifier 
	- Overview
	- Specification Consideration
	- Output Impedance
	- Gain
	- DC Load Line + Q-point 
		- Distortion and Clamping
	- V base 
	- Voltage Divider Biasing
	- Coupling Capacitors 

![[Pasted image 20260311120723.png]]

> To design and implement a common emitter amplifier it is wise to have set specifications in mind. Key specifications that need to be considered as shown in FIGURE HERE. ![[Pasted image 20260311121433.png]]
>
>To get started on the design, the input and output impedances can be taken into consideration first. The Input impedance of the common emitter amplifier is the resistance “seen” by the input signal when looking into the base terminal. Inspecting the base terminal the impedance can be clearly seen as the resistors in parallel as seen in EQUATION HERE. As for the output impedance, the relation of the output impedance can be roughly estimated to be equal to $Z_{out}$ as shown in EQUATION HERE. This allows for the resistor value of $R_4$ to be assumed. 
>
With the impedance relationships determined, the amplifier gain relationship may be utilized to obtain $R_3$ and $R_4$ . The voltage gain equation as many know is described as the output voltage over the input voltage, as shown in FIGURE HERE this can be oversimplified and estimated to be negative $R_3$ over $R_4$. Through this relationship we are able to assume values for the resistors and continue developing the amplifier.
With preliminary resistor values assumed, the DC behavior of the amplifier must now be analyzed to ensure proper transistor operation. This is accomplished through the development of the DC load line, which represents all possible operating points of the transistor based on the external circuit constraints. The load line is plotted on the collector characteristic curves with collector current $$I_C$$ on the vertical axis and collector-emitter voltage $$V_{CE}$$ on the horizontal axis.

Two boundary conditions define this line. When the transistor is in cutoff, the collector current is zero and the entire supply voltage appears across the transistor:

$$
V_{CE} = V_{CC}
$$

When the transistor is driven into saturation, the collector-emitter voltage approaches zero and the current is limited by the surrounding resistors. The saturation current can therefore be approximated as:

$$
I_{C(\text{sat})} = \frac{V_{CC}}{R_3 + R_4}
$$

Connecting these two points forms the DC load line. Superimposed on this graph are the transistor characteristic curves corresponding to different base currents. The intersection of a selected base current curve with the DC load line defines the operating point, or Q-point. At this location, the transistor operates in the active region and the values are denoted as:

$$
I_{CQ}
$$

$$
V_{CEQ}
$$

To ensure proper amplifier operation and minimize distortion, the Q-point must allow sufficient headroom for signal swing. A common approximation is to position the operating point near the midpoint of the load line, such that:

$$
V_{CEQ} \approx \frac{V_{CC}}{2}
$$

or equivalently,

$$
I_{CQ} \approx \frac{I_{C(\text{sat})}}{2}
$$

Placing the Q-point near the center reduces the likelihood of clipping caused by driving the transistor into cutoff or saturation.

Once the desired quiescent collector current is established, the emitter voltage can be determined using the emitter resistor:

$$
V_E = I_{CQ} \cdot R_4
$$

Since the base-emitter junction behaves approximately like a silicon diode, the base voltage is related to the emitter voltage by:

$$
V_B \approx V_E + 0.65
$$

To set this base voltage, a voltage divider biasing network composed of $$R_1$$ and $$R_2$$ is used. In order to prevent the divider from being significantly loaded by the base current, a common design guideline ensures that the current through the lower divider resistor is much greater than the base current:

$$
I_{R2} \ge 10 I_B
$$

This improves bias stability and reduces sensitivity to variations in transistor gain $$\beta$$. Once $$R_2$$ is selected to satisfy this condition, $$R_1$$ can be calculated using the voltage divider relationship:

$$
V_B = V_{CC} \frac{R_2}{R_1 + R_2}
$$

Finally, coupling capacitors are incorporated to block DC components while allowing AC signals to pass. These capacitors form high-pass filter networks that determine the lower cutoff frequency of the amplifier. In general, the cutoff frequency associated with a coupling capacitor is approximated as:

$$
f_c = \frac{1}{2\pi R_{\text{seen}} C}
$$

The overall lower cutoff frequency of the amplifier is dominated by the largest individual cutoff frequency:

$$
f_L \approx \max(f_{c1}, f_{c2}, \dots)
$$

Although not the primary focus of this design, proper selection of the coupling capacitors ensures that the amplifier operates effectively within the desired frequency range.





Procedure + Results
- Construct the DC biasing 
- Construct full amplifier
- Measure Amplifier Gain
- Measure Distortion
- Measure and Calculate Input Impedance
- Measure and Calculate Output Impedance 
- Overview and Specifications matching
PSPICE
- Initial Setup 
- DC operating Q point 
- Voltage Gain 
- Input Impedance
- Output Impedance
- Output Swing

Conclusions

chat gpt will be utilized for the sake of efficiency