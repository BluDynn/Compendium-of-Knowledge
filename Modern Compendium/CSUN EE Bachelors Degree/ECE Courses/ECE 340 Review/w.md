# Design of Multistage Amplifiers

**Course:** ECE 340L  
**Date:** May 6, 2026  

---

## 1. Introduction

In practical circuit design, a single-stage amplifier is often unable to meet multiple requirements such as high voltage gain, high input impedance, and low output impedance simultaneously. Multistage amplifiers solve this problem by combining different amplifier configurations, where each stage contributes a specific characteristic.

In this experiment, a dual-stage amplifier was designed using a MOSFET and a BJT. The MOSFET stage provides high input impedance, while the BJT stage provides voltage gain and output drive capability.

---

## 2. DC Analysis – BJT (PSPICE)

|                          | $$V_C$$ | $$V_B$$ | $$V_E$$ | $$V_{CE}$$ | $$V_{BE}$$ | $$V_{RE}$$ | $$I_E$$ |
| ------------------------ | ------- | ------- | ------- | ---------- | ---------- | ---------- | ------- |
| **Theoretical (PSPICE)** | 20V     | 8.648V  | 7.975V  | 12.025V    | 0.673V     | 7.975V     | 6.203mA |
| **Measured**             | 20V     | 8.1V    | 7.6V    | 12.54V     | 0.64V      | 7.6V       | 5.96mA  |
| **Percent Error**        | 0.00%   | 6.34%   | 4.70%   | 4.28%      | 4.90%      | 4.70%      | 3.92%   |

This data shows the DC operating point (Q-point) of the BJT stage. The measured values closely match PSPICE results with small errors (~4–6%), mainly due to transistor $$\beta$$ variation and resistor tolerances. The value of $$V_{CE}$$ confirms operation in the active region.

---

## 3. DC Analysis – MOSFET (PSPICE)

|                          | $$V_D$$ | $$V_G$$ | $$V_S$$ | $$V_{DS}$$ | $$V_{GS}$$ | $$V_{RD}$$ | $$I_D$$ |
| ------------------------ | ------- | ------- | ------- | ---------- | ---------- | ---------- | ------- |
| **Theoretical (PSPICE)** | 11.78V  | 6.377V  | 3.738V  | 8.042V     | 2.639V     | 8.22V      | 3.738mA |
| **Measured**             | 11.43V  | 6.34V   | 3.91V   | 7.52V      | 2.5V       | 8.61V      | 3.97mA  |
| **Percent Error**        | 2.97%   | 0.58%   | 4.60%   | 6.49%      | 5.27%      | 4.74%      | 6.21%   |

The MOSFET results show good agreement with PSPICE. Small deviations are due to variations in threshold voltage $$V_{th}$$ and transconductance $$g_m$$. The device is properly biased in the saturation region.

---

## 4. AC Analysis – Dual Stage Amplifier

|              | $$v_i$$   | $$v_{out}$$ | $$A_v$$ |
| ------------ | --------- | ----------- | ------- |
| **Measured** | 100mVpp   | 3.24Vpp     | 32.4    |

$$
A_v = \frac{v_{out}}{v_i} = \frac{3.24V_{pp}}{0.100V_{pp}} = 32.4
$$

The amplifier provides a gain of approximately 32.4, indicating strong amplification from the cascaded stages.
![[l13_1.png]]
---

## 5. Frequency Response – 3 dB Point

$$
V_{3dB} = \frac{3.24}{\sqrt{2}} \approx 2.29V
$$

| Sample Point          | Frequency | Voltage | Gain |
| --------------------- | --------- | ------- | ---- |
| **Midband Reference** | 1 kHz     | 3.24V   | 32.4 |
| **Near 3 dB Point**   | 90Hz      | 2.4V    | 24.0 |
| **Below 3 dB Point**  | 40Hz      | 1.47V   | 14.7 |

![[Pasted image 20260506161127.png]]

The cutoff frequency occurs near 90 Hz, where the output approaches the 3 dB level. This behavior is caused by coupling capacitors limiting low-frequency response.

---

## 6. Output Swing & Clipping

|              | $$v_i$$  | $$v_{out}$$ | Gain  |
| ------------ | -------- | ----------- | ----- |
| **Measured** | 65mVpp   | 3.8073Vpp   | 58.57 |

![[Pasted image 20260506163642.png]]

The amplifier produces an output greater than 3.8Vpp before distortion occurs, confirming a wide linear operating range.

---

## 7. Input Impedance Measurement

|              | $$v_1$$ | $$v_2$$ | $$R_{ss}$$ | $$Z_{in}$$ |
| ------------ | ------- | ------- | ---------- | ---------- |
| **Measured** | 3.24V   | 16.2V   | 120kΩ      | 120kΩ      |

![[Pasted image 20260506161540.png]]

The input impedance is high (120kΩ), confirming minimal loading on the input signal.

---

## 8. Output Impedance Measurement

|              | $$v_1$$ | $$v_2$$ | $$R_L$$ | $$Z_o$$ |
| ------------ | ------- | ------- | ------- | ------- |
| **Measured** | 4.4V    | 2.2V    | 320Ω    | 320Ω    |

![[Pasted image 20260506162702.png]]
![[Pasted image 20260506163133.png]]

The output impedance is approximately 320Ω, indicating the amplifier can effectively drive loads.

---

## 9. Conclusion

The multistage amplifier successfully meets design expectations. The DC analysis confirms proper biasing of both the MOSFET and BJT stages. The amplifier achieves a high voltage gain of 32.4, along with high input impedance and relatively low output impedance.

The frequency response shows a lower cutoff near 90 Hz, and the output swing exceeds 3.8Vpp before distortion. Overall, the design demonstrates effective use of a MOSFET-BJT hybrid configuration to achieve desired amplification and impedance characteristics.