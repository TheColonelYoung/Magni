# Magni
Electric linear actuator powered by stepper motor. Based on 3D printed body with built-in bearing.

![](pics/magni_1.png)

Actuator is easily modifiable, with with any length. There are only two parts which needs to be modified for greater length.
Project is designed in Onshape. Project can be downloaded or forked on this [link](https://cad.onshape.com/documents/d29122f55449fc9b32e37efc/w/e29782a3cd26bfe716aed0ac/e/d3b8e881492a84b656a9ecee)

Actual version have mounting holes for NEMA17 motor. Motion from motor is transmitted from motor to trapezoid rod via GT2 belt.
Belts are mounted on 32 teeth gears. Gears are printed from HIPS, so are more stiffer.
Ration between motor rotation and actuator shift is 3 mm shift per 1 rotation if motor.
Maximal achievable speed is around 20mm/s with common motor.

Inside shaft is fixed printed T-nut. Commercial steel nut not fit into this tight space. This nut is best to print from HIPS because is one of the most the stiffest material from from commercially available (another possibility is carbon fibber filled PLA). Nut is fixed in shaft by 4 worm screws.

Possible issue is with stability of push rod.
This can be resolved by mounting trapezoid into bearings.
But bearings need to be perfectly in line, because otherwise can be bearing damaged by turning of main rod.
Stability can be upgraded with better stability of body, this can be achieved by more mounting screws between gearbox and body.

### Build-in bearings
This gcode can be placed into marked layer to stop during print. During pause can be bearing inserted, after it print can be resumed by pressing a button.
Issue can be if you are using sticky parameter. So speed of command after this block can be affected by last used speed.
```gcode
G91
G1 E-6 F4800
G1 Z50 F600
M300 S300 P1000
M0 Click to continue...
G1 Z-50 F600
G1 E6.5 F4800
G90
```

# Pictures
### **Open gearbox**
![](pics/magni_2.png)
### **Cross section of shaft**
![](pics/magni_cross_section.png)

## Main parts
- [Shaft](STL/Shaft.stl)
- [Body](STL/Body.stl)
- [Front cover](STL/Front_cover.stl)
- [Back cover](STL/Cover_back.stl)
- [Pulley - motor](STL/Pulley_32T_B5.stl)
- [Pulley - trapezoid](STL/Pulley_32T_B12.stl)
- [Gearbox - base part](STL/Gearbox_body.stl)
- [Tensioner head](STL/Tensioner_head.stl)
- [Trapezoidal nut](STL/T-nut.stl)

## Other parts
- Bearings
    - 4x12x4, 1 pcs
    - 12x18x4, 4pcs
- Belt - GT2, 155mm closed loop belt
- Trapezoidal screw rod T12 - length 172mm
- Steel bearing balls - diameter 4mm, 40 pcs
- Screws - TODO
