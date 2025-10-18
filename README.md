# SQUARE WAVE


## AIM:
1.Write a 8051 c program to generate a square wave with frequency of 50khz

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software

## PROGRAM:
```
CLR P1.0
MOV TMOD, #01H
AGAIN:MOV TL0, #0F7H
MOV TH0, #0FFH
CPL P1.0
SETB TR0
WAIT:JNB TF0, WAIT
CLR TR0
CLR TF0
SJMP AGAIN
END
```

### OUTPUT:


### RESULT:
Thus the 8051 C program to generate a square wave with frequency of 50khz using keil was done and shown the output.

# SQUARE WAVE


## AIM:
2.Write a 8051 c program to generate a square wave with frequency of 50khz

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software

## PROGRAM:
```
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
![WhatsApp Image 2025-10-18 at 16 03 58_9c40ca54](https://github.com/user-attachments/assets/af08b577-f55e-494b-ade4-d4b2c175529c)

### RESULT:
Thus the 8051 C program to generate a square wave with frequency of 50khz using keil was done and shown the output.

