# very-basic-BMS
Very basic BMS made from S8211C chips. Each chip can measure one cell and report OV or UV states by CMOS outputs.
Those signals are translated to isolated 12V lines via ACPL-227 dual opto isolator. 
One board is capable of guarding 16S setup with no minimum requirements. I.e. a single cell could be watched by one board.
4 wires are connected to BMS board and 4 wires go from one board to next BMS board or finally to master board.
Both OV and UV signals are AND loop where a single deviation causes disconnect of appropriate function. For example if in the course of a charge single cell would hit OV alarm, then charger would stop. 
UV signal is wired directly and it is used to stop the car in case of undervoltage. For additional safety the UV loop is wired with pullup so if a cell would just die at zero volts. Then car would stop to protect the battery. 

