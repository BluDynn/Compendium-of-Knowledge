**Jayden Silpachai, Daniel Adrayan**

Group #6

April 14, 2026

  

# Eperiment 7 Prelab: DAC

  
  

###### 1. What is the purpose of a Digital-to-Analog Converter (DAC) in an embedded system? Explain how a DAC can bridge the gap between microcontrollers and analog signals.
    

  

With embedded systems, the DAC can serve as a bridge between the digital and the real analog world. Microcontrollers transmit data through digital signals, sending out bits and bytes and 0s and 1s. A DAC can serve as a “translator” turning digital signals into analog voltage outputs, this can be in specific voltage levels or specific waveform data. 

  
  

###### 2. The MCP4822 DAC requires a 16-bit configuration and data word to be transmitted over SPI. Describe the bits in the 16-bit word that are used to configure the DAC channel, gain, and shutdown control. Refer to the MCP4822 Datasheet
    

  

The 16 bit word that needs to be transmitted through SPI on the MCP4822 is composed of 12 bits for data and 4 bits for control. Bits 0:11 are used for the DAC value in 12 bits, bit 12 is a shutdown bit that refers to active or disabled, bit 13 refers to the gain of the output which is either 1x or 2x that of the digital value. Bit 14 is the Buffer control which determines if the reference voltage is buffered or unbuffered, and lastly bit 15 is the Channel select for the output pin.

  

###### 3.  Why is it important to match the SPI mode between the TM4C123GH6PM microcontroller and the MCP4822 DAC? What can go wrong if the SPI mode is mismatched?
    

  

Matching SPI modes is important not just for this specific module, but when utilizing any SPI communication module, if the SPI modes are not matched then there will be both reading and writing errors, this would lead to shifted bits, which leads to unintentional actions, which leads to a lab that lasts past 9:45, all of which are examples of things that can go wrong with the SPI mode. In all seriousness utilizing mismatched SPI modes leads to errors and can go from devices not working as intended, to not working at all due to data not being transmitted right.