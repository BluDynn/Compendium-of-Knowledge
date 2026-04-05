Jayden Silpachai, Daniel Adrayan
Group #6
March 24, 2026

Experiment 5 Prelab: LCD
LCD Menu
### 1. Explain the purpose of the Register Select (RS) pin on the HD44780 LCD controller. In addition, describe the function of the Read-Write (R/W) pin. 

>[!tip] Answer 
>The HD44780's Register Select pin selects between two registers, The instruction register and the data register. As for the read or write pin, it selects what mode the selected register performs in. With the instruction register, when in write mode it writes to the Instruction Register while in read mode it acts as the Busy flag and Address Counter. With the Data register, the pin will act as expected reading and writing dependent on the pin setting. 
>> [!help] lmao i almost forgot to put the table for this 
>> ![[Pasted image 20260402170434.png]]
### 2. What two types of registers are present in the HD44780 LCD controller? Which register handles the received commands? Which register is responsible for handling data displayed on the LCD?

> [!tip] Answer
>

The two registers present in the HD44780 LCD controller are the instruction register and the data register. The IR (instruction reg. [^1]) stores the "received commands" or instruction codes. The DR (Data reg. [^1]) stores data to be written into and saved for display on the LCD.

### 3. What is the Enable (E) pin used for? According to the timing diagram shown in Figure 4.5-1, the enable signal must be set high for a specified period of time. During a read or write operation, what is the minimum time that the enable signal must be High?

>[!tip] Answer
The enable pin is used to initiate data transmission depending on the Read/ Write Pin. The enable pin should be high for as long as before the data is transmitted and turned off before the next message... acording figure 4.5-1, i didnt see it, but according to the bus timing characteristics on the data sheet, the high level pulse width is 450ns for both read and write with a minimum 1000ns before the next enable. 
> 
### 4. Describe the purpose of each bit (i.e. D, C, and B) in the Display On / Off Control command.

> [!tip]
> ![[Pasted image 20260402172430.png]]
> 
> D - sets the display on or off 
> C - cursor on or off
> B - Cursor Blink on or off 

[^1]: for those new in chat, if you didnt know reg is short for register 



