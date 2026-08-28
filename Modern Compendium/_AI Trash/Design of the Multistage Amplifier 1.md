## 1. Common Emitter (CE) 
*Voltage Amplifier* 

- high voltage gain
- moderate current gain
- medium input impedance
- medium to high output impedance
- 180° phase shift
- commonly used as a main gain stage

**Use in multistage design**
- good when you need to significantly amplify a small signal
- often used in the first or middle stage


## 2. Common Collector (CC)  
*Buffer / Impedance Matching (Emitter Follower)*

- voltage gain ≈ 1  
- high current gain  
- high input impedance  
- low output impedance  
- no phase shift  
- does not significantly amplify voltage  

**Use in multistage design**
- used to prevent loading of previous stage  
- ideal for driving low-resistance loads  
- often placed at the output stage  
- commonly used after a CE stage  


## 3. Common Base (CB)  
*High-Frequency / Low Input Impedance Amplifier*

- high voltage gain  
- low current gain (≈ 1 or less)  
- low input impedance  
- high output impedance  
- no phase shift  
- excellent high-frequency response  

**Use in multistage design**
- used when bandwidth is important  
- useful in high-speed or RF circuits  
- not ideal for weak signals (due to low input impedance)  


## MOSFET


## 4. Common Source (CS)  
*Voltage Amplifier*

- high voltage gain  
- moderate current gain  
- high input impedance  
- medium to high output impedance  
- 180° phase shift  
- MOSFET equivalent of CE  

**Use in multistage design**
- used as a main gain stage  
- good for amplifying weak signals  
- often used in the first or middle stage  


## 5. Common Drain (CD)  
*Buffer / Impedance Matching (Source Follower)*

- voltage gain ≈ 1  
- high current gain  
- very high input impedance  
- low output impedance  
- no phase shift  
- MOSFET equivalent of CC  

**Use in multistage design**
- used to isolate stages  
- ideal for driving loads  
- often used as the final stage  
- prevents loading of previous stage  


## 6. Common Gate (CG)  
*High-Frequency / Low Input Impedance Amplifier*

- high voltage gain  
- low current gain  
- low input impedance  
- high output impedance  
- no phase shift  
- MOSFET equivalent of CB  

**Use in multistage design**
- used in high-frequency applications  
- useful when low input impedance is acceptable  
- sometimes used in cascoded designs  


## Equivalent pairs
- CE ↔ CS  
- CC ↔ CD  
- CB ↔ CG  


## Quick intuition
- Emitter / Source → gain stage (CE / CS)  
- Collector / Drain → buffer (CC / CD)  
- Base / Gate → high-frequency (CB / CG)  

>[!tip]- Differences From The Two Types of Transistor Amplifiers 
>"If they have similar use cases then whats the difference"
>
> > [!abstract]- CE vs CS (Voltage Amplifiers)
> > **Similarities**
> > - high voltage gain  
> > - 180° phase shift  
> > - used as main gain stage  
> >  
> > **Differences**
> > - CE (BJT): lower input impedance, requires base current, higher transconductance → typically higher gain  
> > - CS (MOSFET): very high input impedance, almost zero input current, lower transconductance, more sensitive to bias (VGS)  
> >  
> > **Key Idea**
> > - CE gives stronger gain per current  
> > - CS minimizes loading on the input source  
>
> > [!abstract]- CC vs CD (Buffers)
> > **Similarities**
> > - voltage gain ≈ 1  
> > - no phase shift  
> > - used for impedance matching  
> > - low output impedance  
> >  
> > **Differences**
> > - CC (BJT): high input impedance (but not extreme), requires base current, better current drive  
> > - CD (MOSFET): very high input impedance, almost zero input current, slightly weaker drive capability  
> >  
> > **Key Idea**
> > - CC is better for driving loads  
> > - CD is better for protecting sensitive inputs  
>
> > [!abstract]- CB vs CG (High-Frequency / Low Input Impedance)
> > **Similarities**
> > - high voltage gain  
> > - low input impedance  
> > - no phase shift  
> > - good high-frequency response  
> >  
> > **Differences**
> > - CB (BJT): higher transconductance → stronger gain, requires input current, often better high-frequency performance  
> > - CG (MOSFET): lower transconductance, no input current, easier voltage interfacing  
> >  
> > **Key Idea**
> > - CB is stronger (gain + speed)  
> > - CG is easier to interface with voltage signals  

# Experiment 13 - Design of the MultiStage Amplifier

*  𝑍𝑖 ≥ 100𝐾Ω
-   𝑍𝑜 = 620Ω ± 10%
-  Voltage gain, 𝐴𝑣 ≥ 5 with a 620Ω load
-  Output voltage swing of at least 1V peak-to-peak across 620Ω load
-  Power supply 𝑉𝐶𝐶 = 20𝑉
-  Low end cutoff frequency ≤ 40 Hz. You may use any configuration you wish.


Ive simply decided to continue with the common source and Common Collector due to list of reasons as follows:
**Common Collector** - stage 1
- easier to set input impedance and bias
- output impedane is also relatively easy
- Biasing process and caluclations are straight forward
- Voltage gain is simple
**Common Source** - stage 2 
****

*  𝑍𝑖 ≥ 100𝐾Ω - considered in stage 1
-   𝑍𝑜 = 620Ω ± 10% - considered in second stage
-  Voltage gain, 𝐴𝑣 ≥ 5 with a 620Ω load - considered in stage 1 
-  Output voltage swing of at least 1V peak-to-peak across 620Ω load 
-  Power supply 𝑉𝐶𝐶 = 20𝑉
-  Low end cutoff frequency ≤ 40 Hz. You may use any configuration you wish.
## Stage 1 - Common Source 
The most important parts of this stage is getting input impedance set, getting a gain greater than 5, and then making our output impedance relatively low. 

equations to be considered - 

## Stage 2 - Common Collector 
This stage is getting a input impedance that is higher than the previous output impedance and adjusting the output impedance to operate as desired. 