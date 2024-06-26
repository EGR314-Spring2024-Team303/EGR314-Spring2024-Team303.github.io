---
title: Final Software Implementation
---

[Home](/index.md)|[Team organization](/Team_organization.md)|[User Needs, Benchmarking, and Requirements](/User_Needs_Benchmarking_Requirements.md)|[Design Ideation](/Design_Ideation.md)|[Final Selected Design](/Selected_Design.md)|[Final Block Diagram of the product](/Block_Diagram_of_the_product.md)|[Final Component Selection](/Component_Selection.md) 
[Microcontroller Selection](/Microcontroller_Selection.md)|[Final Hardware Implimentation](/Final_Hardware_Implementation.md)|[Final Software Implimentation](/Software_Proposal.md)|[System Verification](/System_Verification.md)|[Lessons Learned](/Lessons_Learned.md)|[Recommendations for future students](/Recommendations_for_future_students.md) 

# Final Software Implementation
## Software Diagrams

![Software Proposal](https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/8b8b9f04-f935-40db-9e36-a7f8a398150d)
## Functionality of the Software Diagram relating to user needs
The software diagram for the ground-moving weather station incorporates several key functionalities to meet user needs and product requirements effectively. By integrating sensor functions into the main loop, the system ensures continuous monitoring and processing of temperature and atmospheric pressure data, enabling dynamic control of the motor and LED in response to environmental conditions. Additionally, the addition of a stop drive loop interrupt prioritizes safety by providing a reliable mechanism to halt motor operations in emergency situations. Refactoring the atmospheric sensor code to avoid blocking other processes enhances system responsiveness, while the inclusion of sensor clog detection improves system reliability by alerting users to potential sensor issues. Moreover, optimizing the initialization process minimizes redundant operations during startup, ensuring quick and efficient system initialization to meet user expectations for smooth operation and efficiency of our design. Overall, these functionalities collectively contribute to the creation of a reliable and user-friendly ground-moving weather station that effectively meets user needs for accurate data collection and system reliability while satisfying product requirements for safety, efficiency, and performance.

## Design and Decision making Process
The decision to integrate sensor functions into the main loop was driven by the goal of creating a ground-moving weather station, where temperature and atmospheric pressure sensors were pivotal for system control. This choice aimed to enhance real-time responsiveness and centralize control over sensor data processing and motor operations. Additionally, the addition of a stop drive loop interrupt prioritized safety, crucial for a system involving moving parts and external environmental factors. Refactoring the atmospheric sensor code from an infinite loop improved system responsiveness and resource management, ensuring efficient sensor readings without blocking other processes. Furthermore, the inclusion of sensor clog detection, through an LED indicator, underscored the commitment to reliability and diagnostics, crucial for ensuring accurate sensor data. Finally, optimizing the initialization process minimized redundant operations and streamlined system startup, aligning with the overarching goal of maximizing system efficiency and resource utilization.

## Changes Made in the Sofware Diagram


## 1. Main Loop Incorporates Sensor Functions:
In the previous setup, the sensor functions were called within the motor control loop. This coupling of sensor readings with motor operations could lead to inefficiencies, especially if sensor data was not needed continuously or if sensor processing caused delays in motor control. Now according to our diagram, sensor readings can be performed independently of motor control, allowing for better organization of code and more efficient resource utilization. Additionally, this separation of concerns simplifies debugging and maintenance, as sensor-related code is decoupled from motor control logic.

## 2. Addition of Stop Drive Loop Interrupt:
Previously, the system relied on a flag to signal when the motor drive loop should stop. While effective, this approach could introduce delays, especially if the flag-checking mechanism was embedded within a loop. By implementing a stop drive loop interrupt, the system gains a more responsive and deterministic way to halt motor operations. Interrupts allow the processor to immediately respond to external events or conditions, such as the flag dropping down when it's below a certain temperature. This enhances the safety and reliability of the system by providing a quicker means of halting motor operations so the motor doesn't try to gather more current.

## 3. Handling Infinite Loop in Atmospheric Sensor:
The atmospheric sensor was initially implemented within an infinite loop, which could potentially block other processes from executing. This design flaw could lead to delays in system responsiveness and inefficient resource utilization. By recognizing this issue and addressing it, the system now takes sensor readings without causing delays or interruptions to other tasks. This improvement is typically achieved by implementing non-blocking methods for sensor reading, such as using interrupts or timed sampling. As a result, the system operates more smoothly and efficiently, ensuring timely processing of sensor data while maintaining responsiveness to other tasks.

## 4. Addition of Sensor Clog Detection:
Previously, there was no mechanism to detect if the atmospheric pressure sensor was clogged or malfunctioning. This lack of diagnostics could lead to undetected sensor failures, potentially compromising the reliability and accuracy of the system. By adding an LED indicator within the loop, the system gains a visual indication of sensor health. If the LED remains off or exhibits unusual behavior, it could indicate a sensor blockage or malfunction, prompting further investigation and maintenance. This enhancement improves system reliability and diagnostics by providing a means to detect and address sensor issues proactively.

## 5. Optimization of Initialization Process:
In the previous setup, every system was initialized on every loop iteration, which could result in redundant initialization and unnecessary resource consumption. This approach may lead to inefficiencies, especially if system initialization involves complex or time-consuming operations. By optimizing the initialization process, such as initializing systems only once at the beginning of the program or based on specific conditions, the system operates more efficiently and reduces overhead. This improvement improves overall system performance and resource utilization by minimizing redundant operations and streamlining initialization procedures.


## Possible Improvements
In addition to the existing functionalities, there are several possible improvements that could enhance the software for the ground-moving weather station. One potential enhancement is the addition of plotting capabilities to visualize the collected data based on geographical location and time. Implementing this feature would allow users to analyze and interpret weather trends more effectively, aiding in decision-making for various applications such as agriculture and environmental monitoring. Furthermore, organizing the plotted data based on location would provide users with a comprehensive overview of weather conditions across different areas, facilitating better insights and comparisons. Another potential improvement is to explore the possibility of switching to a different microcontroller, as the current one may lack support for debugging features in MP LAB XIDE. Adopting a microcontroller with robust debugging capabilities would streamline the development process and enhance the software's reliability and maintainability. These improvements would contribute to the overall effectiveness and usability of the ground-moving weather station, enabling users to make informed decisions based on accurate and well-organized weather data.# Final Software Implementation


[Appendix A](/Appendix_A.md) | [Appendix B](/Appendix_B.md) | [Appendix C](/Appendix_C.md) | [Appendix D](/Appendix_D.md)

