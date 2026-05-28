## DC Analysis – BJT   
  
|                          | $$V_C$$ | $$V_B$$ | $$V_E$$ | $$V_{CE}$$ | $$V_{BE}$$ | $$V_{RE}$$ | $$I_E$$ |     |
| ------------------------ | ------- | ------- | ------- | ---------- | ---------- | ---------- | ------- | --- |
| **Theoretical (PSPICE)** | 20V     | 8.648V  | 7.975V  | 12.025V    | 0.673V     | 7.975V     | 6.203mA |     |
| **Measured**             | 20V     | 8.1V    | 7.6V    | 12.54V     | 0.64V      | 7.6V       | 5.96mA  |     |
| **Percent Error**        | 0.00%   | 6.34%   | 4.70%   | 4.28%      | 4.90%      | 4.70%      | 3.92%   |     |
  
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

Construct the rest of the dual stage amplifier and apply a 100 mV peak-to-peak, 1 kHz sine wave input. Use the oscilloscope to measure and record the input and output voltages. Calculate and record the amplifier’s voltage gain. Compare the amplifier gain to the one calculated in the pre-lab.

|              | $v_i$   | $v_{out}$ | $A_v$ |
| ------------ | ------- | --------- | ----- |
| **Measured** | 100mVpp | 1.5V<br>  | 9.8   |
![[l13_1.png]]
## Frequency Response – 3 dB Point

Calculate the output voltage that is 3 dB less than that measured in step 2. Slowly lower the signal generator frequency until the output voltage falls to this level. At various frequency intervals, record the output voltage. Use this data to graph the frequency response of the amplifier on log-log coordinates. Record the frequency where the output voltage falls by 3 dB.

| Sample Point                  | Frequency | Voltage |
| ---------------------------- | --------- | ------- |
| **Midband Reference**        | 1 kHz     | 1.19V   |
| **Near 3 dB Region**         | 40 Hz     | 0.77V   |
| **Below 3 dB Region**        | 30 Hz     | 0.59V   |
gain came to be 8.7 compared to 11.9 making a diff of 3.2 

![[l13_11.png]]

## Input Impedance Measurement

Measure the input impedance of your amplifier. Compare the measured input impedance to the one calculated in the pre-lab.

|              | $v_1$ | $v_2$ | $R_{ss}$ | $Z_{in}$ |
| ------------ | ----- | ----- | -------- | -------- |
| **Measured** | 2.24V | 1.11V | 220kΩ    | 220kΩ    |
![[l13_3.png]]
## Output Impedance Measurement

Measure the output impedance of your amplifier. Compare the measured output impedance to the one used in the pre-lab.


|              | $v_1$ | $v_2$ | $R_L$ | $Z_o$ |
| ------------ | ----- | ----- | ----- | ----- |
| **Measured** | 2.29V | 1.22V | 330Ω  | 340Ω  |




![[l13_12.png]]



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