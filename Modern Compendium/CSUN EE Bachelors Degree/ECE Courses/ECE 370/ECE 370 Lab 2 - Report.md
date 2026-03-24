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


# if it goes bad

 Considering the design process of the low-pass filter on a transmission line and comparing the constructed board to the simulated results, it is evident that there are noticeable discrepancies between the two. The simulated data shows a cutoff frequency near 2.5 GHz, while the measured data deviates from this behavior, indicating the impact of non-ideal factors introduced during fabrication. These differences highlight the importance of precision during construction, as small variations in physical dimensions, material properties, and soldering can significantly affect performance.

Although design in ADS provides a straightforward and idealized model, real-world implementation introduces sources of error that are not fully captured in simulation. As seen when comparing Fig. \ref{fig:Measrued S21} and Fig. \ref{fig.6}, the measured results exhibit additional noise, offset, and a peak at higher frequencies that is not present in the simulated response.

Despite the mismatch between simulated and measured data, the overall behavior of the filter remains consistent with design expectations, and valuable insights can still be drawn. The general trend of attenuation beyond the cutoff frequency is preserved, demonstrating that the underlying design methodology is valid, even if practical limitations affect accuracy.


# if its good 

Considering the design process of the low-pass filter on a transmission line, as well as the comparison between the constructed board and the simulated model, it is evident that precision during fabrication is critical. Although designing the filter in ADS is relatively straightforward, higher operating frequencies demand significantly greater accuracy in trace dimensions.

From the comparison between simulation and measured data, noticeable discrepancies are present, which can likely be attributed to imperfections in the physical construction of the filter. As shown in Fig. \ref{fig:Measrued S21} and Fig. \ref{fig.6}, the measured response exhibits both noise and offset relative to the simulated results.