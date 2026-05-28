## DC Analysis – BJT

|                          | $$V_C$$ | $$V_B$$ | $$V_E$$ | $$V_{CE}$$ | $$V_{BE}$$ | $$V_{RE}$$ | $$I_E$$ |
| ------------------------ | ------- | ------- | ------- | ---------- | ---------- | ---------- | ------- |
| **Theoretical (PSPICE)** | 20V     | 8.648V  | 7.975V  | 12.025V    | 0.673V     | 7.975V     | 6.203mA |
| **Measured**             | 20V     | 8.1V    | 7.6V    | 12.54V     | 0.64V      | 7.6V       | 5.96mA  |
| **Percent Error**        | 0.00%   | 6.34%   | 4.70%   | 4.28%      | 4.90%      | 4.70%      | 3.92%   |

---

## DC Analysis – MOSFET

|                   | $$V_D$$  | $$V_G$$  | $$V_S$$  | $$V_{DS}$$ | $$V_{GS}$$ | $$V_{RD}$$ | $$I_D$$   |
| ----------------- | -------- | -------- | -------- | ---------- | ---------- | ---------- | --------- |
| **Theoretical (PSPICE)** | 11.78V   | 6.377V   | 3.738V   | 8.042V     | 2.639V     | 8.22V      | 3.738mA   |
| **Measured**      | 11.43V   | 6.34V    | 3.91V    | 7.52V      | 2.5V       | 8.61V      | 3.97mA    |
| **Percent Error** | 2.97%    | 0.58%    | 4.60%    | 6.49%      | 5.27%      | 4.74%      | 6.21%     |

---

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
![[Pasted image 20260506163133.png]]