`;
; end_gcode
G92 E0                          ; zero the extruded length
G1 E-5 F9000                    ; retract
M104 S0                         ; turn off temperature
M140 S0                         ; turn off bed
G91                             ; relative positioning
G1 E-1 F300                     ; retract the filament a bit before lifting the nozzle, to release some of the pressure
G1 Z+20 E-5 X-20 Y-20 F7200     ; move Z up a bit and retract filament even more
G1 X320 Y150 F10000             ; move right mid
M107                            ; turn off layer fan
M84                             ; disable motors
G90                             ; absolute positioning
;
;EOF
`
