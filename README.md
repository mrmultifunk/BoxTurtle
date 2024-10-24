# BoxTurtle V1.0
BoxTurtle Automated Filament Changer (requires AFC-Klipper-Add-On (Beta))

![BT_Render](https://github.com/user-attachments/assets/c06e961f-8d1d-41ae-9c80-036669ba2657)
[![Join me on Discord](https://discord.com/api/guilds/1229586267671629945/widget.png?style=banner2)](https://discord.gg/eT8zc3bvPR)

Box turtle is exactly what it appears to be. An open source AMS style filament changer for klipper machines. 
Box turtle uses AFC-Klipper add on found [Here](https://github.com/ArmoredTurtle/AFC-Klipper-Add-On).
The goal of BoxTurtle is to deliver a user experience as close to an AMS as possible in vanilla klipper. i.e. an "AMS" for any klipperized printer regardless of form factor but VORON Design printers in particular.

If you appreciate the work we are doing, you can support us [Here](https://www.armoredturtle.com/pages/donate).

# How it works

BoxTurtle is an automated, lane-based filament changing system, also known by some as a "Type B MMU." Each lane is equipped with its own dedicated motor that moves filament to and from the tool head independently, eliminating the need for a selector cart or servos. Synchronization between the lane motor and the tool head occurs when the filament triggers a sensor located in or near the tool head.

To accommodate any differences in rotation distance between the extruder in the tool head and the lane motors, BoxTurtle uses a buffer system, such as the [belay by annex engineering](https://github.com/Annex-Engineering/Belay) or the T[TurtleNeck](https://github.com/ArmoredTurtle/TurtleNeck) by ArmoredTurtle. This system is "bufferless," meaning no filament boxes are required, similar to the AMS. Each lane features an independent respooler equipped with a brushed motor, which helps rewind the spool and assists the lane motor in feeding the filament smoothly. This prevents issues like spool tangling or "bucking."

For precise PWM control of the brushed motors, BoxTurtle relies on a custom MCU, AFC-lite, developed by [Isik's Tech @xbst](https://github.com/xbst/AFC-Lite/)  While the system currently supports BTT MMB CAN, this is a temporary solution to facilitate broader testing and will not be a permanent feature.

# Manual (WIP)

[Will update this as progress is made](https://armoredturtle.xyz)

# Wiring

![BoxTurtle_AFC-Lite_Pinout](https://github.com/user-attachments/assets/134796f6-8458-4a61-9967-1292963d7b4b)

# Slicer configuration

Orca Slicer is the prefered slicer for BoxTurtle use.
![Screenshot (57)](https://github.com/user-attachments/assets/b0e93466-8c66-42dd-9105-e7e3ecdc08f2)
