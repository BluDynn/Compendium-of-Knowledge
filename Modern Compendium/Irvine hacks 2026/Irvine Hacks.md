### Project Ideas 
Pickle Ball  Hardware
Car Trip monitor 


UI - implementation - placement data


Arduino Q - Board 

Piezo Electric Sensors - 
we will be utilizing an array of sensors to determine positioning. 


config 1 senses whole vibration and signal as the sensor generates due to mechanical variation 

update: i forgot that this works really fast, I get a normal high and a spike lol  still detectable but will test other config
![[Pasted image 20260227231308.png]]

config 2 - "spike detection" this would primarily read spikes in things - 
update: both configs act the same ... what 

![[Pasted image 20260227231328.png]]

overall the config as of 11:49pm would be the spike detection with a transistor to trigger an interrupt to enter a polling mode. 

 OR 

I could have all three be spike detection and each interupt ... all three would have to be spike detect to ensure we dont miss a signal- so essentially we have three interrupts... no cant do that cause of priority 

transitor edge interrupts- 
![[Pasted image 20260228005828.png]]


Esp 32 - prototyping ![[Pasted image 20260227231224.png]]




# DAY 2 

configure time stamping and multi piezo calculations
configure hardware implementations
figure out diode config 
skip transistor

Morning of 
configuring the code 
flow should run as follow 

interrputs set time stamp - calculate differences 

but how do we know when to calculate the differences 

opt 1 
polling, interval polling specifically. by just having a function call held within the main function it would call periodically and run as usual. 

opt 2 
Within the interupts - complex as its new to me - 
by sensing which interrupt is triggered last we can have that interrupt call the function to run the calculations


[[Devpost - Project Story Draft]]


# Key take aways 
Learn OpenGL - defying gravity google
Learn how to make an app 
