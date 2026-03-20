Theory

Block diagram - ignore
Back ground  // 
GPTM - details 
- timer0 timerA 
Register config 
Mode init sequence
Timer 0A init
ISR config

Prelab

address offsets hex
peripherals

Procedure 
interrupt driver every 1 miilis 
	mod func
suser defined func 
udf call - handler 
timer isr 
udf creations
mod main - task set - 

measurements Osc 
img

global counter - seven segment display - 

project init 

TASKS
1 - counter speed - why it works - + how
To practice the use of interrupt timers and 
2 - T_1A IDD 
3 - T_1A IDVerify 
4 - O Probe test 

Questions 
1. use cases for GPTM 
2. T_0A - programs
3. key features of GPTM + modes
4.  bit GPTM A to change count direction
5. explain lab demonstation  and the concept of concurrency and advantages of periodic interrupts over polling 
6.. 
```
void Timer_0A_Periodic_Task(void)
{
    Timer_0A_ms_elapsed++;

    if (Timer_0A_ms_elapsed >= 200)
    {
        Timer_0A_ms_elapsed = 0;
        GPIOB->DATA ^= 0x01;
    }
}
```


6. 