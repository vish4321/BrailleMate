# BrailleMate
A learning and reading assistant for the visually impaired.

This was my final course project for the Smart Devices course at the University of Pennsylvania. It was built around the Arduino, and written in baremetal C. The mechanism was a 2x3 grid of solenoids mimicking a braille character that we could control through a BJT and an ATMega328P. We created a system of two operational modes to use this grid effectively -- learning mode and reading mode.

In learning mode, the user controls a joystick that can be used to select a character. The character is put on the grid and said aloud by a speaker at the same time. In reading mode, there is a text file on our host system and a python script that uses pyserial to send the data character by character to the ATMega328P. As the MCU receives a character, it puts it on the grid.

The baremetal firmware running on the ATMega328P is in the BrailleMate folder, and the helper files for reading mode (python script and text file) are in the ReadingMode directory.

More details available on [Devpost](https://devpost.com/software/braillemate?ref_content=user-portfolio&ref_feature=in_progress)
