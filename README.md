# module-dual-supply

### This awesome little board handles a question that persistently pops up in forums: given a voltage and ground (aka a single supply), how can you get a negative voltage (aka a dual supply)? The centerpiece of this board is the awesome little TC7660 inverting DC-DC charge pump, which can easily be sourced for less than $1 in single quantities.

### This module is essentially just a breakout board for the TC7660. There are a couple of things to note when using this chip, and hence this module:

### 1. The positive voltage (V+) must be between 1.5V and 10V. If you need to handle higher voltages, the pin-equivalent TC7662 goes up to 15V but costs a little more than twice as much as the TC7660.

### 2. If, and only if, V+ is less than 3.5V then the header pin pair JP (upper-right of board layout) must be jumpered.

### 3. The capacitors should be 10uF. If you are using polarized capacitors, be very very sure to get the orientations correct.

### 4. As far as we know, the decoupling capacitor C3 is optional for the TC7660; a 2.2uF decoupling capacitor is required for the TC7662 if the input voltage has a large impedance.

### 5. Both the TC7660 and TC7662 can source up to 20mA, which is more than sufficient for running some dual-supply op amps on a single supply board.

### 6. Finally, note that the TC7660H is also available (roughly 20% for expensive than the TC7660) which has a higher switching frequency and only requires 1uF capacitors instead of 10uF capacitors.
