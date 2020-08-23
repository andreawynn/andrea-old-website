## Computer Processor Project
## Course: CSSE232 - Computer Architecture
*Completed in Winter 2019-20*

**Please note that I cannot share the source code or files for this course project due to academic integrity regulations at Rose-Hulman.**

### Project Description
The Computer Processor project is a simple yet fully functional "miniscule instruction set" computer processor that can execute programs stored in an external memory unit. This processor was built from scratch using an accumulator architecture and a fully customized assembly language. This assembly language features 17 unique 16-bit instructions and support for procedures, calls, loops, and other essential functionality. 

The project was modeled, designed, tested, debugged, and assessed based on performance benchmarks, all by the project team members. The processor was tested for efficiency and functionality by running a benchmark program written in the processor's assembly language to compute relatively prime values using Euclid's algorithm. The processor comes with full, highly detailed documentation that includes specifications for all instructions, hardware, and testing procedures. 

Our team chose to add the additional functionality for this project to be runnable on a Field Programmable Gate Array (FPGA) microchip. At the conclusion of the project, the team also gave a live presentation and demonstration to the class. 

Our team received a high A on this project for our well-designed processor, strong teamwork, and well-organized documentation. 

### My Contribution
I contributed to nearly all parts of this project, while also splitting work fairly with my 3 teammates. 

My team and I worked together to design our hardware architecture as well as the instruction set that accompanied it. We iteratively improved and corrected our design as we stepped through the execution of single instructions all the way to execution of complex programs such as the Euclid's Algorithm benchmark program written in our own assembly language. 

I implemented, debugged, and tested the following individual components independently (using Verilog and Xilinx):
Control Unit
Memory Unit
Resettable Register
Multiple-Input Multiplexors
Sign & Zero Extenders

I also implemented, debugged, and tested the most complex of the three intermediate integration stages specified by our group during the design process (which handled all memory operations, as well as the system output signal), and helped to debug the two other stages (including the program counter updating stage and the arithmetic stage). 

During the final integration stage, when all three intermediate stages were put together to create the full processor system, our team worked together to test and debug the full project, taking turns at the keyboard. We iterated this process until we had a fully functional processor that could correctly run the benchmark Euclid's Algorithm program. 

In addition to my significant technical contributions, I was also the most significant contributor to the project documentation, writing over half of it independently and editing it all for organization, consistency, and grammar before the final submission. 

### Technical Architecture and Tools Used
*Programming Languages* <br>
Verilog & Xilinx - The hardware components of our project were implemented in these languages, per project requirements. 

*Version Control* <br>
GitHub - I used GitHub to collaborate with my team for this project and ensure that our work was up to date while working in parallel.

