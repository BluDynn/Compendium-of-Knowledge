> [!info]+ SYSCTL - System Control (Root)
> Clock Gating - its in charge of enabling core modules and how they operate in different  clock modes 
> 
> > > [!warning]- Some good info
> >I suppose it is in good use that this gets explained, RCGC stands for Run Clock Gating Control. This essentially tells how the module clocks will act when the board is in the standard run mode. There also lies the SCGC and the DSCGC which is the sleep and deep sleep clock gating controls, similarly to the RCGC they control how the clocks operate in the respective modes. These are not covered in class and therefore will not be covered in my research until I feel like it. 
> 
> >[!abstract]- RCGC - Run Mode Clock Gating 
> > > [!info]- RCGCGPIO - General Pin Input Output 
> > > Controls GPIO ports no duh, but it controls the clock gate for GPIO  specifically. 
> > > - `bit 0 -> Port A`
> > > - `bit 1 -> Port B`
> > > - `bit 2 -> Port C`
> > > - `bit 3 -> Port D`
> > > - `bit 4 -> Port E`
> > > - `bit 5 -> Port F`
> > > 
> > > when using ANY  pins if that port clock is not enabled that shi will not react.
> > 
> > 
> > > [!info]- RCGCUART - Universal Asynchronous Receiver/Transmitter  
> > >  Controls the UART module Clock connection 
> > > - `bit 0 -> UART 0`
> > > - `bit 1 -> UART 1`
> > > - `bit 2 -> UART 2`
> > > - `bit 3 -> UART 3`
> > > - `bit 4 -> UART 4`
> > > - `bit 5 -> UART 5`
> > > - `bit 6 -> UART 6`
> > > - `bit 7 -> UART 7`
> > > If you dont have them enabled the UART modules will not work with your data
> >
> > > [!info]- RCGCCAN - Controller Area Network  
> > >  we dont use this in class why the fuck did you check it
> > >  ![[Pasted image 20260414102406.png|250]]
  > >
> > > [!info]- RCGCSSI - Synchronous Serial Interface (SPI)  
> > >  controls the clock gate for SSI modules
> > >  `bit 0 -> SSI0`
> > >  `bit 1 -> SSI1`
> > >  `bit 2 -> SSI2`
> > >  `bit 3 -> SSI3`
  > >
> > > [!info]- RCGCI2C - Inter-Integrated Circuit  
> > >  this was not in the notes bro who approved this
> > >  ![[Pasted image 20260414102406.png|250]]
  > >
> > > [!info]- RCGCTIMER - General Purpose Timers (16/32-bit)  
> > >  
  > >
> > > [!info]- RCGCWTIMER - Wide Timers (32/64-bit)  
> > >  i love how this was never mentioned even once
> > >  ![[Pasted image 20260414102406.png|250]]
  > >
> > > [!info]- RCGCADC - Analog to Digital Converter  
> > >  
  > >
> > > [!info]- RCGCPWM - Pulse Width Modulation  
> > >  we definitely did not spiritually cover this
> > >  ![[Pasted image 20260414102406.png|250]]
  > >
> > > [!info]- RCGCQEI - Quadrature Encoder Interface  
> > >  lmao why you checking things you know wont be on the exam
  > >
> > > [!info]- RCGCEEPROM - EEPROM  
> > >  bro are you gonna check all of these?
> > >  ![[Pasted image 20260414102406.png|250]]
  > >
> > > [!info]- RCGCDMA - Micro Direct Memory Access (uDMA)  
> > >  ur just wasting your time checking this
> > >  ![[Pasted image 20260414102406.png|250]]
  > >
> > > [!info]- RCGCHIB - Hibernation Module  
> > >  its not even relevant to what you want to study right now
> > >  ![[Pasted image 20260414102406.png|250]]
  > >
> > > [!info]- RCGCUSB - Universal Serial Bus  
> > >  yeah cause of course we studied this in class ... WE DIDNT  STOP CHECKING THIS
> > >  ![[Pasted image 20260414102406.png|250]]
  > >
> > > [!info]- RCGCWD - Watchdog Timers  
> > > ![[Pasted image 20260414102406.png|250]]
> 
> 
> > [!abstract]- SCGC -Sleep Mode Clock Gating 
> > you shouldnt have checked this its not in class
> >  ![[Pasted image 20260414102406.png|250]]

> [!info]- GPIOx
> Pin control (DIR, DEN, AFSEL, PCTL)
> GPIO is responsible for the behavior of the pins after being enabled by SYSCTL
>
> > [!abstract]- DIR - Direction  
> > Sets pin as input or output  
> > - `0 -> Input`  
> > - `1 -> Output`  
> 
> 
> > [!abstract]- DEN - Digital Enable  
> > Enables digital functionality of the pin  
> > - `0 -> Disabled`  
> > - `1 -> Enabled`  
> 
> 
> > [!abstract]- DATA - Data Register  
> > Used to read/write pin values  
> > - write → output  
> > - read → input  
> 
> 
> > [!abstract]- AFSEL - Alternate Function Select  
> > Chooses between GPIO and peripheral  
> > - `0 -> GPIO`  
> > - `1 -> Peripheral`  
> > 
> 
> 
> > [!abstract]- AMSEL - Analog Mode Select  
> > Enables analog functionality on a pin  
> > - `0 -> No analog function`  
> > - `1 -> Analog function enabled`  
> >
> 
> 
> > [!abstract]- PCTL - Port Control  
> > Selects which peripheral function the pin uses  
> > - 4 bits per pin  
> > - example: UART, CAN, etc.  
> 
> 
> > [!abstract]- PUR - Pull-Up Resistor  
> > Keeps pin HIGH when floating  
> 
> 
> > [!abstract]- PDR - Pull-Down Resistor  
> > Keeps pin LOW when floating  
> 
> 
> > [!abstract]- ODR - Open Drain  
> > Output can only pull LOW  
> 
> 
> > [!abstract]- DR2R / DR4R / DR8R - Drive Strength  
> > Controls output current strength  
> 
> 
> > [!abstract]- SLR - Slew Rate Control (optional)  
> > Limits rate of voltage change  
> 
> 
> > [!abstract]- IS / IBE / IEV / IM / RIS / MIS / ICR - Interrupts (optional)  
> > Handles interrupt configuration and status  
> 
> 
> > [!abstract]- LOCK / CR - Lock & Commit (optional)  
> > Allows modification of protected pins

> [!info]+ UARTx
> Responsible for the configuration and utilization of each UART module 
> > [!abstract]+ CTL - Control  
> > Turns UART on/off and enables TX/RX  
> > - enable module  
> > - enable transmit  
> > - enable receive  
> > 
> >  `bit 0 - UARTEN` // turn off before config
> >  `bit 8 - TXE` // auto set
> >  `bit 9 - RXE` //auto enabled
> > - 
> 
> 
> > [!abstract]- IBRD / FBRD - Baud Rate  
> > Sets communication speed  
> > - integer + fractional divider  
> 
> 
> > [!abstract]- LCRH - Line Control  
> > Defines data format  
> > - data length (5–8 bits)  
> > - parity  
> > - stop bits  
> > - consider each bit as a true or false statement
> > 
> > `bit 1 - Parity Enable (PEN)`
> > `bit 2 - Even Parity Select (EPS)`
> > `bit 3 - Stop Bits 2 (STP2)`
> > `bit 4 - FIFO Enable (FEN)`
> > `bits 5:6 - Word Length 5:8 (WLEN)` 
> 
> 
> > [!abstract]- DR - Data Register  
> > Used to send/receive data  
> > - write → transmit  
> > - read → receive  
> > 
> > - `bits 7:0 -> DATA` = actual data byte  
> > - `bit 8 -> FE` = Framing Error  
> > - `bit 9 -> PE` = Parity Error  
> > - `bit 10 -> BE` = Break Error  
> > - `bit 11 -> OE` = Overrun Error  
> > 
> > lower 8 bits = your data  
> > upper bits = error flags associated with that data  
>
> > [!abstract]- FR - Flag Register  
> > Status of UART  
> > 
> > - `bit 7 -> TXFE` = Transmit FIFO Empty  
> > - `bit 6 -> RXFF` = Receive FIFO Full  
> > - `bit 5 -> TXFF` = Transmit FIFO Full  
> > - `bit 4 -> RXFE` = Receive FIFO Empty  
> > - `bit 3 -> BUSY` = UART Busy (still transmitting)  
> > 
> > used to check if you can send or receive safely  
> 
> 
> > [!abstract]- IFLS - FIFO Level Select (optional)  
> > Controls when interrupts trigger based on FIFO level  
> 
> 
> > [!abstract]- IM / RIS / MIS / ICR - Interrupts (optional)  
> > Handles UART interrupt behavior  
> 
> 
> > [!abstract]- DMACTL - DMA Control (optional)  
> > Enables DMA usage with UART

> [!info]- SSIx
> Synchronous Serial Interface (SPI communication)
> Each SSIx is its own module (SSI0–SSI3)
>
> >[!abstract]- CR0 - Control Register 0
> >Sets the communication format
>> - `bits 15:8 -> SCR` = Serial Clock Rate
>> - `bit 7 -> SPH` = Serial Clock Phase
>> - `bit 6 -> SPO` = Serial Clock Polarity
>> - `bits 5:4 -> FRF` = Frame Format
>> - `bits 3:0 -> DSS` = Data Size Select
>
>> [!abstract]- CR1 - Control Register 1
>> Controls operation of the SSI
>> - `bit 4 -> EOT` = End of Transmission mode
>> - `bit 2 -> MS` = Master / Slave Select
>> - `bit 1 -> SSE` = SSI Enable
>> - `bit 0 -> LBM` = Loopback Mode
>
>> [!abstract]- DR - Data Register
>> Used to send and receive data
>> - `bits 15:0 -> DATA`
>
>> [!abstract]- SR - Status Register
>> Shows current SSI status
>> - `bit 4 -> BSY` = Busy
>> - `bit 3 -> RFF` = Receive FIFO Full
>> - `bit 2 -> RNE` = Receive FIFO Not Empty
>> - `bit 1 -> TNF` = Transmit FIFO Not Full
>> - `bit 0 -> TFE` = Transmit FIFO Empty
>
>> [!abstract]- CPSR - Clock Prescale Register
>> Sets the SSI clock prescaler
>> - `bits 7:0 -> CPSDVSR` = Clock Prescale Divisor
>
>> [!abstract]- IM - Interrupt Mask (optional)
>> Controls interrupt masking
>> - `bit 3 -> TXIM` = Transmit FIFO interrupt mask
>> - `bit 2 -> RXIM` = Receive FIFO interrupt mask
>> - `bit 1 -> RTIM` = Receive timeout interrupt mask
>> - `bit 0 -> RORIM` = Receive overrun interrupt mask
>
> >[!abstract]- RIS / MIS / ICR - Interrupts (optional)
>> Interrupt raw status / masked status / clear
>
>> [!abstract]- DMACTL - DMA Control (optional)
>> Enables DMA usage with SSI
>> - `bit 1 -> TXDMAE` = Transmit DMA Enable
>> - `bit 0 -> RXDMAE` = Receive DMA Enable
>
>> [!abstract]- CC - Clock Configuration (optional)
>> Selects SSI baud clock source
>> - `bits 3:0 -> CS` = Clock Source



> [!info]- TIMERx
> General timing / delays / counters

> [!info]- ADCx
> Analog to digital conversion


> [!info]- I2C (optional)
> Two-wire communication

> [!info]- CAN (optional)
> CAN bus communication

> [!info]- WTIMER (optional)
> Wide timers (larger range)

> [!info]- PWM (optional)
> Signal generation (duty cycle control)

> [!info]- QEI (optional)
> Encoder interface (position/speed)

> [!info]- EEPROM (optional)
> Non-volatile memory

> [!info]- DMA (optional)
> Memory transfer engine

> [!info]- HIB (optional)
> Low power / hibernation

> [!info]- USB (optional)
> USB communication

> [!info]- WATCHDOG (optional)
> System safety reset