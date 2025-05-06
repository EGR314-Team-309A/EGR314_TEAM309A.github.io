## Final Reflections of EGR 314: Embedded Systems Design II

### Lessons Learned
- Working on this project as part of Team 309A in EGR314 provided us with a wide range of valuable technical and personal lessons:

- PCB and Schematic Design: We learned how to effectively design schematics and PCBs using industry-standard tools. This included labeling nets, organizing components, and ensuring logical flow for easier debugging and manufacturing.

- Industrial Communication Protocols: We gained hands-on experience working with SPI and I2C protocols—learning not only how to implement them in code but also how to troubleshoot issues like timing mismatches, improper wiring, or register configuration errors.

- Server and WiFi Setup Using Microcontrollers: We experimented with setting up local servers and WiFi communication using ESP32s in conjunction with our PIC microcontrollers, preparing us for future IoT or web-connected hardware applications.

- Human-Machine Interface (HMI) Programming: We developed a simple yet effective user interface to monitor and interact with our system, learning how to bridge low-level hardware control with user-facing functionality.

- Debugging and Testing with Oscilloscopes: Using lab tools like oscilloscopes helped us trace UART signals, validate logic levels, and verify protocol timing—skills that are essential for any embedded system engineer.

- Persistence in Debugging: One of the most important lessons was learning to stay persistent. Many bugs were not resolved quickly, and it took multiple iterations, logic reviews, and hardware checks to isolate and solve issues.

- Problem-Solving Under Pressure: At times, we were stuck without a clear path forward, but through brainstorming and cross-verifying each subsystem, we learned to logically decode issues and find working solutions.

- Work Ethic and Engineering Reality: We experienced firsthand what it takes to be an engineer—spending long hours, working weekends, and putting in extra effort to ensure the system functioned as expected.

- Team Communication and Collaboration: Clear communication between team members was essential. We coordinated changes, shared updates regularly, and supported each other through design and testing hurdles.

- Deliverable Management and Time Efficiency: Throughout the course, we improved our ability to produce correct and complete deliverables under tight deadlines, a critical skill in both academic and professional engineering environments.

### Recommendations for Future Students
- Start learning how to use MPLAB X and MCC early so that you are comfortable with configuring peripherals like SPI, UART, and I2C when the time comes.

- Get familiar with reading datasheets—they are your best source for understanding how to properly set up and control sensors, drivers, and microcontrollers.

- Prioritize clear team communication from day one to avoid duplicate work or design mismatches later in the semester.

- Regularly test individual subsystems before integrating them, as debugging a full system without knowing the behavior of its parts is very difficult.

- Keep up with your documentation and commit code often, so that your reports and demos are easier to assemble when deadlines are tight.

### Version 2.0 – Communication Architecture Improvements
If we were to create a Version 2.0 of our communication architecture and system design, we would focus on improving hardware reliability, user interaction, and development workflow to create a more robust and interactive experience.

- Reliable Temperature Sensor Integration: In Version 1.0, our sensor had issues with reliably. For Version 2.0, we would select a tested temperature sensor and fully validate it using I2C scanning tools and oscilloscope monitoring to ensure accurate communication with the PIC18F series microcontrollers.

- Using the PIC18F47Q10 for Both Subsystems: Standardizing on the PIC18F47Q10 across both PCBs would unify our firmware, reduce debugging time, and simplify code development by avoiding hardware-specific variations.

- Improved PCB Modularity and Compactness: We would redesign the layout for a smaller, more modular PCB with clearer separation of subsystems (power, comms, logic). This would save space and reduce manufacturing costs while maintaining clarity in the hardware architecture.

- Verification of Soldering and Continuity: In Version 2.0, we would conduct thorough soldering checks and use a multimeter to test all critical traces and pins—especially for UART, SPI, and I2C—before powering the board.

- Incorporating Multiple Test Points: We would add test points on all major signal (UART pins, I2C pins and SPi pins) lines to allow quick and safe probing during debugging, reducing the risk of damaging the board and helping isolate faults faster.

- Early Setup of MPLAB X and MCC: We would fully configure MPLAB X and MCC Classic early in the semester, and build small test projects to confirm UART, SPI, and I2C setup before integrating them into the full system.

- Maximizing In-Class Lab Resources: Tools like oscilloscopes and in class labs would be used from day one. These would be invaluable in diagnosing signal integrity issues, timing problems, and confirming communication protocols.

- User-Readable Temperature Display: To improve usability and meet interactive display goals, we would implement a live temperature readout on an LCD or OLED display, allowing users to see the real-time sensor output.

- 3D-Printed Spinning Top as a Physical Display: We would design and integrate a 3D-printed spinning top attached to the motor shaft. This would serve as a physical visualization of motor actuation—its speed or direction reflecting the current temperature range, adding a tactile, engaging element to our project.

