# very-basic-BMS
Very basic BMS made from S8211C chips. Each chip can measure one cell and report OV or UV states by CMOS outputs.
Those signals are translated to isolated 12V lines via ACPL-227 dual opto isolator. 
One board is capable of guarding 16S setup with no minimum requirements. I.e. a single cell could be watched by one board.
4 wires are connected to BMS board and 4 wires go from one board to next BMS board or finally to master board.
Both OV and UV signals are AND loop where a single deviation causes disconnect of appropriate function. For example if in the course of a charge single cell would hit OV alarm, then charger would stop. 
UV signal is wired directly and it is used to stop the car in case of undervoltage. For additional safety the UV loop is wired with pullup so if a cell would just die at zero volts. Then car would stop to protect the battery. 

I had to make some modification to my R1 boards. It seems i wasnt carefull enough and i forgot to introduce some reference connections. I also made an error in placement of load transistor. Since i used P mosfet that has reverse diode now all current drains through diode....
And of course i added two P-mos transistors to reverse signals from BMS chip to opto. Daisy chain signal still pulls 12V down to signal OV/UV event.
Newest files are in LiPo_16Cell2.zip archive.
