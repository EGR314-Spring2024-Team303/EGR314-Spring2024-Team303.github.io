---
Title: Final Hardware Implementation
---
[Home](/index.md) | [Team organization](/Team_organization.md) | [User Needs, Benchmarking, and Requirements](/User_Needs_Benchmarking_Requirements.md) | [Design Ideation](/Design_Ideation.md) | [Final Selected Design](/Selected_Design.md) 
[Final Block Diagram](/Block_Diagram_of_the_product.md) | [Final Component Selection](/Component_Selection.md) | [Microcontroller Selection](/Microcontroller_Selection.md) | [Final Hardware Implimentation](/Final_Hardware_Implementation.md) | [Final Software Implimentation](/Software_Proposal.md) | [System Verification](/System_Verification.md) | [Lessons Learned](/Lessons_Learned.md) | [Recommendations for future students](/Recommendations_for_future_students.md)

# Final Hardware Implementation

### Design Functionality: Addressing User Needs

As a mobile weather station, our project HAD to read and write weather data. Our team incorporated both an atmospheric pressure sensor and a temperature sensor. Both of our sensors utilized I2C protocol. This made it very easy to implement, as we only needed to add the sensor lines and their respective pull-up resistors. We feel that although this is a rudimentary system, our device provides enough data to keep our users informed on the current weather at that point in time. Our team also included an LED that would tell the user if the atmospheric pressure sensor has been clogged or blocked.

We also wanted a way to inform the user about severe temperature conditions that could risk system integrity. Our device implements a motor driver and a motor. We did this in order to lift a flag that would provide a visual queue to inform anyone in the vicinity that the surrounding temperature is above 100 degrees Fahrenheit. This is done by taking in data from the temperature sensor into the microcontroller. The microcontroller then communicates with the motor driver by using its SPI protocol. 

Our project includes two microcontrollers. One of them is the PIC18F27Q10, which runs code in C and offloads the majority of the computational portion of this device. However, the PIC Microcontroller cannot communicate wirelessly, it would be impossible for us to make it such. Our team would need to have a higher frequency signal than what the MCU is capable of, and impedance match the onboard antenna. This is another reason why we chose to use the ESP32. The ESP32 is able to connect to a webserver and displays relevant data with its built-in 2400 MHz antenna. The ESP32 is able to receive this data from PIC microcontroller through their respective RX and TX asynchronous serial pins. 

All of these components listed above need stable voltage. Our team used a 3.3v regulator and fuse. The regulator we used was the LM2575 switching buck regulator. This regulator provides 3.3 volts to all of the digital components. Switching regulators can be quite tricky to work out, but the efficiency is unrivaled by low dropout voltage regulators. This is imperative, our users would want a device to work for extended periods of time without recharging the battery. We utilized the typical circuit application in the datasheet in order to set the output voltage to 3.3 volts. 

### Version 2.0

There are many features and redesigns that we would want to implement in our final project. On a superficial level, we would want more sensors such as humidity, windspeed and a GPS. We would also want to change the schematic to provide 3.3 volts to the 3.3 volt pin on the ESP32. Currently, our 3.3 volts powers the voltage input pin. This means that when we use the micro-usb to the ESP for coding and debugging it powers the 3.3 volt line to 5 volts. This is the one thing that we didn't want to happen. We fixed this by cutting the trace and connecting it manually on the back with a wire, but will be changed in future production. In addition our 7.4 volt line that powers the motor should come after the fuse. In our current set up, if there is more than 40v or 3 amps applied to the input the motor driver will be rendered dysfunctional. This will be mitigated in the future design by changing that supply line after the fuse.

Our concept as a whole would benefit more from a more complex design. It was our vision to create a mobile weather station that could be deployed and run automatically in any condition. This would be achieved by using a more robust radio system that uses different radio frequencies and direct satellite connectivity. This could be done realistically by creating a mesh network with other nearby rovers or a starlink connection. It would also be highly desired to put a camera on these rovers that would give a low-latency video signal to a master network. 

![image](https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/f082cddd-9d6d-4206-ad86-2fa4284f2c19)

[Appendix A](/Appendix_A.md) | [Appendix B](/Appendix_B.md) | [Appendix C](/Appendix_C.md) | [Appendix D](/Appendix_D.md)




