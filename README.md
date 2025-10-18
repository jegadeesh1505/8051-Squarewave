# 8051 - SQUARE WAVE


## AIM:
Write a 8051 c program to generate a square wave with frequency of 50khz

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software

## PROGRAM:
```c
#include <reg51.h>

sbit sqWave = P1^0;

void main()
{
    unsigned char TH0_val = 0xFF;
    unsigned char TL0_val = 0xF6;

    TMOD = 0x01; 

    while(1)
    {
        TH0 = TH0_val;
        TL0 = TL0_val;
        TR0 = 1;          
        while(TF0 == 0);  
        TR0 = 0;          
        TF0 = 0;          
    }
}
```

### OUTPUT:

![to edit](https://github.com/user-attachments/assets/7d28b679-e591-4c97-ada6-d08d00431cd9)



### RESULT:
Thus the 8051 C program to generate a square wave with frequency of 50khz using keil was done and shown the output.




















































