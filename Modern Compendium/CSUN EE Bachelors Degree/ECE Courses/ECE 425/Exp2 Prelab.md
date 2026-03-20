# Q1
**How many 16/32-bit timer modules are provided by the General-Purpose Timer Module (GPTM) peripheral? List the names of all the timers. Refer to the General-Purpose Timers section of the Tiva TM4C123GH6PM Microcontroller Datasheet.**

There are 6 16/32 timer modules, the names are as followed

1. Timer 0 
2. Timer 1
3. Timer 2 
4. Timer 3
5. Timer 4
6. Timer 5


Each of these timers have 2 sub timers, Timer A and Timer B. 

# Q2
**Which bits must be set within the RCGCTIMER register in order to enable the following modules: timer module 0 and timer module 1?**

0x03

# Q3 
**List the address offsets in hexadecimal format and the descriptions of the following GeneralPurpose Timer Module (GPTM) registers. Provide the register access type (read-write, write-only, or read-only). Refer to the General-Purpose Timers section (Table 11-12, Timers Register Map) of the Tiva TM4C123GH6PM Microcontroller Datasheet.**


| Register  | Address Offset | Access Type | Description                                                |
| --------- | -------------- | ----------- | ---------------------------------------------------------- |
| GPTMCFG   | 0x000          | RW          | Config register  - setting the structure of the module     |
| GPTMTAMR  | 0x004          | RW          | Mode Register - defines timer behavior                     |
| GPTMCTL   | 0x00C          | RW          | Control Register - Enable / disable - edge triggers        |
| GPTMIMR   | 0x018          | RW          | Interrupt Mask Register - which timers generate interrupts |
| GPTMMIS   | 0x020          | RO          | Interrupt Status Register                                  |
| GPTMICR   | 0x024          | W1C         | INterupt Clear Register - set 1 to clear                   |
| GPTMTAILR | 0x028          | RW          | Intverval Load Register -sets the starting count value     |
| GPTMTAPR  | 0x038          | RW          | Prescale Register - timing resolution                      |
| GPTMTAR   | 0x048          | RO          | Timer Register - counter value storage                     |
| GPTMTAV   | 0x050          | RW          | Value Register  - current timer value                      |
|           |                |             |                                                            |
# Q4
**For each timer peripheral listed, provide the interrupt request (IRQ) number and the name of the corresponding interrupt service routine (ISR). Refer to the startup_TM4C123.s startup file (which can be found in Keil) and Table 2-9 (Interrupts) of the Tiva TM4C123GH6PM Microcontroller Datasheet.**

| Peripheral | IRQ Number | ISR (Handler) Name |
| ---------- | ---------- | ------------------ |
| TIMER 0A   | 19         | Timer0A_Handler    |
| TIMER 0B   | 20         | Timer0B_Handler    |
| TIMER 1A   | 21         | Timer1A_Handler    |
| TIMER 1B   | 22         | Timer1B_Handler    |
| TIMER 5A   | 108        | Timer5A_Handler    |
| TIMER 5B   | 109        | Timer5B_Handler    |
