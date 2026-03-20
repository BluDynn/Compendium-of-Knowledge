Provide your answers to the following questions (5 points each) in a text document and
submit your file on Canvas. Code statements must be written in C. Use only the method
shown in both the lecture and the lab. No credit will be given if variable names that are not
supported by the TM4C123GH6PM.h header file are used. Acceptable formats
include .doc, .docx, and .pdf.


1. Write a statement that sets Bit 4 of the GPIODATA register for Port F to high. Assume that the GPIODIR register has already been configured.

	``` 
	GPIOF -> DATA |= 0x20; // address -> register
	// 0010 0000 
	```



2. Write a statement that clears Bit 1 and Bit 3 of the GPIODIR register for Port C to low.

	```
	GPIOC -> DIR  &= ~(0x09); // DIR 0000 1001 
	```
 

3. What is the purpose of the GPIO Digital Enable (GPIODEN) register? Write a statement that enables the digital functionality of the following pins: PD0 and PD2.

	The GPIODEN register enables digital GPIO of the port that it is registered under, this allows for pins to be read and written to. 

``` 
GPIOD -> DEN |= 0x05;  // 0101
```

4. Suppose that a push button is connected to the PC0 pin. Write a function that configures the PC0 pin as an input GPIO pin with pull-down resistors enabled.

```
//assuming no previous initialization has occured
void initC (){
SYSCTL -> RCGCGPIO |= 0x04; //init clock for pin C
GPIOC -> DIR &= ~(0x01); //input(0) output(1) direction 
GPIOC -> AFSEL &= ~(0x01); //clear the pin functions 0 - GPIO
GPIOC -> DEN |= (0x01); // sets it as a digital pin
GPIOC -> PDR |=(0x01); // PDR - Pull down registers PUR - pull up resistors

// its configured but it doesnt state to set its values in a var :P 
}

```



5. Suppose that two switches are connected to PA2 and PB4. Write a function that configures the PA2 and PB4 pins as input GPIO pins with pull-up resistors enabled.

```
	// am i assuming they have been initialized yet ;-; im going to assume not
	
	void initAB (){
		SYSCTL -> RCGCGPIO |= 0x03; //Enable Clocks for port A and B 
		GPIOA -> DIR &= ~(0x04); // set PA2 as input (0)
		GPIOB -> DIR &= ~(0x10); // set PB4 as input(0)
		
		GPIOA -> AFSEL &= ~(0x04);
		GPIOB -> AFSEL &= ~(0x10); //clear any pin functions
		 
		GPIOA -> DEN |= 0x04; 
		GPIOB -> DEN |= 0x10; //configure digital mode 
		
		GPIOA -> PUR |= 0x04;
		GPIOB -> PUR |= 0x10; // pupll ups 
		
		// do you want me to also put the function of reading the data?
		// it just states to initialize it lol
		
 		}
```

6. Suppose that two LEDs are connected to the PB1 and PD3 pins. Write a function that configures the PB1 and PD3 pins as output GPIO pins. Initialize the value of the pins to zero.

```
// in different ports :( 

void initBDLEDS (){ 
SYSCTL -> RCGCGPIO |= 0x0A; // 0 1010 - ports B and D 

GPIOB -> DIR |= 0x02; // input(0) output(1) direction 
GPIOD -> DIR|= 0x04; 

GPIOB -> AFESEL &= ~(0x02); // clear pin functions
GPIOD -> AFESEL &= ~(0x08);

GPIOB -> DEN |= 0x02; //set in digital mode
GPIOD -> DEN |= 0x08;

GPIOB -> DATA &= ~(0x02); //initialize as 0
GPIOD -> DATA &= ~(0x08);

}
```


7. Explain what an interrupt is and the purpose of an interrupt service routine (ISR). What are the advantages of using interrupts as opposed to polling?

	An interrupt is a "hardware event mechanism" that temporarily pauses/suspends the normal program execution and run the interrupt service routine, which is essentially the function set by the user that is ran when the interrupt is called. Compare this to polling this allows for immediate action to be taken when a condition is met, best way to put it is to envision a phone call. Polling would be like if you were to put your attention towards watching your phone and waiting for a call, while an interrupt would be like you doing a task and then getting a phone call, stopping your task to take the phone call. In the terms of microcontrollers this allows for accurate timing of programs and reduces delays due to waiting for functions. 

8. Write a void function named PA_and_PD_Init that takes no arguments and initializes the following pins as GPIO pins with the specified direction.
• Inputs: PA0, PA2, PA4, PA6
• Outputs: PD1, PD3, PD5, PD7 

```
//sir why so many :( - jk i'll get it done 

void PA_and_PD_Init(){ 
SYSCTL -> RCGCGPIO |= 0x09; // 0 1001 - ports A and D 

// input(0) output(1) direction
GPIOA -> DIR &= ~0x55;  // 0101 0101 = 0x55 // 0 - input
GPIOD -> DIR |= 0xAA; // 1010 1010 = 0xAA // 1 - output 

GPIOA -> AFESEL &= ~(0x55); // clear pin functions
GPIOD -> AFESEL &= ~(0xAA); // 

GPIOA -> DEN |= 0x55; //set in digital mode
GPIOD -> DEN |= 0xAA;

GPIOA -> DATA &= ~(0x55); //initialize as 0

// no need  to config data for input pins
}

```


8. Write a uint8_t function named Get_PA_Status that takes no arguments and returns the
status of the push buttons connected to the given input pins: PA0, PA2, PA4, and PA6.
The function must not return the value of the other GPIO Port A pins.

```

uint8_t Get_PA_Status(){
// am i assuming pins have been initalized? im going to make that assumption.

return (GPIOA -> DATA & 0x55);

}


```