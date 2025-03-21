# EEE3088F Micromouse Powersubsystem project

*Requirement 1 as per project deliverables*: 
Operate up to 4 motors bidirectionally with the pins available to you (listed in the power pinout
table). You will need to control 2x brushed DC motors which could each draw 200mA at the
highest voltage of a 1S1P battery (the battery is further specified in the battery section).

*Possible solution*:
*comments: *Bidirectionally operating the motors can be achieved simply by using the H-bridge circuit, however a IC is more preferable since some have protection measures in case of over-supply of current,since IC's are smaller it means that we'll be ensuring that minimum utilization of space on the PCB. 

Upon Research, mainly YouTube. We have found the following ICs(Components in the hobby space are mostly affordable hence the researching on YouTube"for lack of a better phrase"):
1. DRV8834RGER (The datasheet of which shall be attached in this repo)
2. DRV8837CDSGR (The datasheet of which shall be attached in this repo)
3. LN298D(The datasheet of which shall be attached in this repo) # Usually needs a heat sink. Less efficient than the other two 
Some useful YouTube links which provided clarity and a sense of direction on *Requirement 1*https://www.youtube.com/watch?v=PVyAcgYkzDs, https://www.youtube.com/watch?v=6HUs4ERsVkE&t=43s

At this juncture, we shall perform cost and performance analysis of the above-mentioned motor drivers:
