
# Premise
 In the modern scene of hobby level remote control electronics, devices are configured to be plug and play drones or planes. This is great for beginners looking to have a Lego like experience, being able to create the plane of their dreams and learn and experiment with the idea of flying objects. However for those that are interested in the lesser conventional flight configurations, such as the VTOL, they are heavily limited to premade kits that do not allow for customization. Ontop of this most affordable hobby grade drone flight controllers do not allow for smart control such as hover or smart modes. 
# Solution
To solve this issue the creation of a DIY instruction kit to construct such a flight controller will be done. 

# Requirements 
This project will be utilizing a capable microcontroller that can process and carry out instructions with precision. In this case the TM4C123G LaunchPad will be utilized along side a LoRa module for wireless communication. The RC controller being utilized is the __ I forgot the name will change soon. 

This Project will consist of two members and therefore two sections, this is to maximize team efficiency and to ensure both members will have something to work on. 

## Primary Flight Controller - Daniel Focused
> A lot more Physically implemented

The primary section will involve the TM4C123G microcontroller in conjunction with the MPU6050 IMU devboard, and sets of motors and servos for the control services. The board will act as the primary flight controller, operating between two modes. Vertical Flight Mode and Standard Flight Mode. For the sake of seeming cooler and more professional these modes will be referred to as VF Mode and SF Mode. As expected VF Mode will act synonymously as a drone, allowing for vertical take off, hover, and lateral movement. While in SF Mode the flight controller will act as a standard RC plane, allowing the user to control pitch, yaw, and roll directly. 

The board will communicate with two other control devices, an ESP-32 for wireless communication with the Secondary Component of the project, and an FLYSKYi6AB wireless receiver in Serial Communication mode. The Wireless receiver will simply allow for serial communication between the user's remote controller to operate the device. while the LoRa will be sending sensor data in packets and receiving instruction data. 

The Primary focus of the Primary Module is the stabilization and motor control of the device. It will simply receive instructions from the secondary, and keep the device stable. 
To put the process simply, it reads the IMU data and outputs neccesary motor control to stablize the the device, while also listening to wirelessly received instructions. 
l
# Secondary Telemetry Device - Miko Focused 
> Its more software ended lmao

%% Miko you gotta hear me out man this is going to either sound really complected or really simple, either way this is doable with probably 2 good nights of work and an energy drink. If you really don't think its possible get me a bottle of soju and lemme at it. This is something i personally really want to do and would have fun with so i wouldn't mind doing it. 
%%

The Secondary section will involve a secondary TM4C123G in conjunction with a %%miko i swear its alot easier than it sounds pls pls pls dont be scared by it%% LoRa communication device %%here it is%% and a custom N x M LED matrix for visualization of sensor data and device positioning. The Secondary module will simply be connected up to a computer program able to read and write serial data to the microcontroller, this allows for time scalable potential, if there is extra time in the project to do so the outcome can be as basic as simple position data to transmit to full AI control. The limit is endless. As for the N x M LED it will simply read the changes in the IMU data and output a radar like positioning view, showcasing the drones' position vector. 

# Component List 
 ok i think the adhd hyperfixation wore off for the night so ill just send a rough draft of what i have


%% pls follow this format for future editing %%

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
> 	- [ ] LoRa Communication
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

