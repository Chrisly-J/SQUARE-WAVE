# SQUARE WAVE


## AIM:
1.Write a 8051 program to genrate a square wave with frequency of 50khz.

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
<img width="1178" height="873" alt="Screenshot 2025-10-18 165516" src="https://github.com/user-attachments/assets/f7f21eff-72d5-4137-8582-d171a9811809" />


### RESULT:
Thus the 8051 C program to generate a square wave with frequency of 50khz using keil was done and shown the output.



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
<img width="1338" height="755" alt="Screenshot 2025-10-18 170753" src="https://github.com/user-attachments/assets/d6d2f047-a133-4e7e-b0ef-ad1e89561bfe" />


### RESULT:
Thus the 8051 C program to generate a square wave with frequency of 50khz using keil was done and shown the output.

