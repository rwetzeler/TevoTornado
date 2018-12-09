`
M117 Initial Startup and set temps
G21                     ; Set all units to mm
M107                    ; Turn off the part cooling fan
M104 S210               ; Set extruder to 210 C and move on immediately
M140 S60                ; Set bed to be 60 C and immediately move on
M190 S60                ; Set bed to  be 60c and wait until temp reached
M109 S210               ; Set extruder to 210c and wait until temp reached
G28                     ; Home all axes
M117 Start Clean        ; Indicate nozzle clean in progress on LCD
G1 X3 Y5 Z15 F9000      ; Move safe Z height to shear strings
G1 X5 Y5 F1500         ; move to avoid binder clips
G92 E0                  ; Set extruder to [0] zero
G1 Z0.2 F3000             ; set nozzle to bed
G1 X100 E20 F600        ; prime nozzle
G1 X200 F5000           ; quick wipe - move 100 mm with no extrusion
G92 E0                  ; Set extruder to [0] zero
M117 Update Quality Settings...
M205 X10                ; Lower Jerk to 10
M204 P500 T1000         ; Lower Acceleration
M300 S300 P1000         ; Play a 300Hz beep to sound for 1000ms
M117 Begin Printing...
`
