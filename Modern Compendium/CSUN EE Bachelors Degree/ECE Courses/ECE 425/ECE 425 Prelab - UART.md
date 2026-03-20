
## 4.5 Pre-Lab Assignment

---

## 1. UART Modules and Frame Format

How many UART modules are within the TM4C123GH6PM microcontroller?  How many data bits and stop bits can be supported by the UART module? Refer to the Universal Asynchronous Receivers / Transmitters (UARTs) section of the TM4C123GH6PM Microcontroller Datasheet.

> In the TM4C123GH6PM microcontroller there are 8 modules. Each module supports 5-8 data bits and up to 2 stop bits.

---

## 2. Baud-Rate Generation

Review Section 14.3.2 (Baud-Rate Generation) on page 896 of the TM4C123GH6PM Microcontroller Datasheet. How many bits does the baud-rate divisor have?  How can it be calculated?  Which UART registers are used?

> 
> The baud-rate divisor have 22 total bits across two registers: 16 bits for the integer portion and 6 bits for the fractional portion. The baud-rate divisor is calculated using
$$  
BRD = \frac{SystemClock}{16 \times BaudRate}  
$$


> The integer portion of the divisor is stored in the UARTIBRD (Integer Baud-Rate Divisor) register, and the fractional portion is stored in the UARTFBRD (Fractional Baud-Rate Divisor) register.

---

## 3. UARTLCRH Register Configuration

Which bits in the UARTLCRH register are used to configure the UART word length, the parity bit, the number of data bits the number of stop bits. Refer to pages 916–917 of the TM4C123GH6PM Microcontroller Datasheet.

> The UART word length is determined by bits 6 and 5, The parity enable bit is bit 1, the even parity select  is determined by bit 2, stick parity bit 7, and the number of stop bits is determined by bit 3. 

---

## 4. UART Register Map

List the address offsets in hexadecimal format and the descriptions for the following UART registers. Provide the register access type (read-write, write-only, or read-only). Refer to the Register Map section (Table 14-3, UART Register Map) of the TM4C123GH6PM Microcontroller Datasheet.

| Register | Address Offset (Hex) | Access Type | Description                                      |     |
| -------- | -------------------- | ----------- | ------------------------------------------------ | --- |
| UARTDR   | 0x000                | Read/Write  | Direction of data register - Transmit or Receive |     |
| UARTFR   | 0x018                | Reaad Only  | UART flag register                               |     |
| UARTIBRD | 0x024                | Read/Write  | "integer Baud rate divisor" -big number          |     |
| UARTFBRD | 0x028                | Read/Write  | "fractional baud rate divisor" - small number    |     |
| UARTLCRH | 0x02C                | Read/Write  | Line Control - Question#3                        |     |
| UARTCTL  | 0x030                | Read/Write  | UART control - UART/TXE/RXE - enable             |     |
| UARTCC   | 0xFC8                | Read/Write  | Clock Config                                     |     |

---

## 5. GPIO Alternate Functions for UART

For each alternate function listed below, provide the pin name and the GPIOPCTL PMCx bit field encoding value. Refer to Table 23-5 (GPIO Pins and Alternate Functions) on pages 1351–1352 of the TM4C123GH6PM Microcontroller Datasheet.

| Alternate Function | Pin Name | GPIOPCTL PMCx Bit Field Encoding Value |
|--------------------|----------|----------------------------------------|
| U0Rx               | PA0      | 1                                      |
| U0Tx               | PA1      | 1                                      |
| U1Rx               | PB0      | 1                                      |
| U1Tx               | PB1      | 1                                      |
| U1CTS              | PC4      | 1                                      |
| U1RTS              | PC5      | 1                                      |
| U2Rx               | PD6      | 1                                      |
| U2Tx               | PD7      | 1                                      |
| U3Rx               | PC6      | 1                                      |
| U3Tx               | PC7      | 1                                      |

---
