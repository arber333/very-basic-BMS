# very-basic-BMS
Very basic BMS made from S8211C chips. Each chip can measure one cell and report OV or LV states by CMOS outputs.
Those signals are translated to isolated 12V lines via ACPL-227 dual opto isolator. 
One board is capable of guarding 16S setup with no minimum requirements. I.e. a single cell could be watched by one board.
4 wires are connected to BMS board and 4 wires go from one board to a different BMS board or a master board.
