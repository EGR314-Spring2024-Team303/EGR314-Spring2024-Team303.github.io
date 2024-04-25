---
title: Final Component Selection 
---
[Home](/index.md) | [Team organization](/Team_organization.md) | [User Needs, Benchmarking, and Requirements](/User_Needs_Benchmarking_Requirements.md) | [Design Ideation](/Design_Ideation.md) | [Final Selected Design](/Selected_Design.md) 
[Final Block Diagram](/Block_Diagram_of_the_product.md) | [Final Component Selection](/Component_Selection.md) | [Microcontroller Selection](/Microcontroller_Selection.md) | [Final Hardware Implimentation](/Final_Hardware_Implementation.md) | [Final Software Implimentation](/Software_Proposal.md) | [System Verification](/System_Verification.md) | [Lessons Learned](/Lessons_Learned.md) | [Recommendations for future students](/Recommendations_for_future_students.md)

# Final Component Selection 

## Motor Driver 
<img src="https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/d3d621fa-b87c-4e78-943a-27085d5b9e3b" width = "300" height = "300">

* IFX9201SGAUMA1-6A H bridge with SPI Motor Driver

Our team picked IFX9201SG. This particular surface mount H-bridge model has an SPI interface which our team had already experienced in one of the ICC. 
So, our team is confident to work around this component. Moreover, the component's operating voltage range is 3.3V - 5.0V. 

## Temperature Sensors 
<img src ="https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/2faca3f8-fac7-4f8a-b503-419a9ad86b02" width = "300" height = "300">

* TC74A4-3.3VCTTR Surface Mount Temperature Sensor

Our team chose The TC74. Since the components are I2C, it is easier to implement with a wide range of microcontrollers. It's tiny in size so it won't interfere with other components on 
a PCB. Moreover, it's already provided in class so it's cost-effective, and our team would be more familiar with working around it. 

# Barometric Sensors
<img src ="https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/f21d38a9-6406-4f76-886d-1444f8d43790" width = "300" height = "300">

 * SM9543-005M-D-C-3-S TE Connectivity / SMI Mouser Surface mount Barometric sensor
      
Our team chose SM9543. This model of the barometric pressure sensor compared to other models is bulkier than other models but at the same time compact enough to fit in a small project. 
It's easy to solder and operate with I2C Interface. 

## Motor 
<img src="https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/3d5246d1-1888-48c5-8ac1-d3f23bc936a3" width ="400" height ="300">
  
   * DC3V-12V DC Geared Motor

Of all the models, we found this model is a good fit for our project. This motor model provides a good amount of RPM and it also operates from 3V to 12V
which is also a good fit for the integration into our project. On top of that, it's cost-effective.
  
## Battery
<img src="https://github.com/EGR314-Spring2024-Team303/EGR314-Spring2024-Team303.github.io/assets/156623314/df8f2404-8f6a-479f-bbb0-057acae989e3" width ="300" height="300">

* ICR18650 2200mAh 3.7V

This battery has a higher discharge rate. On top of that, the energy density will make sure that the motors and the PCB can run for a longer period.
It also makes it easier with the outer shell being more protected this is very important as we do not want our batteries becoming puffy and exploding when they are potentially     
penetrated.

# Power Budget

According to our [Power Budget Spreadsheet](/Appendix_C.md) our team on board battery will last roughly 3 hours in the most power-hungy conditions. This is acceptable as we want our weather station to collect data for extended periods. In future designs, our device will be able to drive for hours at a time and record weather data for days on end with power efficacy gained by choosing different components.

Our most pressing matters for the power consumption would be the temperature sensor and the Microcontrollers. All of these components draw hundreds of milliamps of current as other components draw tens of milliamps. It should be noted that the Wifi module will always be a power-hungry device as it needs to transmit data in the gigahertz range and run the web server.  

[Appendix A](/Appendix_A.md) | [Appendix B](/Appendix_B.md) | [Appendix C](/Appendix_C.md) | [Appendix D](/Appendix_D.md)
 

