---
Title: User Needs Benchmarking
---
[Home](/index.md)| [Team organization](/Team_organization.md) | [User Needs, Benchmarking, and Requirements](/User_Needs_Benchmarking_Requirements.md) | [Design Ideation](/Design_Ideation.md) | [Selected Design](/Selected_Design.md) 
[Block Diagram of the product](/Block_Diagram_of_the_product.md) | [Component Selection](/Component_Selection.md) | [Microcontroller Selection](/Microcontroller_Selection.md) | [Final Hardware Implimentation](/Final_Hardware_Implementation.md) | [Final Software Implimentation](/Software_Proposal.md) | [System Verification](/System_Verification.md) | [Lessons Learned](/Lessons_Learned.md) | [Recommendations for future students](/Recommendations_for_future_students.md)


# User Needs, Benchmarking, and Requirements 
## Voices of Customers (VOC) Benchmarking 

 Five existing products that were reviewed were related to the ground-moving weather station. Products that are similar to the idea of the ground-moving weather station were chosen. Also, products that highlighted certain features were chosen. Even if it's not the exact product that is being made certain qualities or features help with possible designs. Each product has three positive and negative reviews and has consumer needs based on each of the reviews. If you want more information on the consumer reviews you can refer to [Appendix B](Appendix_B.md). The majority of our references are mostly existed weather measuring device with a usage in daily routine for a specific purposes. 


# Product Assessment

## Functionality

Check if all required systems and parts are in the product. Verify the accuracy and speed of data storage and transmission. Assess the product's response time under certain constraints. Ensure compatibility with devices for the WIFI connection.


## Usability:

There will be testing to identify any usability issues and  Evaluate the performance  of the user interface. The user feedback will be used to make improvements accordingly. Also, the ease of setup will be tested and adjusted based on consumer feedback.


## Reliability:

The product will be tested under different conditions. Monitor for flaws errors or vulnerabilities with the product. Assess the product's ability to handle prolonged usage. Implement fail-safes and error-handling mechanisms.


## Performance:

Measure data storage and WIFI connection strength and speed. Benchmark the product against similar solutions in the market.
Test the code and fix it for efficiency.


## Safety:


Conducts tests to make sure the product is safe for children and follows ASU safety guidelines. Check for the products' safety in accordance with the safety standards for the market. industry-specific standards. Use the feedback to add any additional safety if needed.

# Product Requirements Document

## Summary
The Mobile Weather Station, introduced in this Product Requirements Document, is envisioned to redefine weather tracking with its real-time monitoring of temperature, humidity, and wind speed. Tailored for a diverse user base, from professionals to outdoor enthusiasts, the device's objectives include serial sensing, MQTT data transmission, and motor control. Stakeholders range from outdoor workers to retailers, each with specific needs. Three use cases highlight the device's adaptability: Jenna utilizes it for business planning, William optimizes training, and Keith relies on it for road trips. The design focuses on portability, durability, and user-friendly interfaces, emphasizing lightweight, consistent power, multiple sensors, seamless data transfer, and affordability. Key functionalities encompass accurate data output, multi-purpose measurements, real-time updates, wireless connectivity, remote control, and scalability. User interaction features include guided setup, camera assistance, threshold conditions, intuitive interfaces, and customization options. Hardware specifications cover integration on a PCB, 3D printing, mobility across terrains, self-correction, and compatibility with spatial audio systems. Compliance with regulations, safety features, customization options, and thorough testing complete the holistic approach, positioning the Mobile Weather Station as a versatile and reliable tool for a wide audience.

## Introduction

Mobile weather stations have been a new way to track the weather yourself. With features to track temperature, humidity, and wind speed. Instead of staying indoors and checking through your phone or TV, you can check the weather forecast on your mobile weather station along with other relevant information such as storm warnings or highs and lows for temperature in the future.

## Objectives

The goal of this project is to produce systems that can respond to the environment using serial sensing and actuation in your system for a mobile weather station. The team will then output the data gathered to the internet over WiFi using the MQTT protocol. The system must sense at least 2 environmental conditions through at least 2 separate serial sensors: temperature, humidity, atmospheric pressure, and wind speed. other modalities with instructor approval. In addition, the team will need at least one motor controlled by a motor controller communicating over the I2C or SPI-based protocol.

## Stakeholders

Target group- This product is for people such as farmers, landscapers, or campers.

Target purchaser- This product is for people who spend time or have activities outdoors for long periods. People such as Wheater scientists report.

Customer service- Prefers a durable, smooth interface as well as easy to connect and set up over wifi or another app.

Retailers- Prefer products that can withstand a wide range of storage conditions including variations in temperature, vibration, and humidity.

## Use Cases

#### User Story #1: Jenna (Mobile Weather Station)

Jenna is a 33-year-old executive who regularly visits outdoor locations for work. She often needs to monitor weather conditions for business planning. Using her new portable weather station, Jenna can instantly switch between a mode that focuses on detailed weather data and a mode that combines weather information with the ambient sounds around her. The device also allows her to quickly adjust settings without having to take out her phone. Whether she's in a park or at a construction site, Jenna can efficiently gather weather data while staying connected to her surroundings.

#### User Story #2: William (Mobile Weather Station)

William is a 6’7” 26-year-old professional sprinter who trains outdoors every day. Accurate weather information is crucial for planning his training sessions. With the new portable weather station, which offers a custom fit for his preferences, William can monitor real-time weather conditions during his workouts. The device is sweat-resistant, ensuring that it stays securely in place. Additionally, he can track the location of his weather station through a dedicated app, providing him with valuable data for optimizing his training routine.

#### User Story #3: Keith (Mobile Weather Station)

Keith is a 45-year-old self-made man who enjoys traveling in his vintage car. As he often embarks on road trips, having a mobile weather station is essential for planning his journeys. Keith's wife Jennifer gifted him the portable weather station for Christmas, allowing him to access accurate weather information on the go. The device's noise reduction feature helps minimize distractions from wind noise when driving with the convertible roof down. Keith can also interact with the weather station using voice commands, enabling him to focus on driving while staying informed about changing weather conditions.

# Aspects

## 1. Product Design

1.1   The product shall be lightweight, and compact, for ease of transport.

1.2   The product should have a consistent and reliable power source that promotes longevity.

1.3 should include multiple sensors that can gather environmental data.

1.4   The product should be able to connect to a server or WIFI connection to a smartphone to transfer data smoothly.

1.5   The product should have a user interface that is user-friendly such as an app or server.

1.6   The product shall be able to collect and store data.

1.7   The product should be durable against moderate accidents or long-term use.

1.8   The product should be able to withstand moderate environmental obstacles such as heat.

1.9 The product should be affordable.

1.10 The product should be calibrated to ensure the components in the system operate as intended.


#### 2. Functionality

2.1   The product should be able to output accurate data.

2.2   The product should be multi-purpose. It should be able to measure different weather patterns. 

2.3   The product should be able to give real-time data that includes periodic updates. 

2.4   The product should be able to be connected wirelessly through wifi.

2.5   The product should operate efficiently on a given power supply.

2.6   The product should be able to be controlled remotely for mobility.

2.7   The product should be able to connect with different operating software. 

2.8   The product should operate efficiently given the system it operates in.

2.9   The product should be able to have some type of feedback for debugging.

2.10 The product should be able to be an appropriate scale for the user. 


#### 3. Interactivity

3.1   The product should be able to guide users in the initial process and setup. 

3.2   The product should have a camera to guide the user based on the desired location they want to go to.

3.3   The product should have conditions for certain thresholds containing the data it's collecting.

3.4   The product shall include a timer for data collection within a certain period.

3.5   The user interface shall be intuitive for all users after the setup. 

3.6   The product shall seamlessly connect to a server where the data is displayed.

3.7   The product shall offer different eyes to interact with the interface such as voice activation.

3.8   The product shall be designed to have basic security measures. 


#### 4. Hardware

4.1   The product shall be incorporated on a PCB. 

4.2   The product will be 3d printed to meet expat measurements. 

4.3   The product should be intuitive based on the setting it is placed in. 

4.4   The product should be able to move in different terrains to gather data.

4.5   The product should be able to correct its position or flip over. 

4.6   The product shall be compatible with spatial audio systems where sound becomes tuned to head orientation for a directional experience while watching a movie. 


#### 5. Customization

5.1   The user interface on the weather interface should be user-friendly. Such as dark mode or unit scaling. 

5.2   The product should run a 10-kilometer route by runners of different heights, ethnicities, and sexes. 

5.3   The product shall be offered with an additional engraving service for texts or icons onto the product. 

5.4   The product shall be offered in different colors for user-friendliness. 


#### 6. Regulations/Safety

6.1   The product shall meet regulations based on the objective of the class. 

6.2   The product should have a proximity sensor in case of potential accidents. 

6.3   The product should be user-appropriate depending on the age range. 

6.4   The product should be heat and cold-resistant. 

6.5   The Product should be resistant to certain chemicals that could eat away at the plastic 

6.6   The product should have eclectic safety to prevent shocks or short-circuiting. 

6.7   The product should be mechanically safe to prevent wounds or other bodily injuries. 

6.8   The product should have emergency protocols to prevent overheating. 

6.9   The product should be able = to get access to debug any issues that may arise 

6.10 The product should be tested for certain thresholds to be used publicly. 


#### Open Questions

·   	Can we move towards a recyclable and repairable product for environmental friendliness?  

·   	Can we improve on failing or self-igniting batteries?

·   	Can we improve  connectivity to wifi?

·   	Are there mechanisms for durability versatile)?

·   	What kind of observations can be made early on to avoid certain pitfalls?

[Appendix A](/Appendix_A.md) | [Appendix B](/Appendix_B.md) | [Appendix C](/Appendix_C.md) | [Appendix D](/Appendix_D.md)
