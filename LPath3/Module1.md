# [Choose the best Azure IoT service for your application](https://docs.microsoft.com/en-us/learn/modules/iot-fundamentals/)
## Module 1 - has 8 units
### UNIT 1: Introduction
-  Azure IoT services across many different facets of their operations, from new product development to logistics and point-of-sale
- Identify the best Azure IoT service
---
### UNIT 2: Identify the product options
- Sensors like
```
Environmental sensors that capture temperature and humidity levels.
Barcode, QR code, or optical character recognition (OCR) scanners.
Geo-location and proximity sensors.
Light, color, and infrared sensors.
Sound and ultrasonic sensors.
Motion and touch sensors.
Accelerometer and tilt sensors.
Smoke, gas, and alcohol sensors.
Error sensors to detect when there's a problem with the device.
Mechanical sensors that detect anomalies or deformations.
Flow, level, and pressure sensors for measuring gasses and liquids.
```
- **IoT Hub**
  -  a central message hub for bidirectional message passing
  -  **IoT Hub monitoring**
  - track health by events like - device creation, failure, device connections 

- **Azure IoT Central**
  -  builds **_on top of IoT Hub by adding a dashboard_** that allows you to connect, monitor, and manage your IoT devices. 
  -  The **visual user interface (UI)** makes it easy to quickly connect new devices and watch as they begin sending telemetry or error messages.
  -  You can _watch the overall performance_ , _can set up alerts that send notifications_ when a specific device needs maintenance. Finally, you can _push firmware updates_ to the device.

  - Speciality of IoT central is device templates - 
      - _usually no code on server side_
      - but needs coding on dev side to match the template

- **Azure Sphere**
  - Azure Sphere creates an end-to-end, highly secure IoT solution for customers 
  - Comprehensive IoT security solution
    - including hardware (crossover microcontroller), OS, and cloud components for IoT device security
    - to actively protect your devices, your business, and your customers

  ![image](https://user-images.githubusercontent.com/43994542/119222366-b62a5d80-bb11-11eb-91af-994c0bd777e4.png)
  - Azure Sphere comes in three parts:
  1. The first part is the Azure Sphere micro-controller unit (MCU), 
  2. The second part is a customized Linux operating system (OS) that handles communication with the security service and can run the vendor's software.
  3. The third part is Azure Sphere Security Service, also known as AS3.
      - It authenticates n only then device can send telemetry
---
### UNIT 3: Analyse decision criteria
- Security of device
  - appln specific - ATM >>>> importance Washing machine
  - Use **sphere** for more secure
- Dashboard
  - No need - **use IoT hub**
  - control through alerts, push - use templates - **use IoT Central **
---
### UNIT 4: Use IoT hub
> The Tailwind Traders senior leadership team has decided to partner with a leading appliance manufacture to create an exclusive, high-end brand that promises a preemptive maintenance service agreement. This unique feature would differentiate Tailwind Traders appliances in a crowded, competitive market. The feature also makes the brand lucrative, because a yearly subscription would be required. To build a strong brand reputation, the appliances will send telemetry information to a centralized location, where it can be analyzed and maintenance can be scheduled. The devices will not require remote control. They will merely be sending their telemetry data for analysis and pro-active maintenance. Because Tailwind Traders already has software in place for managing appliance maintenance requests, the company wants to integrate all functionality into this existing system.

- Explain the decision criteria and why not Central or Sphere

---
### UNIT 5: Use IoT central
> Tailwind Traders owns a fleet of delivery vehicles that transport products from warehouses to distribution centers, and from distribution centers to stores and homes. The company is looking for a complete logistics solution that takes data sent from an onboard vehicle computer and turns it into actionable information.
Furthermore, shipments can be outfitted with sensors from a third-party vendor to collect and monitor ambient conditions. These sensors can collect information such as the temperature, humidity, tilt, shock, light, and the location of a shipment.
- A few goals of this logistics system include:
   1. Shipment monitoring with real-time tracing and tracking.
   1. Shipment integrity with real-time ambient condition monitoring.
   1. Security from theft, loss, or damage of shipments.
   1. Geo-fencing, route optimization, fleet management, and vehicle analytics.
   1. Forecasting for predictable departure and arrival of shipments.
    The company would prefer a pre-built solution to collect the sensor and vehicle computer data, and provide a graphical user interface that displays reports about shipments and vehicles.

---
### UNIT 6: Use Azure Sphere
> Tailwind Traders wants to implement a **touchless point-of-sale solution for self-checkout**. The self-checkout terminals should be, above all else, secure. Each terminal must be impervious to malicious code that could create fraudulent transactions, force the company to take the systems offline during a heavy shopping period, or send transactional data to a spying organization. The terminals should also report back vital information on the company's health and allow secure updates to its software remotely. 
   After reviewing many possible solutions during a request for proposal process, Tailwind Traders decides that it needs features that vendors have yet to implement. Instead of using an existing solution, the company decides to work with a leading engineering firm that specializes in IoT solutions. This approach allows the company to build a uniquely secure terminal that gives it a retail platform to build on going forward. 
  Although most of the company's focus is on the terminal itself, Tailwind Traders realizes that it wants a solution that can help it make sense of all the data that will be generated by these terminals across all of its retail stores. And it wants an easy way to push software updates to its terminals.

**Platform on top of both Azure IoT Central and Azure Sphere.**

---
### UNIT 7: Knowledge check

![image](https://user-images.githubusercontent.com/43994542/119223333-70bc5f00-bb16-11eb-8ad1-51c0c54dd430.png)

---
### UNIT 8: Summary
- Without Azure IoT services, receiving messages from devices might still be possible, but it would likely be much less secure and require custom development to implement a dashboard for reporting and management. It would also be more difficult to push software or firmware updates to each device.
- Sensor and device driven = IoT best!!

---
