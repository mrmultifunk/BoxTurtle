# BoxTurtle V1.0
BoxTurtle Automated Filament Changer (requires AFC-Klipper-Add-On (Alpha))

![BT_Render](https://github.com/user-attachments/assets/c06e961f-8d1d-41ae-9c80-036669ba2657)

Box turtle is exactly what it appears to be. An open source AMS style filament changer for klipper machines. 
Box turtle uses AFC-Klipper add on found [Here](https://github.com/ArmoredTurtle/AFC-Klipper-Add-On).
The goal of BoxTurtle is to deliver a user experience as close to an AMS as possible in vanilla klipper. i.e. an "AMS" for any klipperized printer regardless of form factor but VORON Design printers in particular.

If you appreciate the work we are doing, you can support us [Here](https://www.armoredturtle.com/pages/donate).

# How it works
BoxTurtle is a lane based automated filament changing system, refered to as "type b mmu" by some.
This means that each "lane" has its own motor responsible for moving filament to and from the tool head. This system uses no selector cart and no servos. Each lane motor syncs with the toolhead once the filament activates a [filament sensor](https://github.com/ArmoredTurtle/Filatector) in (or near) the toolhead.
In order to cover any discrepancies in rotation distance between the toolhead's extruder and lane motors rotation distance, a toolhead buffer like [belay by annex engineering](https://github.com/Annex-Engineering/Belay) or [TurtleNeck](https://github.com/ArmoredTurtle/TurtleNeck) by ArmoredTurtle is used.
This is a "bufferless" (no spaghetti boxes) system akin to the AMS. Each lane has its own independant respooler that uses a brushed motor to rewind the spool, and to assist the lane motor in feeding to prevent spools bucking out and/or tangling.
To enable pwm brushed motor control, BoxTurtle requires a "custom" mcu made by [Isik's Tech @xbst](https://github.com/xbst/AFC-Lite/) called AFC-lite.
BTT MMB CAN support for BoxTurtle will not be permanent as it is a bandaid solution for testing BoxTurtle on a broader scale more quickly. 

