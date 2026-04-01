**1.** How many SSI modules are within the TM4C123GH6PM microcontroller? How many data bits can be supported by the SSI peripheral?  Refer to the _Synchronous Serial Interface (SSI)_ section of the Tiva TM4C123GH6PM Microcontroller Datasheet.

> There are 4 SSI modules within the board, with each SSI module supporting 4-16 bits for the data and 8 bits for the control message.


**2.** Review Section 15.3.1 (_Bit Rate Generation_) on page 954 of the Tiva TM4C123GH6PM Microcontroller Datasheet.  
How is the frequency of the SCLK signal defined? Which SSI registers and which bit fields are used?

> "The Serial bit rate is derived by divifing  down the input clock (SysClk). ... first divided by an even prescale value CPSDVST from 2 to 254, which is programmed in the **SSI CLOCK PRESCALE (SSICPSR)** register. ... further divided by a value from 1 to 256 which is **1 + SCR** which is programmed in the SSI control0 (SSCCIR0) register""
> 
> ... oh theres the equation right under this quote...
> "The frequency of the output clock SSInClk is defined by: 
> ```
> SSInClk = SysClk / (CPSDVSR * (1+SCR))
> ```
> "
> 
> or in a prettier view, $$\frac{\text{SysClk}}{(~CPSDVSR~ *~(1+SCR) )}= SSInClk$$ 
> with SSICPSR(CPSDVSR) and SSICR0(SCR) relating to the clock rate 
> 

**3.** Which bits in the SSICR0 register are used to configure the following:

- Clock phase: 
- Clock polarity:
- SSI frame format: 
- Data length: 

Refer to pages 969–970 of the Tiva TM4C123GH6PM Microcontroller Datasheet.
> 
> clock phase; bit 7
> clock polarity: bit 6
> SSI frame format: bit 5:4
> Data Length: bit 3:0

## 4. SSI Register Map

List the address offsets in hexadecimal format and the descriptions for the following SSI registers. Include the register access type (read-write, write-only, or read-only).  
_Refer to Table 15-2 (SSI Register Map) in the datasheet._

| Register | Address Offset | Access Type | Description                                                       |
| -------- | -------------- | ----------- | ----------------------------------------------------------------- |
| SSICR0   | 0x000          | R/W         | Data size format clock polarity and clock rate, basic config      |
| SSICR1   | 0x004          | R/W         | Enables SSI, Master/Slave mode selection                          |
| SSIDR    | 0x008          | R/W         | Data Register for Transmitting and Receiving                      |
| SSISR    | 0x00C          | R           | "Status Register" busy and FIFO flags                             |
| SSICPSR  | 0x010          | R/W         | Clock Prescale register - controls prescale divisor of SSI clock. |
| SSICC    | 0xFC8          | R/W         | Clock config/clock selection                                      |
## 5. GPIO Alternate Functions (SSI)

For each alternate function, provide the pin name and the GPIOPCTL PMCx bit field encoding value.  
_Refer to Table 23-5 (GPIO Pins and Alternate Functions)._

| Alternate Function | Pin Name | GPIOPCTL PMCx Value |
| ------------------ | -------- | ------------------- |
| SSI0Clk            | PA2      | 2                   |
| SSI0Fss            | PA3      | 2                   |
| SSI0Rx             | PA4      | 2                   |
| SSI0Tx             | PA5      | 2                   |
| SSI2Clk            | PB4      | 2                   |
| SSI2Fss            | PB5      | 2                   |
| SSI2Rx             | PB6      | 2                   |
| SSI2Tx             | PB7      | 2                   |
