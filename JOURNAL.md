---
title: "black magic"
author: "kevin"
description: "brushless motor controller"
created_at: "2025-06-11"
---
Total time spent: a lot

# June 11: figuring stuff out

Did some research on BLDC motor drivers in general and figured out what I needed. Figured out all the basic parts for a half-bridge circuit and made a quick schematic of one in KiCad. I also began looking into parts for the gate drivers and the MOSFETs specifically.

Turns out this project is actually quite complicated, involves high amounts of current, and is pretty ill-advised for a young child like me. But fuck it we ball

<img width="371" alt="image" src="https://github.com/user-attachments/assets/184dcbbd-98d9-468c-81bf-fe3b3e7a1d27" />

**Total time spent: 4h**

# June 12: parts and stuff

Spent some time looking for good components to use as part of the motor driver circuit. Eventually found some reasonably cheap MOSFETs and gate drivers that fit my requirements. 
Also decided on using the ATMega328P as the microcontroller, as it's pretty cheap and also fits all of the requirements I need.

Hopefully going to get started on the schematic tommorrow, this is already 10x more painful than the other board i made

**Total time spent: 3h**

# June 13: sch'matic

Did some schematic stuff. Copied over the USB-C port schematic from my other project and added the ATMega328P schematic. Also made a schematic for the CP2102 USB to UART bridge because the ATMega doesn't have built in USB support. Added a schematic for the 14.8v to 5v buck converter to power the Arduino straight from the battery.

<img width="182" alt="image" src="https://github.com/user-attachments/assets/97ac4c96-1e5a-4dff-95c9-82d8222efc78" />

<img width="251" alt="image" src="https://github.com/user-attachments/assets/4bec581e-b711-4edf-8617-aacc0ddeb80a" />

<img width="217" alt="image" src="https://github.com/user-attachments/assets/62aba0f2-3064-4ef0-9a61-0e7e749047bc" />

**Total time spent: 2h**


# June 14: (traumatic war flashbacks)

Began working on the PCB layout. Managed to get all of my current schematic layed out, but I'm still planning on adding some other stuff. Also added some preliminary ground, Vin, M1, M2, and M3 copper pours. I decided to use a 4-layer board due to the convenience of routing as well as to reduce EMI.

![image](https://github.com/user-attachments/assets/383626eb-538d-4f13-b7e3-bb7ed2d8333b)

**Total time spent: 4h**

# June 15: other stuff i guess

Completed the schematic by adding some extra stuff I needed for the layout. Basically just added some bulk capacitance, the back EMF resistive bridge, and some mounting holes as well as the PWM input pins. Also worked on the routing a bit more today, mostly by adding the new stuff from the schematic and cleaning up the traces a bit.

<img width="785" alt="image" src="https://github.com/user-attachments/assets/713be242-d1bc-43c3-a129-915e0cbdd01a" />

**Total time spent: 3h**

# June 18: well it's done, time for design review ig

finished the pcb layout and the schematic, so i'm gonna upload this to reddit for a design review. last time I did this I got a lot of rlly helpful suggestions, so hopefully this time i can find a bunch of ways to improve this design. I'm still feeling rather iffy on this design, it seems a bit weird and there are some things I wanted to add (current sensing) but didn't get the space to, so i'll ask about that as well.

![image](https://github.com/user-attachments/assets/cff02669-2272-4837-b93c-3fb6fdeef9fd)
![image](https://github.com/user-attachments/assets/675e986e-80c1-4004-9325-163fb3e0b4c4)

**Total time spent: 3h**

# June 19: rethinking my entire worldview because of what some strangers said to me on the internet

welp its time for a redesign

based on much of the advice on reddit, I have decided that my current design sucks ass. Therefore, I have decided to restart completely and begin redesigning the whole thing, starting from the motor outputs and the MOSFETs. I have also decided to include current sensing because SCOPE CREEP IS NOT REAL AND CANNOT HURT ME.

I have made the decision to change my design from using three seperate half-bridge drivers to one big fancy DRV8323 motor driver. This is because it saves a bunch of space, money (from supporting components), and has current sensing integrated into the driver, so I don't need any extra components for that. 

Lots of datasheets today! I'm having fun! I'm having fun! I'm having fun!

**Total time spent: 5h**


# June 20: beginning the redesign

Did a bunch of layout work today and added the DRV8323 schematic as well as the new mosfet schematics. I found some good shunt resistors for current sensing and added those to the design as well. This redesign addresses a bunch of the issues present in the old design, and it's going ok so far????

![image](https://github.com/user-attachments/assets/1d67315e-67d1-49da-b141-600dbe1fb1c3)


**Total time spent: 3h**

# June 21: cahnges

Officially decided to swap out the ATMega328p to a STM32 chip. Just looked at the specs and the STM32s are so much better it isn't even a close comparison. Because of this, I also now don't need a USB to UART bridge because the STM32 has built in USB! It's perfect! 

Spent a while reading the datasheet just to see if the STM32 had everything I needed (pwm outputs, enough comparators for back EMF, etc) and the best pin layout to use for it.

**Total time spent: 2h**

# June 22: the work continues

Placed the DRV8323 motor driver and connected all the tracks to the motor drivers. Also redid the schematics (changed the buck converter to output 3.3v and added a linear voltage regulator)
Didn't do much today so thats about it


**Total time spent: 1h**

# June 26: this is the grind that never ends

Spent a bunch of time today adding the STM32 to the board, connecting all the tracks for those, and just adding everything else that needed to be added. Layout is basically done now. I'm tired man

![image](https://github.com/user-attachments/assets/6d2bccaa-ed2b-4c93-b039-729aa3196ad0)



**Total time spent: 4h**


