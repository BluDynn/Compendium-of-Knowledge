This should the config although the char and other functions can be replaced and modfied. Simply put all thats neccesary is the packet recieve data nad the stop bit data. 

when reading the FS-iA6B UART 
you would wait for the header byte, which is `0x20` // `0100 0000`then make sure its followed by `0x40` // `1000 0000` if the mesage is not the continue to wait. if it is enable the read mode and consider the next 32 bytes which is the packet.  

```cpp
//struct definition for reading 

struct FS32BYTES{
int CH1;
int CH2;
int CH3;
int CH4;
int CH5;
int CH6;
int CH7;
int CH8;
int CH9;
int CH10;
} FSiA6B


FSiA6B.CH1 

```

```cpp
/**
 * @file UART1-FS-iA6B.c
 *
 * @brief Source code for the UART1 driver thtat communicates with the FS-iA6B receiver.
 *
 * This file contains the function definitions for the UART1 driver.
 **
 * @note Assumes that the frequency of the system clock is 50 MHz.
 *
 * @author Daniel Jeorge Adrayan
 */

#include "UART1.h"
//YOU LAST WROTE HERE =========================================================================================================

void UART1_Init(void)
{
    // Enable clocks for UART1 and Port B
    SYSCTL->RCGCUART |= 0x02;
    SYSCTL->RCGCGPIO |= 0x02;

    // Small delay to allow clocks to stabilize
    volatile uint32_t delay = SYSCTL->RCGCGPIO;
    (void)delay;

    // Disable UART1 during configuration
    UART1->CTL &= ~0x0001;

    // Use system clock / 16
    UART1->CTL &= ~0x0020;

    // Baud rate for 50 MHz clock, 115200 baud
    // BRD = 50,000,000 / (16 * 115200) = 27.1267
    // IBRD = 27
    // FBRD = round(0.1267 * 64) = 8
    UART1->IBRD = 27;
    UART1->FBRD = 8;

    // 8-bit, no parity, 1 stop bit, FIFOs enabled
    UART1->LCRH &= ~0x7E;   // clear format bits first
    UART1->LCRH |=  0x70;   // WLEN=8-bit, FEN=1

    // Configure PB0 as U1RX and PB1 as U1TX
    GPIOB->AFSEL |= 0x03;
    GPIOB->PCTL  &= ~0x000000FF;
    GPIOB->PCTL  |=  0x00000011;
    GPIOB->DEN   |= 0x03;

    // Optional: disable analog on PB0/PB1
    GPIOB->AMSEL &= ~0x03;

    // Enable UART1, RX, and TX
    UART1->CTL |= 0x0301;
}

struct

char UART1_Input_Character(void)
{
    while ((UART1->FR & UART1_RECEIVE_FIFO_EMPTY_BIT_MASK) != 0);

    return (char)(UART1->DR & 0xFF);
}

void UART1_Output_Character(char data)
{
    while ((UART1->FR & UART1_TRANSMIT_FIFO_FULL_BIT_MASK) != 0);

    UART1->DR = data;
}

void UART1_Input_String(char *buffer_pointer, uint16_t buffer_size)
{
    int length = 0;
    char character = UART1_Input_Character();

    while (character != UART1_CR)
    {
        if (character == UART1_BS)
        {
            if (length)
            {
                buffer_pointer--;
                length--;
                UART1_Output_Character(UART1_BS);
            }
        }
        else if (length < buffer_size)
        {
            *buffer_pointer = character;
            buffer_pointer++;
            length++;
            UART1_Output_Character(character);
        }

        character = UART1_Input_Character();
    }

    *buffer_pointer = 0;
}

void UART1_Output_String(char *pt)
{
    while (*pt)
    {
        UART1_Output_Character(*pt);
        pt++;
    }
}

uint32_t UART1_Input_Unsigned_Decimal(void)
{
    uint32_t number = 0;
    uint32_t length = 0;
    char character = UART1_Input_Character();

    // Accepts until <enter> is typed
    // The next line checks that the input is a digit, 0-9.
    // If the character is not 0-9, it is ignored and not echoed
    while (character != UART1_CR)
    {
        if ((character >= '0') && (character <= '9'))
        {
            // "number" will overflow if it is above 4,294,967,295
            number = (10 * number) + (character - '0');
            length++;
            UART1_Output_Character(character);
        }

        // If the input is a backspace, then the return number is
        // changed and a backspace is outputted to the screen
        else if ((character == UART1_BS) && length)
        {
            number /= 10;
            length--;
            UART1_Output_Character(character);
        }

        character = UART1_Input_Character();
    }

    return number;
}

void UART1_Output_Unsigned_Decimal(uint32_t n)
{
    // Use recursion to convert decimal number
    // of unspecified length as an ASCII string
    if (n >= 10)
    {
        UART1_Output_Unsigned_Decimal(n / 10);
        n = n % 10;
    }

    // n is between 0 and 9
    UART1_Output_Character(n + '0');
}

uint32_t UART1_Input_Unsigned_Hexadecimal(void)
{
    uint32_t number = 0;
    uint32_t digit = 0;
    uint32_t length = 0;
    char character = UART1_Input_Character();

    while (character != UART1_CR)
    {
        // Initialize digit and assume that the hexadecimal character is invalid
        digit = 0x10;

        if ((character >= '0') && (character <= '9'))
        {
            digit = character - '0';
        }
        else if ((character >= 'A') && (character <= 'F'))
        {
            digit = (character - 'A') + 0xA;
        }
        else if ((character >= 'a') && (character <= 'f'))
        {
            digit = (character - 'a') + 0xA;
        }

        // If the character is not 0-9 or A-F, it is ignored and not echoed
        if (digit <= 0xF)
        {
            number = (number * 0x10) + digit;
            length++;
            UART1_Output_Character(character);
        }

        // Backspace outputted and return value changed if a backspace is inputted
        else if ((character == UART1_BS) && length)
        {
            number /= 0x10;
            length--;
            UART1_Output_Character(character);
        }

        character = UART1_Input_Character();
    }

    return number;
}

void UART1_Output_Unsigned_Hexadecimal(uint32_t number)
{
    // Use recursion to convert the number of
    // unspecified length as an ASCII string
    if (number >= 0x10)
    {
        UART1_Output_Unsigned_Hexadecimal(number / 0x10);
        UART1_Output_Unsigned_Hexadecimal(number % 0x10);
    }
    else
    {
        if (number < 0xA)
        {
            UART1_Output_Character(number + '0');
        }
        else
        {
            UART1_Output_Character((number - 0x0A) + 'A');
        }
    }
}

void UART1_Output_Newline(void)
{
    UART1_Output_Character(UART1_CR);
    UART1_Output_Character(UART1_LF);
}

```
