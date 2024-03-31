# arew

**Floorplan steps:**
1. Determine the dimensions (width and height) of the core and die area.
2. Establish locations for IO pad sites to accommodate input-output connections.
3. Arrange the placement of macros, which are pre-designed functional blocks, within the layout.
4. Generate rows for standard cell placement, ensuring efficient use of space for logic elements.
5. Conduct power planning activities before routing to optimize power distribution across the layout.
6. Integrate physical-only cells into the design as needed for specialized functions.
7. Position blockages strategically to reserve space for specific components or avoid interference between elements.

We'll start by creating a basic netlist, which combines sequential elements like flip-flops (launch flop and capture flop) with some combinational logic in between. This serves as an example to determine the width and height of the core and die. This initial setup can later be scaled up to handle designs with millions of gates.

When defining the chip dimensions, we primarily consider the dimensions of logic gates or standard cells rather than wires. Wires are crucial in later stages.

**Utilization Factor**:
  The utilization factor determines the portion of the chip area allocated for placing standard cells, macros, and other cells, as opposed to routing.

  Utilization factor of 0.8 (UF = 0.8) implies that 80% of the area is used for cell placement, while 20% is reserved for routing.
Core utilization is calculated by dividing the combined area of macros, standard cells, and other cells by the total core area.
Die utilization is determined by dividing the sum of the core area and IO area by the total die area.<br/>

**Aspect Ratio:**
  Aspect ratio influences the size and shape of the chip or block.
It's defined as the ratio of height to width or the ratio of horizontal routing resources to vertical routing resources.
An aspect ratio greater than 1 indicates a taller chip, while a ratio less than 1 signifies a wider chip. An aspect ratio of 1 results in a square shape.
