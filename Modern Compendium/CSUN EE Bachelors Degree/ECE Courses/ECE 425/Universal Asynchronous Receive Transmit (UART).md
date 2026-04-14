#Dirty 

# Initialization Process
1. Enable UART Clock 
2. Enable GPIO Port 
3. Set the GPIOAFSEL
	1. ![[Pasted image 20260413175106.png]]
	![[Pasted image 20260413175244.png]]
4. Clear the PMCN field using the GPIOPCTL before config 
5. write the encoding value to GPIOPCTL reg to configure pins as UART 
6. ENable Digital funcitonality using GPIODEN

7. Diable UART by clearing the UARTEN in the UARTCTL reg
8. Specift the UART Clock souurce using the UARTCC
9. Configure the speed of the UART module by setting or clearing HSE bit in the UARTCTL register
10. Calculate Baud rate BRD then write integer and fractional portions
11. Configure the desired serial parameters using UARTLCRH
12. Enable UART by setting the UARTEN but un the UARTCTL register

## UART Checklist 

- [ ] Enable the modules
> [!info]+ Specifics 
> - [ ] Enable the UART module (connect clock → UART)
> - [ ] Enable the GPIO Port (connect clock → pins)

- [ ] Route the GPIO
> [!info]+ Specifics
> - [ ] Select the correct pins (e.g., PA0 = RX, PA1 = TX)
> - [ ] Enable Alternate Function (AFSEL = 1)
> - [ ] clear pctl just in case 
> - [ ] Set PCTL to UART function (assign peripheral to pins)\
> - [ ] Refer to pg 1351 on the data sheet table 23-5
> 
> 💡 This is the “wiring step”  
> If wrong → pin acts like normal GPIO or wrong peripheral

- [ ] Set the Pin Behavior 
> [!info]+ Specifics
> - [ ] Enable Digital Function (DEN = 1)
> - [ ] Set Direction:
>   - RX → input
>   - TX → output
> - [ ] (Optional) Configure pull-ups if needed
> 
> 💡 This is the “electrical layer”  
> If wrong → signal won’t physically behave correctly

- [ ] Config The UART
> [!info]+ Specifics
> - [ ] Turn OFF the UART module (safe configuration)
> - [ ] Set Baud Rate (communication speed)
> 	- [ ] IBRD
> 	- [ ] FBRD
> - [ ] Set Frame Format:
>   - Data bit length 
>   - Parity
>   - Stop bits
> - [ ] Enable TX and RX paths
> - [ ] Turn ON the UART module
> 
> 💡 This is the “protocol layer”  
> Defines how bits are interpreted

- [ ] Check (optional)
> [!info]+ Specifics
> - [ ] Verify flags (TX ready, RX ready, not busy)
> - [ ] Confirm data is transmitting/receiving
> - [ ] Debug by checking each layer:
>   - Clock (RCGC)
>   - Routing (AFSEL/PCTL)
>   - Behavior (DEN/DIR)
>   - Config (UART settings)
> 
> 💡 Debug rule:
> Work **top-down through layers**, not randomly

