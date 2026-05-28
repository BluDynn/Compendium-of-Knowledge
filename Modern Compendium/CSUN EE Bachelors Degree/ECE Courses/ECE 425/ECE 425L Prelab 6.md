**

Jayden Silpachai, Daniel Adrayan

Group #6

April 14, 2026

# Experiment 6 Prelab: ADC

  
  

## 1. How many ADC modules are within the TM4C123GH6PM microcontroller? How many sample sequencers does each ADC module have? 

  

The TM4C has two ADC modules, ADC0 and ADC1 which are 12 bit analog to digital converter modules. Each ADC module has 4 sample sequencers, Sample sequencer 0 through Sample sequencer 3 for ADC0 and ADC1.

  

## 2. How many bits of conversion resolution does each ADC module have? How many input channels are supported by the ADC modules?

  

ADC0 and ADC1 both are 12 bit ADC’s so the ADC has 2^(12)  distinct voltage cases, 0 to 4095. The ADC has 64 input channels, determined by the input of 0 to 63 in the ADCPP register, in bit field 9:4. 

  

## 3. List the address offsets in hexadecimal format and the descriptions for the following ADC registers. Provide the register access type

  
  

|   |   |   |   |
|---|---|---|---|
|Register|Offset|Type|Description|
|ADCACTSS|0x000|RW|Active Sample Sequencer|
|ADCRIS|0x004|RO|Raw Interrupt Status|
|ADCISC|0x00C|RW1C|Interrupt Status and Clear|
|ADCEMUX|0x014|RW|Event MUX Select|
|ADCTSSEL|0x01C|RW|Trigger Source Select|
|ADCPSSI|0x028|RW|Sample Sequence Initiate|
|ADCCTL|0x038|RW|ADC Control|
|ADCSSMUX0|0x040|RW|SSI MUX 0|
|ADCSSCTL0|0x044|RW|Sample Sequence Control 0|
|ADCSSFIFO0|0x048|RO|ADC Sample Sequence Result FIFO 0|

  

## 4. What is the ADCACTSS register used for? What is the purpose of the ASENn bits as described in the ADCACTSS register?

  

ADCACTSS is the ADC Active sample sequencer which is used for the activation of the corresponding sample sequencer, and can be activated or deactivated independently. The ASEN# bit is used for the activation for the 4 individual ADC sample sequencers, 0 through 3.

**