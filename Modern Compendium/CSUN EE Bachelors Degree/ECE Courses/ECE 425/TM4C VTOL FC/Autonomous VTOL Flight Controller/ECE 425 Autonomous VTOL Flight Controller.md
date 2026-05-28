
# Premise
 In the modern scene of hobby level remote control electronics, devices are configured to be plug and play drones or planes. This is great for beginners looking to have a Lego like experience, being able to create the plane of their dreams and learn and experiment with the idea of flying objects. However for those that are interested in the lesser conventional flight configurations, such as the VTOL, they are heavily limited to premade kits that do not allow for customization. Ontop of this most affordable hobby grade drone flight controllers do not allow for smart control such as hover or smart modes. 
# Solution
To solve this issue the creation of a DIY instruction kit to construct such a flight controller will be done. 

# Requirements 
This project will be utilizing a capable microcontroller that can process and carry out instructions with precision. In this case the TM4C123G LaunchPad will be utilized . The RC controller being utilized is the __ I forgot the name will change soon. 

This Project will consist of two members and therefore two sections, this is to maximize team efficiency and to ensure both members will have something to work on. 

## Primary Flight Controller - Daniel Focused
> A lot more Physically implemented

The primary section will involve the TM4C123G microcontroller in conjunction with the MPU6050 IMU devboard, and sets of motors and servos for the control services. The board will act as the primary flight controller, operating between two modes. Vertical Flight Mode and Standard Flight Mode. These modes will be referred to as VF Mode and SF Mode. As expected VF Mode will act synonymously as a drone, allowing for vertical take off, hover, and lateral movement. While in SF Mode the flight controller will act as a standard RC plane, allowing the user to control pitch, yaw, and roll directly. 

The board will communicate with an FLYSKYi6AB wireless receiver in Serial Communication mode. The Wireless receiver will simply allow for serial communication between the user's remote controller to operate the device. 

The Primary focus of the Primary Module is the stabilization and motor control of the device. It will simply receive instructions from the gyro board and keep the device stable. To put the process simply, it reads the IMU data and outputs neccesary motor control to stablize the the device, while also listening to wirelessly received instructions. 

[[425 UART1 Config FS -iA6B]]
# Secondary Telemetry Device - Miko Focused 
> Its more software ended lmao

%% Miko you gotta hear me out man this is going to either sound really complected or really simple, either way this is doable with probably 2 good nights of work and an energy drink. If you really don't think its possible get me a bottle of soju and lemme at it. This is something i personally really want to do and would have fun with so i wouldn't mind doing it. 
%%

The Secondary section will involve a secondary TM4C123G in conjunction with a %%miko i swear its alot easier than it sounds pls pls pls dont be scared by it%% LoRa communication device %%here it is%% and a custom N x M LED matrix for visualization of sensor data and device positioning. The Secondary module will simply be connected up to the primary board to communicate through UART. As for the N x M LED it will simply read the changes in the IMU data and output a radar like positioning view, showcasing the drones' position vector. 

# Component List 
 ok i think the adhd hyperfixation wore off for the night so ill just send a rough draft of what i have


%% pls follow this format for future editing %%

estimated weight: 

> [!info]+  TM4C123G MicroController
> Online Purchase link: no 
> Data Sheet: sometimes
> Custom Notes: 
> In Class MicroController board 

> [!info]+  FlySky iA6B transciver set 
> Online Purchase link: ober here
> Data Sheet: ober here
> Custom Notes: 

> [!info]+  Motor here
> Online Purchase link: ober here
> Data Sheet: ober here
> Custom Notes: 

> [!info]+  Motor Controller
> Online Purchase link: ober here
> Data Sheet: ober here
> Custom Notes: 

> [!info]+  Servos Here
> Online Purchase link: [Amazon Link](https://www.amazon.com/180%C2%B0Metal-Waterproof-Airplane-Helicopter-Mechanical/dp/B09JWK2GB3?th=1)
> Data Sheet: [Official Data Sheet]([https://soldered.com/productdata/2017/01/Soldered_MG995_datasheet.pdf](https://www.electronicoscaldas.com/datasheet/MG995_Tower-Pro.pdf?srsltid=AfmBOooptdz_Rzpbvkmlh-xSZvU5i-Ew5WyVLM8CQYWlQBGjg91YkkLK))
> Custom Notes: 

> [!info]+  RYLR896 LoRa Module (wireless transciver)
> ![General ISM > 1GHz LoRa™ Transceiver Module 820MHz ~ 960MHz Antenna Included Chassis Mount](https://mm.digikey.com/Volume0/opasdata/d220001/derivates/1/001/168/801/MFG_5487_RYLR896_sml%28200x200%29.jpg)
> 
> Online Purchase link: [DigiKey Link](https://www.digikey.com/en/products/detail/reyax/RYLR896/22145027)
> Data Sheet: [DigiKey Link](https://reyax.com//upload/products_download/download_file/RYLR896_EN.pdf)
> Custom Notes: 

> [!info]+  Leds ig (is this neccesary to write?)
> Online Purchase link: ober here
> Data Sheet: ober here
> Custom Notes: 

> [!info]+  Ovonic CAR 5000 mAh 11.1V 55.5mAh LiPo Batter
> ![[Pasted image 20260405151102.png|250]]
> Online Purchase link: [Ovonic Site]([https://www.ovonicshop.com/products/ovonic-11-1v-5000mah-3s-50c-lipo-battery-pack-with-xt60-plug](https://www.ovonicshop.com/products/ovonic-120c-11-1v-3s-5000mah-lipo-battery-with-trx-plug-for-slash-e-revo-udr-x-maxx?_pos=7&_sid=8f57b8e7b&_ss=r))
> 
> - I got off of amazon for ALOT cheaper oml
> 
> Data Sheet: N/A
> Custom Notes: 
> >Specifications of **3s lipo battery 5000mah***:  
> >- Brand: Ovonic   
>> - Chemistry: Li-polymer  
>> - Cells Number: 3S  
>> - Voltage(V): 11.1V   
>> - Capacity(mAh): 5000mAh   
>> - Discharge: 120C   
>> - Max Burst Discharge Rate (C): 240C   
>> - Discharge Plug: TRX Plug  
>> - Battery Weight(dev.20g): 356g   
>> - Battery Dimension: 154x43x26mm
> 
> fuck i have the CAR and I found that the AIR is just lighter...
> 10 grams lighter to be exact  


> [!info]+  IMU module
> ![[Pasted image 20260405153406.png|250]]
> Online Purchase link: ober here
> Data Sheet: [Official Data Sheet](https://cdn.sparkfun.com/datasheets/Components/General%20IC/PS-MPU-6000A.pdf)
> [Cirkit Designer Hobby Design](https://docs.cirkitdesigner.com/component/13d9720f-5d9e-6438-9ecd-58ce523757db/invensense-mpu6050)
> Custom Notes: 
> The 6050 is an outdated model... who knew hobby grade tech would advance so far in the past 6 years. All current documentation is hard to find wtf 

> [!info]+  LM2596 BuckConverter 
> ![[Pasted image 20260405161210.png|250]]
> Online Purchase link: [Ebay Link](https://www.ebay.com/itm/165419732687)
> lost amazon link
> Data Sheet: N/A 
> Custom Notes: 
> Feed back Regulator - safe to use once calbrated for a specific voltage, max voltage 35 V



> [!info]+  NeoPixel LED Array \[Optional\] fuck nah bro imma so ffr rewriting a library for ts will be ass and is its own project 
> Online Purchase link: ober here
> Data Sheet: ober here
> Custom Notes: 

> [!info]+  GPS module \[Optional\] awh hell nah probably not unless you get me drunk at 1am and give me the parts 
> Online Purchase link: ober here
> Data Sheet: ober here
> Custom Notes: 

> [!info]+  Template
> Online Purchase link: ober here
> Data Sheet: ober here
> Custom Notes: 

# Success Factors 

%% Template Call outs for later%%

> [!done]+ Thing We did that works
> yeah so we did this thing that works

>[!caution] Thing we did that kinda works 
>yeah so we tried this thing but compromomised 

> [!fail]+ 
> Yeah so we tried this thing and it didnt work

> [!bug]
> yeah so this thing we dont want can sometimes happen


# Risks

# Milestones + Schedule

> [!Todo] This is the todo list of challenges to face
> # ECE 425 Project Prototype Due Date May 5th 
> as of 4/4/2026 there is only a month left to complete the project 
> ## Week 1 - April 6 - 10 
> - [ ] Individual Modules Utilization
> 	
> 	#### Primary 
> 	- [ ] Transceiver UART
> 	- [ ] Motor Controller PWM 
> 	- [ ] Servo PWM Control 
> 	- [ ] IMU Communication 
> 	#### Secondary
> 	- [ ] Construction of LED Charlieplexing Matrix 
> 	- [ ] Testing of LED Charlieplexing Matrix
> ## Week 2 April 13 - 17 - I get Paid again
>  - [ ] Simplified T Frame Set Up Contstructed
>  - from this point on everything should be more software focused
> 	#### Primary 
> 	- [ ] Flight Drivers 
> 	#### Secondary
> 	- [ ] Construction of LED Charlieplexing Matrix 
> 	- [ ] Testing of LED Charlieplexing Matrix 
> 		- bro imma be so ffr this is probably the most conceptually challenging part of the project, which is exactly why i want to include this. Anyways this is the heavy part of your individual research. Search up ***Charlie-Plexing***
> ## Week 3 April 20 - 24  
> - This week i can hyper fixate like crazy to get the whole thing done
> - All extra time to solving the project
> ## Week 4 April 27 - May 1 - I get Paid Again
> - more extra time + Presentation Prep
> ## Week 5 May 4 - 5 _***PRESENTATION DAY***_
> 

# Constraints + Challenges

> [!warning] We are Very Ambitious
> but to be honest, if we spend a weekend hyper fixated on this like crazy we can make it.
> - I will state, I personally am a big fan of human written code as it lets me explain it better and feel more knowledgeable about what I did, but do not be afraid to use chat gpt as a resource. There should also be alot of libraries that we should be able to utilize but either way this class gave us the fundamentals to write out own libraries. Not that I want to but im not against using chat to modify libraries to work on the TM4C123G. 
> - Our Ambition may be high but I am cautious enough to not fly too close to the sun, by this, I purposely made our project title very vague, that we can be as ambitious as we want but we can also step down in areas that we would like. 
> - Time and balancing other classes, yeah ngl i plan on finishing this whole project in a few nights of ADHD hyperfixation so that way i can focus, plus this schedule i roughly set should help me limit myself to what I can do in a week.

# Project Members 

> [!info] Daniel Jeorge Adrayan
> This is a guy


> [!info] Miko Lacre
> This is also a guy

# Report - Primary Flight Controller 

The Primary Flight Controller board will be in charge of reading the user input and error correction from the MPU6050 gyro as well as the FS-iA6B reciever, and then outputting the PWM signals to control the servos and the motors. Though it may seem challenging, it was done through simple use of the on board UART PWM and I2C modules. most challenges coming from the implementation of all modules at once and the software ended driver configuration.  

## FS-iA6B UART communication 

The FlySky iA6B reciver module is a 10 channel reciever that ouputs pwm by standard, most hobbist utilize the pwm signals stright from the reciver to control rc devices such as planes, however to utilize this in a more complex enviornment the channels must be read and parsed. This is where a key part of the revicer comes in, the reciver allows for UART communication, able to connect to sensors and output channel data through uart. THe channel output communication of the reciver will be utilized. 

image here of UART oscilloscope reading 

due to a lack of easy to access documentation on how the reciever sends ouot the uart signals, the reciever was observed under an oscilloscope to understand how to read the signals. Upon inspectiong looking at that figure over there, the message that the reciver sends is a 32 byte (not bit) message. (slang incoming) for those new in chat a byte is a word consisiting of 8 bits, so to sya that 32 bytes were sent .. yknow, anyways with the oscilloscope reading, the initialization of the UART module was ready to be experimented with. From research and oscilloscope confirmation the following intialization settings were used on the board to develop a custom driver to communicate with the reciever. 

shows small snippet of code 

With this the channel data can be configured and parsed as follows. Simply by taking the message and knowing which bytes reffer to which channel allows for this to work.. 

shows more code 

To verify the use of the driver the main script was fitted with a debug mode that output all channel information to a serial monitor. 

show screen shot here 

## PWM configuration 

With the radio wireless configuration set, the PWM modules can be tested, utilizing a simple 12g servo connected to the board powered by a 5V rail from the reciever. From previous knowledge of how this shit works (sorry im brain dumping the format) the initialization had to go as follows 

shows code

the communication through pwm was not a simple 0 - 100 for the duty cycle so the ranges of the servos were tested, it was found that duty cycles from xx to xx was the 12g servos operating range, anything closer towards these values lead to a risk in burning the servo motors which happened once cause i was a dumbass. 

Moving from the servo test the motor escs were also tested, utilizinig a stray fixture from JD2201 and a custom 3d printed enclosure a motor was fitted and strapped down for testing with the esc, plugged similar to the servos. also like the servos, the esc operates within bounds for the duty cycle, for motors in this case was from xx to xx. 

picture of that here

With the PWM bounds configured, integration between wireless communication and PWM output was tested. by taking the channel data and knowing that channel data can range from a set value an eqaution of the sorts was used to convert the bounds of the channel data to the bounds of they duty cycle pwm data  $$\text{PWM duty cylcle output}=\left(\frac{\text{channel data}-\text{min channel data}}{\text{max channel data}-\text{min channel data}}\times \left(\text{max PWM bound}-\text{min PWM bound}\right)\right)+\text{min PWM bound}$$
allowing for the mapping of servo and motor control to the controller. This proved to be successful and opened the gates for wireless mechanical control. 

## MPU 6050 IMU I2C config 

The MPU6050 is a 6-axis Inertial Measurement Unit (IMU) that combines a 3-axis accelerometer and a 3-axis gyroscope to measure motion and orientation.

A useful way to understand how it works is by considering the constant downward vector of gravity. The accelerometer continuously measures acceleration along the x, y, and z axes, which includes the acceleration due to gravity. By observing how this gravity vector is distributed across the axes, the system can estimate the device’s tilt and orientation relative to the ground.

For example, if the device is perfectly level, gravity is primarily aligned with one axis. As the device tilts, the gravity vector “shifts” across multiple axes, allowing the system to infer pitch and roll.

The gyroscope complements this by measuring angular velocity (rate of rotation) about each axis. While the accelerometer provides an absolute reference (gravity), the gyroscope provides short-term rotational motion data, allowing for smooth and responsive tracking of movement.

Together, these sensors enable accurate estimation of orientation and motion when their data is combined.

All sensor measurements are stored internally in registers on the MPU6050, which can be accessed by a microcontroller through the I2C communication protocol.


### I2C Crash Course

#### Intuitive Understanding
I2C can be understood as a shared communication line where multiple devices are connected on the same two wires. Unlike SPI, which uses separate chip select lines for each device, I2C allows all devices to exist on a single “bus.”

A helpful way to think about this is through a room analogy:

- SPI is like shouting into different rooms. You first select a specific room (chip select), then broadcast your message. Only devices in that room hear it, but you need a separate room (pin) for each device. It’s structured, direct, but a bit resource-heavy.

- I2C is like everyone being in the same room. Instead of selecting a room, you call out a specific person’s name first: “Hey Liam,” and then deliver your message: “I love you.” Everyone hears it, but only Liam knows it’s meant for them—and only they responds.

In this way, I2C reduces wiring complexity by using only two lines (data and clock), while still allowing communication with multiple devices on the same bus.
#### Professional Understanding
Inter-Integrated Circuit (I2C) is a synchronous, serial communication protocol that utilizes two bidirectional lines: a Serial Data Line (SDA) and a Serial Clock Line (SCL).

Communication is initiated by a master device, which generates a **start condition** followed by a **7-bit or 10-bit address** corresponding to the target slave device. This address frame includes a read/write bit indicating the direction of data transfer.

Only the addressed slave device acknowledges and participates in the communication, while all other devices remain idle despite sharing the same bus.

Data is transmitted in byte-sized frames, each followed by an acknowledgment (ACK) bit. The communication concludes with a **stop condition**, signaling the end of the transmission.

This addressing scheme allows multiple slave devices to coexist on a single bus without requiring additional chip select lines, making I2C efficient in terms of pin usage and system complexity.


To test the usage of the board, a custom I2C driver was configured and implemented, in this case I I linked the gyroscope yaw vector to pwm duty cycle to showcase that it can interact with the rest of the system. from here the individual components were tested 

## Total System Integration 

