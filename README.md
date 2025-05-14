# EEE3088F Micromouse Powersubsystem project

**User requirements**
1. Operate up to 4 motors bidirectionally with the pins available to you (listed in the power pinout
table). You will need to control 2x brushed DC motors which could each draw 200mA at the
highest voltage of a 1S1P battery (the battery is further specified in the battery section).
The other 2x motors are for the auxiliary connection and need to operate 500mA each.
2. Place an INA219 for monitoring the battery on the I2C Bus and configure it correctly with
respect to the hardware (cannot have BOTH A0 AND A1 on GND)
3. Charge the battery from the 9V input pin (listed in the power pinout table).
4.  Have two charging modes for a higher and lower charging current for the battery (200mA, and
approximately 600mA ±100mA from the battery perspective.
5. Integrate USB C and get 9V out of the USB Host
6. Provide 2x External Load Switching at 1A each (High Side connected to your 5V)
7. Provide a 3V3 5% accuracy (300mA max) and 5V Out 5% accuracy (1.5A max)
8. Provide an ON/OFF switch. OFF state: battery draw <30uA. ON state: can provide your robot
peak current of 2A. The switch needs to shut down 5V and 3V3.

**Breakdown and Analysis of Requirements**
Requirement 1 Possible solution
Bidirectionally operating the motors can be achieved simply by using the H-bridge circuit, however a IC is more preferable since some have protection measures in case of over-supply of current,since IC's are smaller it means that we'll be ensuring that minimum utilization of space on the PCB.

Upon Research, mainly YouTube. We have found the following ICs(Components in the hobby space are mostly affordable hence the researching on YouTube"for lack of a better phrase"):
1. DRV8834RGER (The datasheet of which shall be attached in this repo)
2. DRV8837CDSGR (The datasheet of which shall be attached in this repo)
3. LN298D(The datasheet of which shall be attached in this repo) # Usually needs a heat sink. Less efficient than the other two
4. TB6612FG (Can also be an interesting alternative)
Some useful YouTube links which provided clarity and a sense of direction on *Requirement 1*https://www.youtube.com/watch?v=PVyAcgYkzDs, https://www.youtube.com/watch?v=6HUs4ERsVkE&t=43s

At this juncture, we shall perform cost and performance analysis of the above-mentioned motor drivers:
[Motor Driver Selection IC.pdf](https://github.com/user-attachments/files/19388597/Motor.Driver.Selection.IC.pdf)

Cost analysis of components to satisfy other requirements:
[Componests selection and cost analysis.docx](https://github.com/user-attachments/files/19429474/Componests.selection.and.cost.analysis.docx)
Revised table
[Componests selection and cost analysis.docx](https://github.com/user-attachments/files/19621390/Componests.selection.and.cost.analysis.docx)
