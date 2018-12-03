`G28 ; Home all Axes
G29 ; auto bed level
G1 Z5 F3000 ; lift
G1 X40 Y5 F1500 ; avoid binder clips
G92 E0 ; reset extrusion distance
G1 Z0 F3000; set to base
G1 X120 E10 F600 ; prime nozzle
G1 X150 F5000 ; quick wipe
M205 X10 ; Lower Jerk to 10
M204 P500 T1000 ; Lower Acceleration`

