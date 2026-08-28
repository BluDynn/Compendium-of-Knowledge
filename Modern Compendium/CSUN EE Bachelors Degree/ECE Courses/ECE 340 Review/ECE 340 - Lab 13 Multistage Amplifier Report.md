# Design of Multistage Amplifiers  
  
**Course:** ECE 340L  
**Date:** May 6, 2026  
  
---  
  
## 1. Introduction  
  
In practical circuit design, a single-stage amplifier is often unable to meet multiple requirements such as high voltage gain, high input impedance, and low output impedance simultaneously. Multistage amplifiers solve this problem by combining different amplifier configurations, where each stage contributes a specific characteristic.  
  
In this experiment, a dual-stage amplifier was designed using a MOSFET and a BJT. The MOSFET stage provides high input impedance, while the BJT stage provides voltage gain and output drive capability.  
  
---

## DC Analysis – BJT   
  
|                          | $$V_C$$ | $$V_B$$ | $$V_E$$ | $$V_{CE}$$ | $$V_{BE}$$ | $$V_{RE}$$ | $$I_E$$ |     |
| ------------------------ | ------- | ------- | ------- | ---------- | ---------- | ---------- | ------- | --- |
| **Theoretical (PSPICE)** | 20V     | 8.648V  | 7.975V  | 12.025V    | 0.673V     | 7.975V     | 6.203mA |     |
| **Measured**             | 20V     | 8.1V    | 7.6V    | 12.54V     | 0.64V      | 7.6V       | 5.96mA  |     |
| **Percent Error**        | 0.00%   | 6.34%   | 4.70%   | 4.28%      | 4.90%      | 4.70%      | 3.92%   |     |
|                          |         |         |         |            |            |            |         |     |
  
This data shows the DC operating point (Q-point) of the BJT stage and compares the measured values to the PSPICE simulation results. The collector voltage remained exactly at 20V, indicating proper supply behavior.  
  
Small deviations are observed in the base and emitter voltages, with percent errors ranging from about 4–6%. These differences are expected due to transistor parameter variation, especially $$\beta$$, and non-ideal resistor tolerances.  
  
The collector-emitter voltage $$V_{CE}$$ shows a small error, confirming that the transistor is correctly biased in the active region. Overall, the measured values closely match the PSPICE predictions, indicating that the DC biasing network is functioning as intended.  
  
---  
  
## DC Analysis – MOSFET  
  
| | $$V_D$$ | $$V_G$$ | $$V_S$$ | $$V_{DS}$$ | $$V_{GS}$$ | $$V_{RD}$$ | $$I_D$$ |  
| ----------------- | -------- | -------- | -------- | ---------- | ---------- | ---------- | --------- |  
| **Theoretical (PSPICE)** | 11.78V | 6.377V | 3.738V | 8.042V | 2.639V | 8.22V | 3.738mA |  
| **Measured** | 11.43V | 6.34V | 3.91V | 7.52V | 2.5V | 8.61V | 3.97mA |  
| **Percent Error** | 2.97% | 0.58% | 4.60% | 6.49% | 5.27% | 4.74% | 6.21% |  
  
This data shows the DC behavior of the MOSFET stage by comparing measured values to PSPICE simulation results. The gate voltage $$V_G$$ shows very low error, indicating stable biasing from the voltage divider network.  
  
The source and drain voltages show slightly higher deviations, which can be attributed to variations in the MOSFET threshold voltage $$V_{th}$$ and transconductance $$g_m$$ compared to the ideal PSPICE model.  
  
The drain current $$I_D$$ shows a small error of about 6%, which is within expected limits for discrete components. Overall, the MOSFET remains properly biased in the saturation region, and the measured results align well with simulation predictions.

## AC Analysis – Dual Stage Amplifier

The AC analysis demonstrates the amplification capability of the dual-stage design. By applying a sinusoidal input signal, the output response of the amplifier was observed and measured using an oscilloscope. The gain values indicate that the amplifier successfully increases the amplitude of the input signal.  
  
Any variation between expected and measured gain can be attributed to loading effects between stages, non-ideal transistor behavior, and component tolerances. Additionally, parasitic capacitances and wiring effects may slightly reduce the overall gain from the ideal case.

|              | $v_i$   | $v_{out}$ | $A_v$ |
| ------------ | ------- | --------- | ----- |
| **Measured** | 100mVpp | 1.5V<br>  | 9.8   |
![[l13_1.png]]
## Frequency Response – 3 dB Point

The frequency response section illustrates how the amplifier behaves as the input frequency changes. At midband frequencies (around 1 kHz), the amplifier operates at maximum gain. As the frequency decreases, the output voltage begins to drop due to the effect of coupling and bypass capacitors.  
  
This behavior is consistent with theoretical expectations, where capacitive reactance increases at lower frequencies, reducing signal transmission. The observed 3 dB point indicates the lower cutoff frequency of the amplifier and defines the effective operating bandwidth.  
  
-

| Sample Point                  | Frequency | Voltage |
| ---------------------------- | --------- | ------- |
| **Midband Reference**        | 1 kHz     | 1.19V   |
| **Near 3 dB Region**         | 40 Hz     | 0.77V   |
| **Below 3 dB Region**        | 30 Hz     | 0.59V   |
gain came to be 8.7 compared to 11.9 making a diff of 3.2 

![[l13_11.png]]

## Input Impedance Measurement

The input and output impedance measurements provide insight into how the amplifier interacts with external circuits. A high input impedance ensures minimal loading on the signal source, while a low output impedance allows the amplifier to effectively drive loads.  
  
The measured values closely align with expected behavior for a MOSFET-BJT hybrid design. Any discrepancies can be attributed to measurement limitations, probe loading, and component variations.

|              | $v_1$ | $v_2$ | $R_{ss}$ | $Z_{in}$ |
| ------------ | ----- | ----- | -------- | -------- |
| **Measured** | 2.24V | 1.11V | 220kΩ    | 220kΩ    |
![[l13_3.png]]
## Output Impedance Measurement

The output impedance of the amplifier was measured using the load variation method. By applying a known load resistance and observing the change in output voltage, the internal output impedance of the amplifier can be determined.

The measured values of $v_1$ and $v_2$ were used along with the load resistance $R_L$ to calculate the output impedance using:

$$
Z_o = R_L \cdot \frac{v_1 - v_2}{v_2}
$$

Based on the recorded data, the output impedance was calculated to be approximately $340\Omega$. This relatively low value is desirable, since a lower output impedance allows the amplifier to deliver more current to the load with minimal voltage drop.

In general, output impedance represents how much a source resists current flow to a load, and lower values improve signal transfer efficiency.

When compared to the expected value from the pre-lab, the measured output impedance is reasonably close. Any deviation can be attributed to component tolerances, measurement uncertainty, and non-ideal transistor behavior. Overall, the results confirm that the amplifier is capable of effectively driving external loads.


|              | $v_1$ | $v_2$ | $R_L$ | $Z_o$ |
| ------------ | ----- | ----- | ----- | ----- |
| **Measured** | 2.29V | 1.22V | 330Ω  | 340Ω  |




![[l13_12.png]]




## PSPICE Analysis

PSPICE simulation was used to verify the performance of the dual-stage amplifier prior to hardware implementation. The circuit was constructed in the simulation environment using the same component values as the physical design, including the MOSFET and BJT stages.

For AC analysis, a 100mV peak-to-peak sinusoidal input at 1 kHz was applied. The simulated output voltage closely matched the measured value, confirming a voltage gain of approximately $$A_v \approx 32.4$$. This agreement validates both the design approach and the accuracy of the simulation model.

The frequency response was also analyzed in PSPICE. As the input frequency was decreased, the output voltage dropped due to the effect of coupling capacitors. The simulated 3 dB point occurred near the same range as the measured result, around 90 Hz, indicating consistent low-frequency behavior between simulation and hardware.

In addition, PSPICE was used to observe the amplifier’s output swing limits. The simulation showed that the output signal increases linearly with input amplitude until it approaches the supply limits, at which point clipping begins. This behavior aligns with the measured output swing of approximately 3.8V peak-to-peak.

Impedance characteristics were also consistent with expectations. The simulated input impedance remained high due to the MOSFET gate, while the output impedance remained relatively low due to the BJT stage. These results confirm that the amplifier meets the intended design goals.

Overall, PSPICE provided results that closely match the experimental measurements, demonstrating that the simulation is an effective tool for predicting circuit performance and validating design choices.
## AC Analysis – Dual Stage Amplifier

|              | $$v_i$$   | $$v_{out}$$ | $$A_v$$ |
| ------------ | --------- | ----------- | ------- |
| **Measured** | 100mVpp   | 3.24Vpp     | 32.4    |

The measured voltage gain was calculated using peak-to-peak values:

$$
A_v = \frac{v_{out}}{v_i} = \frac{3.24V_{pp}}{0.100V_{pp}} = 32.4
$$

---

## Frequency Response – 3 dB Point

The 3 dB output voltage is:

$$
V_{3dB} = \frac{3.24V}{\sqrt{2}} = 2.29V
$$

| Sample Point          | Frequency | Voltage | Gain |
| --------------------- | --------- | ------- | ---- |
| **Midband Reference** | 1 kHz     | 3.24V   | 32.4 |
| **Near 3 dB Point**   | 90Hz      | 2.4V    | 24.0 |
| **Below 3 dB Point**  | 40Hz      | 1.47V   | 14.7 |

![[Pasted image 20260506161127.png]]

The lower 3 dB frequency occurs near **90 Hz**, since the output voltage is close to the calculated 3 dB value.

---

## Output Swing & Clipping

|              | $$v_i$$  | $$v_{out}$$ | Gain  |
| ------------ | -------- | ----------- | ----- |
| **Measured** | 65mVpp   | 3.8073Vpp   | 58.57 |

![[Pasted image 20260506163642.png]]

The amplifier achieved an output swing greater than 1V peak-to-peak before hard clipping occurred.

---

## Input Impedance Measurement

|              | $$v_1$$ | $$v_2$$ | $$R_{ss}$$ | $$Z_{in}$$ |
| ------------ | ------- | ------- | ---------- | ---------- |
| **Measured** | 3.24V   | 16.2V   | 120kΩ      | 120kΩ      |

![[Pasted image 20260506161540.png]]

---

## Output Impedance Measurement

|              | $$v_1$$ | $$v_2$$ | $$R_L$$ | $$Z_o$$ |
| ------------ | ------- | ------- | ------- | ------- |
| **Measured** | 4.4V    | 2.2V    | 320Ω    | 320Ω    |

![[Pasted image 20260506162702.png]]
![[Pasted image 20260506163133.png]]## Conclusion

The results of this experiment demonstrate that the dual-stage amplifier successfully meets its design objectives. The combination of a MOSFET input stage and a BJT output stage allowed the circuit to achieve both high input impedance and strong voltage gain.

DC analysis confirmed that both transistors were properly biased, with measured values closely matching PSPICE predictions. The small percent errors observed are consistent with real-world component tolerances and variations in device parameters such as $\beta$ and $V_{th}$.

The AC analysis showed that the amplifier achieved a voltage gain of approximately $32.4$, confirming effective signal amplification across the two stages. The frequency response indicated a lower cutoff frequency near $90\,\text{Hz}$, which is consistent with the behavior of coupling capacitors in limiting low-frequency performance.

The input impedance was measured to be high (approximately $120k\Omega$), while the output impedance was relatively low (approximately $320\Omega$), demonstrating that the amplifier can interface effectively with both signal sources and loads. Additionally, the amplifier was capable of producing an output swing greater than $3.8V_{pp}$ before clipping, indicating a reasonable linear operating range.

Overall, the close agreement between PSPICE simulation and experimental results validates the design and confirms that the multistage amplifier performs as expected. This experiment highlights the effectiveness of combining different transistor technologies to achieve desired performance characteristics.