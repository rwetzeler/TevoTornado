`
M117 Auto Level Bed     
G28                     ; Home all axes
G29                     ; auto bed level
M117 Start Clean        ; Indicate nozzle clean in progress on LCD
;
M104 S[extruder0_temperature] ; Set target temp for Extruder (no wait)
M109 S[extruder0_temperature] ; Set target temp for Extruder
M109 R[extruder0_temperature] ; Set target temp and always wait
;
G1 X3 Y5 Z15 F9000      ; Move safe Z height to shear strings
G1 X40 Y5 F1500         ; move to avoid binder clips
G92 E0                  ; Set extruder to [0] zero
G1 Z0 F3000             ; set nozzle to bed
G1 X100 E10 F600        ; prime nozzle
G1 X200 F5000           ; quick wipe - move 100 mm with no extrusion
M117 Update Quality Settings...
M205 X10                ; Lower Jerk to 10
M204 P500 T1000         ; Lower Acceleration
;
M117 Begin Printing...
`
