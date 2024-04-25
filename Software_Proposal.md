---
title: Final Software Implementation
--- 
[Home](/index.md) | [Team organization](/Team_organization.md) | [User Needs, Benchmarking, and Requirements](/User_Needs_Benchmarking_Requirements.md) | [Design Ideation](/Design_Ideation.md) | [Selected Design](/Selected_Design.md) 
[Block Diagram of the product](/Block_Diagram_of_the_product.md) | [Component Selection](/Component_Selection.md) | [Microcontroller Selection](/Microcontroller_Selection.md) | [Final Hardware Implimentation](/Final_Hardware_Implementation.md) | [Final Software Implimentation](/Software_Proposal.md) | [System Verification](/System_Verification.md) | [Lessons Learned](/Lessons_Learned.md) | [Recommendations for future students](/Recommendations_for_future_students.md)

# Final Software Implementation
## Software Diagrams

![Software Proposal](https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/8b8b9f04-f935-40db-9e36-a7f8a398150d)
## Functionality of the Software Diagram
## Design and Decision making Process
## Changes Made in the Sofware Diagram

Certainly! Let's break down each change and its implications:

## 1. Main Loop Incorporates Sensor Functions:
Previously, the sensor functions were called inside the motor loop, meaning sensor readings were taken continuously while the motor was running. By moving the sensor functions to the main loop, the system can now handle sensor data independently of motor control. This separation of concerns improves modularity and allows for better organization of code.

## 2. Addition of Stop Drive Loop Interrupt:
Previously, there was no interrupt mechanism to stop the motor drive loop. Instead, a flag was raised to indicate when the loop should stop. By implementing a stop drive loop interrupt, the system gains a more responsive and efficient way to halt motor operations in case of emergencies or specific conditions. This enhances the safety and reliability of the system.

3. Handling Infinite Loop in Atmospheric Sensor:
The atmospheric sensor was previously implemented in an infinite loop, potentially blocking other processes from executing. By recognizing this issue and addressing it, the system can now take sensor readings without causing delays or interruptions to other tasks. This ensures smoother operation and better resource utilization.

4. Addition of Sensor Clog Detection:
Previously, there was no mechanism to detect if the atmospheric pressure sensor was clogged or malfunctioning. By adding an LED indicator in the loop, the system gains a visual indication of sensor health. If the LED remains off or exhibits unusual behavior, it could indicate a sensor blockage or malfunction, prompting further investigation and maintenance. This enhances system reliability and diagnostics.

5. Optimization of Initialization Process:
Previously, every system was initialized on every loop iteration, potentially leading to redundant initialization and unnecessary resource consumption. By optimizing the initialization process, such as initializing systems only once at the beginning of the program or based on specific conditions, the system can operate more efficiently and reduce overhead. This improves overall system performance and resource utilization.

Overall, these changes and possible improvements enhance the functionality, reliability, and efficiency of the embedded system software. They address issues related to modularity, responsiveness, resource management, and diagnostic capabilities, resulting in a more robust and effective system.
## Possible Improvements


[Appendix A](/Appendix_A.md) | [Appendix B](/Appendix_B.md) | [Appendix C](/Appendix_C.md) | [Appendix D](/Appendix_D.md)
[Uploading Team 303 Verification.pdf…]()
