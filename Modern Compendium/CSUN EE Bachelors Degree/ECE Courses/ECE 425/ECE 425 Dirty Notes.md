# 2026-01-22
---
## Lecture Recap
 #ECE425 #LecRecap
## What Happened this session?
Straight forward discussion of computer architecture and the comparison of Microcontrollers and Microprocessors. 

## Key Take Aways:
{}

## What to Expect Next Session: 


# 2026-01-27
--- 
Late
missed content :
Address Bus
Data Bus


> [!tip] **Byte** 
> - smallest addressable unit for a processor
> - 8bit = 1 byte
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE425-Byte-Definition]


> [!tip] **Word** 
> - Natural size in which a processor is handling data 
> - = register size
> 	- 8bit processor (8bits = 1byte = 1word)
> 	- 32 bit processor (32 bits = 4byte = 1 word)
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE425-Word-Definition]
### Memory Space 
> [!tip] **Register** 
> - Storage Space in Microprocessor for ALU
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE425-Register-Definition]

> [!tip] **Cache** 
> - Temporary storage space in microprocessor chip for fast operations
> 	- optional fpr a microprocessor
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE425-Cache-Definition]

> [!tip] **RAM**
> - Temporary storage outside of Microproocessor
> - Random Allocated Memory
> - User Data
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECE425-RAM-Definition]

> [!tip] **ROM**
> - Memory for program code
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]
#### Operation Overview - Instruction Cycle
Fetch v
Decode v
Execution v

#### Comp Archetecture
> [!tip] **Von Neumann Architecture** 
> - busses are shared between data memory and program memory
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

> [!tip] **Harvard** 
> - Non Shared Busses
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

#### CISC vs RISC
> [!tip] ** Complex Instruction Set Computer(CISC)** 
> - one statment can do multiple things
> 	-  add + store
> 	- //x86
> - Emphasized on hardware (more transistors for set instructions)
> - includiing multi clock instruction
> - memory to memory (load and store are incorporated as an instruction)
> - Small memory use Size (small code size)
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]


> [!tip] **Reduced Instruction Set Computer (RISC)** 
> - two seperate instructions  
> 	- add
> 	- store
> - //ARM MIPS
> - increases instruction count but instructions are simpler
> - Emphassized on software (transistors for registers)
> - Single clock reduced instruction 
> - Register to Register (load and store are independent instructions)
> - Large memory use (large code size)
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

^b8a458


EX. 
**CISC** 
add 0x0001, 0x0001, 0x0004 - adds all bytes
- one instruction
**RISC** 
load $t0, 0x0001
load $t1, 0x0004
add $t2, $t0, $t1
store $t2, 0x0001
-many simple instructions
r ^00f03d

## What to Expect Next Session: 
Arm Archetecture 
+ more computer archecture and data sigs

# 2026-01-29
--- 
### What Happened Last Session?
covered basics of multiple data busses within the computer architecture. 

### What to expect this session?
ARM processors Architecture
Coverage on the Class based ARM Cortex-M Based MCU (TI TM4C123G)

## Lecture
#### What should you consider when choosing a MicroController
- ComputingPower
- Speed
- Power Consumption
- Ram + Rom
- numeber of I/O and types
- Budget 
- Internal Function
- IDE + Dev tools
#### ARM Cortex-M4
RISC architecture
- simple task instruction
RISC Archtecture 
- Seperate buses for program code and temp data
32 bit Mcu

#### ARM processors 
> [!tip] **Advanced RISC Machines** (ARM)
> - Simple intstruction based MCU
> - Optimized MCU for energy efficiency and low cost
> - Features bare metal programming 
> **Related Concepts**
> [[#^b8a458|RISC]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

> [!tip] **Memory Mapped I/O** 
> - The idea that peripherals, I/Os, and other devices are mapped to a memory address on the board. by utilizing the MCU to read addresses and write to addresses in memory allows one to communicate with the I/O pin. 
> - Dependent on the architecture of the MCU 

> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

##### Memory Map of TM4C123G
![[Pasted image 20260129132110.png]]

End of 02_Architecture 2-1.pptx

---

#Example #Prompt #ECEXXX
>[!warning] Example Problem: 
>![[Pasted image 20260129134452.png]]
>^[ECEXXX-ProblemTitle-Prompt]

$$
\begin{aligned}
Hexadecimal &\rightarrow Binary &\rightarrow Decimal
0x7C &\rightarrow ??&\rightarrow ??
\end{aligned}
$$
to be continued in cloud back up

---

# 2026-02-12
---
SHET I MISSED SO MANY CLASSES
## Recap : I/O Device control 
Isolated I/O vs Mem map control

Isolated I/O Micro Proc has to have individual lines and instructions 
Mem Map control has shared line and instructions

Example questions
 PD0 - PD 1 
 0000 0011 = 
 0x03
 should be writen
## Driver
 
... bro 425 makes me feel like im behind but im never actually behind.... 
---
---
# Catching up on classes
---

## Lec 8 GPIO  
- oh it looks like its a basic intro ... nvm i didnt miss much
HAHA yeah i really didnt miss much :D 
---

# 2026-02-17
---
## [[2026-02-17.pdf|Lecture Slide]]
GPIO initialization - refer to user guide 
GPIOAFSEL 
-- pre view
 GPIO Configuration
 Project initialization
 Output testing -debug
 Input initialization
  its all initialization :-;
-- end

GPIO RCGCGPIO register
![[Pasted image 20260217134225.png]]
GPIO DIR register 
![[Pasted image 20260217134158.png]]

GPIO AFSEL register
![[Pasted image 20260217134349.png]]

GPIO DIN register 
![[Pasted image 20260217135134.png]]

GPIO DATA register

![[Pasted image 20260217135200.png]]
Practice Exam Question


forgot to write it lmao

# 2026-02-18 - Prelab 
---
## Interrupts
some tasks can be scheduled, while some just respond to things when it happens. Interrupts allow the system to efficiently use processor time. 


> [!tip] **Interrupt** 
> - "hardware trigger, software action"
> - automatic transfer of software execution in response to hardware event that is asynchronous with the current sooftware execution. 
> - dum dum: an action that is done when the sensor trips 
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

compared to a busy wait task which actively checks a status to call for action, interrupts execute actions and "interrupt" the main script when the conditions are met. 
	To operate you must 
	setup
	1. arm the device - tell the device that hey this guy can interrupt you
	2. Enable the device specific "NVIC" nested vector interrupt controller - controls all interupts
	3. Global Enable bit - "I" bit = 0 
		used to turn all interupts on or off - main interrrupt flag
	4. Set priority from high(0-7)low
	event/main
	5. trigger 
ris -raw interrupt status


> [!tip] **Trigger** 
> - Hardware event that calls for an interrupt
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

> [!tip] **Thread** 
> - The path of action of software as it executes
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

# 2026-02-19 [[2026-02-19.pdf|Lecture Slides]]
---
Overview interrupts 

#Example #Prompt #ECEXXX
>[!warning] Disscussion: 
>Suppose you need to update your gpio to init 4 push buttons (SW5-2) on the eduboard instead of one push button. what steps do you need to take 
>assue that the push buttons use: 
>- sw5-pdo0
>- sw4-pdo1
>- sw3-pdo2
>- sw2-pdo3
>^[ECEXXX-ProblemTitle-Prompt]

| reg       | value hex | instruction |
| --------- | --------- | ----------- |
| RCFCGPIO  | 0x08      |             |
| GPIODIR   | 0x0F      |             |
| GPIOAFSEL | ~0x0F     |             |
| GPIODEN   | 0x0F      |             |
| GPIOPUR   | ~0x0F     |             |
| GPIOPDR   | 0x0f      |             |

## Lecture
> [!tip] **Polling** 
> - the process where the computer is actively checking the status before executing a proces
> - "is it active? lemme wait until it is active"
> **Related Concepts**
> \[\[Links here]]
> #definition #concept 
> ^[ECEXXX-Word-Definition]

spin polling -busy waiting

input pollong - checks eveytime it passes by


---
# 2026-03-05
---
## Exam Review - 30/50 
2's compliment - decode review - check my magnitude
Q2. - double check your use of && and || in if and bounds
 
