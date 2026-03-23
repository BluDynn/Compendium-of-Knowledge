## Trouble Shooting
(mm)
W 3.087 L - 62.8975



W 25.634 L - 1.002 %%-- w-25.67 l-0.9989 --- %%

W 1.009 L - 9.051 %%-- w -1.048 l-9.007 --- %%

W 25.634 L - 3.741%% -- w-25.67 l-3.739 --- %%

W 1.009 L - 12.36 %%-- w-1.048 l-12.304 --- %%

W 25.633 L - 2.738 %%-- w-2.737 l- 2.73 --- %%

W 1.009 L - 3.313 %%-- w- 1.048 l-3.296830 --- %%



W 3.087 L - 62.8975

## Lab Report Requirements
- Include an introduction to microstrip stepped-impedance low pass filters.

w yannis
- Discuss your filter’s design specifications, the design procedure, important design equations, and a table showing the calculated characteristic impedances and lengths (in degrees and in mm) of each section of your filter.

	- Need to touch up design specifications Working

- Include a labeled schematic of your filter design and a high-quality photograph of your prototype.

	- Need to get image of prototype before submission 
	- Schematic of fiter design on upload

- Include a figure that shows the simulated filter’s |S11| and |S21| for the implementation with ideal transmission lines and with microstrip transmission line models. Discuss potential reasons for any differences.
	- Matlab compared to ADS 
- Show the measured and simulated |S11| and |S21| of the microstrip stepped-impedance LPF.
	- Matlab to ADS 
- State which VNA was used for measurements.
		-Got it DONE
- Discuss the simulation and measurement results and compare them with the design specifications.
	- End segment after ads sim is properly done
	- 
- Discuss potential reasons for any discrepancies in the simulated/measured performance as well as any possible design improvements.

	- 
- The lab report should be submitted through Canvas in PDF format prior to the start of next week’s lab.

## Calc corrections

The first step was to determine the number of elements (N). The ratio $f/f_c$ was calculated using the given frequencies. With $f$ = 3.0 GHz and $f_c$ = 1.4 GHz, the ratio is $f/f_c$ = 2.14. Using the expression $|f/f_c|-1$ the result is 1.14. Based on this value and the required attenuation, a minimum of (N = 6) elements is needed to meet the attenuation specification.

The next step was to simulate the low-pass filter using ideal transmission lines in ADS, as shown in Fig. 4. The shunt capacitor elements (TL1, TL3, and TL5) were implemented using low impedance lines with $Z_l$ = 10 $\Omega$, while the series inductor elements (TL2, TL4, and TL6) were implemented using high impedance lines with $Z_l$ = 87 $\Omega$. The value of $Z_h$ was chosen carefully to avoid excessively thin transmission lines, which would be difficult to fabricate.
