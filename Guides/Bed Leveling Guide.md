## Intro
I use a BL Touch for my Auto Bed Leveling (ABL) but this isn't specific to that

## Connect
Connect to printer and send the following commands via your favorite software - I use OctoPrint Terminal to send commands

### Reset Z offset
1. G28; home all axes
1. M851 Z0; Reset current Z Offset to 0.00
1. M500; Store Settings in EEPROM
1. M501; Set EEPROM as active parameters
1. M503; Display all Active Setting (look for z-offset to 0.0)
1. G28 Z0; Home only the Z Axis
1. G1 F60 Z0 ; Move nozzle to proper true Z zero offset (speed of 60)

### Disable Soft Limit Switch
1. M211 S0; Switch off Soft Endstop

### Manual Setting
1. Slowly move nozzle downward with small steps until paper barely moves
2. Take note of Z-offset once you've hit that - record this value - e.g. -2.49

### Calculate new Z-Offset
1. Add thickness of paper 0.01MM or whatever you use
2. Add this value to the number you found above e.g. -2.5

### Set new Offset and finish up
1. M851 Z-2.5; Sets the new z-Offset
2. M211 S1; Turn back on soft Endstop
3. M500; Save to EEPROM
4. M501; Set EEPROM to active parameters
5. M503; Display new Settings

### Verify
1. G28; Home All axes
2. G1 F60 Z0; Move back to proper Z zero to check to ensure its at zero


### References

[YouTube - Calibrating Z-Offset With An Auto Bed Levelling Probe](https://www.youtube.com/watch?v=y_1Kg45APko)
