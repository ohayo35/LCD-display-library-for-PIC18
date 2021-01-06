LCD LIBRARY FOR UP TO 4x20 discplay LCD modules
Tested on : 
2 x 16 display modules   LCD 1602
4 x 20 display modules   LCD 2004

Last update : 30/04/2020
Version : v4.1i
Target microcontroller : PIC18F27K42 or PIC18F26K83
LCD module : QAPASS 1602A  / LCD 2004
===================================================================================
LCD module connection to various boards based on PIC16 and PIC18 (28 and 40 pins)
===================================================================================
HPC curiosity : LCD LIBRARY for external 2x16 up to 4x20 display module

Expected result : LCD display will show a loopcounter incrementing each second
                  Terminal software on PC shows "Program started since xxxx seconds" & analog inputs
                  LEDs D2 to D5 will toggle every second

For the PIC18F27Kxx target microcontrollers it will be needed to add some wire straps
as there is no LCD module on HPC curiosity board.
Pins have been selected so that either the connections can be done on J8 & J11 
or use the click socket 1 as it wil NOT be usable
(*) Use the Click socket 2 for the USB <==> I2C/UART (MIKROE-1985) click board

1/ Please make the following connections on HPC curiosity board :
connect RA3 to LCD module pin E
connect RC2 to LCD module pin RW
connect RA1 to LCD module pin RS
connect RB1 to LCD module pin DB4
connect RB2 to LCD module pin DB5
connect RB3 to LCD module pin DB6
connect RB5 to LCD module pin DB7
2/ (*) Insert a MIKROE-1985 click board into the click 2 socket on HPC curiosity board
COnnect a USB cable between the click board and your PC 
Start a terminal software and search for the COM port. Program it with the following parameters :
Speed : 115200,8,N,1

(*) in case you have an HPC curiosity rev2 there is no need for MIKROE-1985 click board because 
rev 2 has an on board cirutal COM port (pins TX and RX below the ATMEL debug chip)
===============================================================================================
PICDEM 2 PLUS LCD LIBRARY FOR 2x16 display module

Expected result : LCD display will show a loopcounter incrementing
                  Terminal software on PC shows "Program started since xxxx seconds"

For the PIC18F26Kxx target microcontrollers it will be needed to add some wire straps
as the LCD module is only connected to PORTD from the 40 pin devices.

Please prepare the PICDEM 2 PLUS as follows :

1/ DISCONNECT the J6 jumper (the LEDs pins must be used by the LCD 4 bits databus)
2/ Make the following connections on connector J4 :
connector J4 connect RB0 to RD0     LCD DB4
connector J4 connect RB1 to RD1     LCD DB5
connector J4 connect RB2 to RD2     LCD DB6
connector J4 connect RB3 to RD3     LCD DB7
connector J4 connect RA1 to RD4     LCD RS
connector J4 connect RA2 to RD5     LCD RW
connector J4 connect RA3 to RD6     LCD E
connector J4 connect RB4 to RD7     LCD 5V (power supply)
3/ Use a RS232 <==> USB adapter to connect the serial port to the PC to see PRINTF
Speed : 115200,8,N,1
