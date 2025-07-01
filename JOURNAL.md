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






