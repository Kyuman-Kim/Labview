These labview project and VIs being used on my static load control system with a DN-10W indicator (DACELL, www.dacell.com) <br><br>
The system controls static load generated by a pneumatic cylinder.<br>
The load (force) measured by a calibrated load cell with the DN-10W indicator. The DN-10W indicator compares the measured force to previsouly entered reference values.<br>
In decision mode, there are three states: Low, High, and OK. These states are separated by two reference values: High limit set value, and Low limit set value. (see manual p.16) <br>
If the measured force is between the High limit set value and the Low limit set value, the state is OK. Then the relay 2 in the DN-10W is ON (other relays are off).<br>
If the measured force is smaller than the Low limit set value, the state is Low. Then the relay 1 is ON (other relays are off).<br>
If the measured force is higher than the High limit set value, the state is High. Then the relay 3 is ON (other relays are off).<br>
In the state OK, there is no change in the system. When the state become Low, a solenoid valve makes cylinder pressure high is ON. In other hand, state become High, another solenoid valve makes cylinder pressure low is ON.<br><br>
The two reference values were entered by push buttons in the front of the DN-10W body manually. This way is too slow. <br>
These codes improve this situation. This program changes the two reference values using modbus-rtu communication between a PC and a DN-10W indicator. The program sets the High limit set value and Low limit set value as the input set value +/- 0.1 kgf. So, the force is controlled within set value +/- 0.1 kgf.<br><br>
Operation
1. Physical connect RX/TX (see manual)
2. Run program
3. Dropdown VISA Resource name
4. Select port
5. Click 'Connect'
6. Click 'Read'
7. Input 'Set value'
8. Click 'SV Update'
<br>
Zero button is zero. <br>
End button enabled under disconnect state closes the program.
