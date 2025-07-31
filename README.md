In this project, I have mainly focused on designing an 8-bit Subtractor and taking it all the way from a Verilog RTL description to a final GDSII layout using SYNOPSYS tools. The process followed a standard VLSI backend design flow:
1. RTL Synthesis: Writing the Verilog code for RTL(Register Transfer Level) description of 8-bit Subtractor, compiling it, and synthesizing it into a gate-level netlist using Design Compiler(DC-tool offered by Synopsys). Then analyzed the timing and QoR(Quality of Results) reports to ensure the design met performance goals.
2. Floorplanning and Powerplanning: Using the ICC2 compiler, I defined the chip"s corer area, pin placements, and power grid setup to ensure reliable power delivery.
3. Placement: Next step is to place the synthesized cells optimally to reduce wire length anf=d improve timing.
4. Clock Tree Synthesis: Created a balanced clock network to distribute the clock signal with minimal skew and latency.
5. Routing: All signal and power connections were made using different metal layers. The routed layout was optimized for performance and then checked for violations.
6. Timing Analysis(STA): Using PrimeTime (PT compiler),I verified that the design met setup and hold timing requirements. After minor SDC adjustments, the final design achieved positive slack, ensuring reliable operation.

The final layout passed all checks for timing, power, and area, proving that the subtractor is ready for tape-out.
Check the full detailed process (Tutorial) in the "Eight_Bit Subtractor RTL to GDSII.pdf" file uploaded.
