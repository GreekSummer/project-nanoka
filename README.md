# project-nanoka
![KiCad 3D render](/assets/3d-render.png)

Project Nanoka is a Raspberry Pi Pico based audio output/input PCB. It exposes two audio terminals (input and output) as well as seven general-purposes input/output lines for external control. 

The PCB can be powered either through the Raspberry Pi's USB port, or through the power terminal. This requires a power module (also hosted on GitHub).

Right now, this is a prototype, and it's usefulness likely applies only to me. There are better solutions out there. I mainly created this to learn KiCad, and more broadly, PCB design which was always an interest of mine. This PCB should not be reproduced for your own personal use. If you do use it, **all responsibility is yours**. 

Known issues from previous version:
1. No audio output because the buffer chip is wired incorrectly (Input to A1, output to Y2)
2. Audio relay footprint is wrong
3. Audio relay footprint was accidentally flipped to the back of the board
4. C3 and C5 footprints are wrong
5. Audio input/output terminals are labelled in reverse
6. A potentiometer to adjust audio levels exists, but adjusting it below 220 ohms can cause damage to the Raspberry Pi

Fixed issues:
1. Audio is now properly routed from the buffer's A2 to Y2
2. Both relay issues have been fixed
3. Audio input/output terminals are labelled correctly and more clearly
4. C3 and C5 footprints fixed
5. Kept potentiometer, but put a warning in place
