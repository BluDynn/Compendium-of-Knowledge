
## Implementation 
# Hardware Implementation 
2 Modules
- 4 generators and a control block 
- module contains 8 outputs 

Total 16 PWM possible outputs 

Initialization process is as per usual 
consider the config settings

> Timer Modes 
> - Count Down mode  // Left/Right Aligned Signals
> 	- Count down and reset timer
> - Count up/down mode // Center Aligned Signals 
> 	- Count down then back up timer


Key init 
RCGCPWM
GPIOx -> AFSEL
GPIOx -> PCTL
GPIOx // usual pin output set up 

PWMx -> ENABLE 