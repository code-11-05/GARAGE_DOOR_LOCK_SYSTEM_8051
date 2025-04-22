# PASSWORD-BASED GARAGE DOOR SYSTEM
This is a garage door lock system based on 8051 microcontroller that provides secure opening and closing of the garage. The whole system is programmed using assembly language.

## OVERVIEW
The system prevents unauthorized access by allowing only a pre-set password to trigger the motor mechanism that opens the shed door. If the wrong password is entered multiple times, the system locks down and raises an alert.
The garage is programmed to close automatically once the vehicle moves out from the garage.

## FEATURES
- Secured password access
- Keypad input for password entry
- LCD display for user interaction
- Motor drivers for controlling the motors
- PWM for motor speed control
- Buzzer alerts for multiple incorrect attempts
- Automatic door closing once vehicle moves out of the garage

## REQUIRED COMPONENTS
- AT89S52 microcontoller 
- 4x4 Matrix Keypad
- 16x2 LCD display
- Dual shaft gear motors(x2)
- L298N motor driver
- 3.7v Li-ion battery(x2)(for providing power supply)
- Buzzer
- Resistors, capacitors, push buttons and crystal oscillator (crystal oscillator to be used, if not using a 8051 microcontroller development kit)
- Programmer IC for AT89S52
- IR sensors

## WORKING
1. The user is prompted to enter the password to unlock the garage
2. If the user enters the correct password,
   - 'correct password' message would be displayed in the LCD
   - the motors are activated and garage door is opened
   - once the door is completely opened, the IR sensors would wait until motion detection of vehicle out of the garage
   - if the vehicle had completely moved out of the garage, the door would close automatically
3. If the user enters the incorrect password,
   - 'incorrect password' message would be displayed in the LCD
   - the user would be asked to enter the password until all the attempts are over(for instance, number of attempts is 3)
   - after 3 continuous incorrect attempts, the door would remain closed and buzzer alert would be triggered
4. The door is closed by the motor mechanism controlled by the motor driver

## PRE-REQUISITES AND BASIC REQUIREMENTS
- Assembly programming of 8051
- Programming experience in Keil uvision
- AT89S52 microcontroller kit requirements
  1. Zadig software for installing driver
  2. ProgISP software for burning the code and uploading it in the chip
- Proteus simulation software(optional for circuit reference)

## FUTURE IMPROVEMENTS
- Wireless password entry using Bluetooth
- Integration with RFID or fingerprint module
- Smartphone control with a mobile app
