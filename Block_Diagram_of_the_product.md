---
Title: Final Block Diagram 
---
[Home](/index.md) | [Team organization](/Team_organization.md) | [User Needs, Benchmarking, and Requirements](/User_Needs_Benchmarking_Requirements.md) | [Design Ideation](/Design_Ideation.md) | [Selected Design](/Selected_Design.md) 
[Block Diagram of the product](/Block_Diagram_of_the_product.md) | [Component Selection](/Component_Selection.md) | [Microcontroller Selection](/Microcontroller_Selection.md) | [Final Hardware Implimentation](/Final_Hardware_Implementation.md) | [Final Software Implimentation](/Software_Proposal.md) | [System Verification](/System_Verification.md) | [Lessons Learned](/Lessons_Learned.md) | [Recommendations for future students](/Recommendations_for_future_students.md)

# Final Block Diagram of the product 
![Block Diagram-314 (1)](https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/bbce8f6a-56d2-4d08-9275-a05007e62109)

For our block diagram, we developed the diagram with a given template and then improvised with a project requirement as a guideline. We started by looking for a microcontroller with 2 I2C lines and at least 1 SPI, then we decided to use a class-given temp sensor and motor driver as it's the most familiar electrical components to our team. We add an atmospheric pressure sensor to achieve two serial sensors on one PCB requirement. In conclusion, Our team has opted for a temperature sensor to operate the motor as a flag raiser. Additionally, both temperature and atmospheric sensors will collect data, which will then be transmitted to the terminal via WiFi using ESP32. This entire operation will be managed by the microcontroller.

[Appendix A](/Appendix_A.md) | [Appendix B](/Appendix_B.md) | [Appendix C](/Appendix_C.md) | [Appendix D](/Appendix_D.md)
