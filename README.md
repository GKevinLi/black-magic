# Black Magic: A Brushless DC Motor Driver

<img width="509" alt="image" src="https://github.com/user-attachments/assets/60654bbd-ea94-4d7c-ba59-509517337e41" />

This is a custom 4S 20A Sensorless BLDC Motor Driver designed for drone motor operation. I haven't had time to make the drone itself because I spent all my time designing this custom PCB instead. Still worth it though.

Features a DRV8323 motor driver chip along with a STM32 microcontroller. Supports full sensorless brushless DC motor operation through PWM input along with current sensing. 

It's called Black Magic because, let's be honest here, I'm messing around with powers beyond my comprehension. I'll be lucky if this thing doesn't blow up the first time I try to plug it in, although I've done my best to make sure that doesn't happen. 20A is still way too much current for someone like me to be playing around with.

This took way longer to make than the other one.... i think its obvious why


## Features
- DRV8323 Motor Controller chip
- STM32 Microcontroller
- USB-C port for programming
- PWM Input
- BEMF Detection through a virtual neutral point
- Current Sensing capabilities
- Voltage Regulator for 3.3v power

![image](https://github.com/user-attachments/assets/1806a90c-3eb9-4d67-84db-0967a97fbb51)

<img width="535" alt="image" src="https://github.com/user-attachments/assets/bb75dcdb-b0e7-40c9-a84d-eda26fd94eae" />

<img width="541" alt="image" src="https://github.com/user-attachments/assets/e983f32d-6e5e-48ad-9e05-c9104aae36a7" />

<img width="570" alt="image" src="https://github.com/user-attachments/assets/1f77479d-b125-4862-b50f-1ad4d8140ea9" />

<img width="509" alt="image" src="https://github.com/user-attachments/assets/94466b2f-bbd2-42c5-b76d-4e025c8c0459" />

<img width="510" alt="image" src="https://github.com/user-attachments/assets/fcd33ad5-4665-4c97-a99f-349d150e93f3" />


## BOM

| Item  | Usage | Source  | Price | Quantity | LCSC ID|
| ----| ----|----|----|----|----|
| 100 uf electrolytic capaciator | Bulk Capacitance | JLCPCB | $4.65 | 20 | C7272127 |
| 10 uf capaciator | Capacitance | JLCPCB | $0.08 | 15 | C19702 |
| 3.3 nf capaciator | Capacitance | JLCPCB | $0.10 | 20 | C26404 |
| 100 nf capaciator | Capacitance | JLCPCB | $0.04 | 40 | C1525 |
| 22 uf capaciator | Bulk Capacitance | JLCPCB | $5.25 | 25 | C5189846 |
| 22 uf capaciator (0603 footprint) | Capacitance | JLCPCB | $0.09 | 10 | C59461 |
| 2.2 uf capaciator | Capacitance | JLCPCB | $0.01 | 5 | C12530 |
| 1 uf capaciator | Capacitance | JLCPCB | $0.02 | 5 | C52923 |
| 47 nf capaciator | Capacitance | JLCPCB | $0.04 | 20 | C272875 |
| Schottky Diode | Preventing reverse current | JLCPCB | $0.10 | 10 | C191023 |
| Red LED | Indication | JLCPCB | $0.03 | 5 | C2286 |
| USB C Receptacle | Programming + Power | JLCPCB | $0.30 | 6 | C2927038 |
| MOSFET | Motor Control | JLCPCB | $8.06 | 30 | C201632 |
| 10 ohm resistor | Resistance | JLCPCB | $0.02 | 30 | C25077 |
| 33k ohm resistor | Resistance | JLCPCB | $0.02 | 30 | C25779 |
| 68k ohm resistor | Resistance | JLCPCB | $0.01 | 30 | C36871 |
| 22k ohm resistor | Resistance | JLCPCB | $0.01 | 5 | C25768 |
| 100k ohm resistor | Resistance | JLCPCB | $0.01 | 5 | C25741 |
| 10k ohm resistor | Resistance | JLCPCB | $0.01 | 20 | C25741 |
| 5.1k ohm resistor | Resistance | JLCPCB | $0.01 | 15 | C25905 |
| 0.01 ohm shunt resistor | Shunt Resistance | JLCPCB | $1.05 | 19 | C393070 |
| 4.7k ohm resistor | Resistance | JLCPCB | $0.01 | 5 | C25900 |
| Button | Button | JLCPCB | $0.42 | 10 | C720477 |
| STM32 | Microcontroller | JLCPCB | $15.86 | 5 | C529355 |
| USBLC6 | USB Data Protector | JLCPCB | $0.96 | 5 | C15999 |
| TLV76133 | Voltage Regulator | JLCPCB | $1.10 | 5 | C7527500 |
| DRV8323 | Motor driver | JLCPCB | $13.29| 5 | C7527500 |
| TPS82130 | Buck Converter | JLCPCB | $6.35 | 5 | C473914 |
