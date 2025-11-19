# Multi-Tank Water Level Management and Automation System

An IoT-based automated water management system that intelligently monitors and controls water levels across multiple tanks, preventing water wastage and eliminating the need for manual supervision.

## 🌟 Project Overview

This system automates the complete water tank filling process in multi-tank setups (common in households and buildings). It uses float sensors, solid-state relays, and a microcontroller to:

- **Automatically maintain water levels** across multiple connected tanks
- **Prevent water pump dry runs** by checking source tank levels before starting pumps
- **Eliminate water wastage** by shutting off pumps when tanks reach maximum capacity
- **Detect municipal water arrival** and initiate automatic filling sequences
- **Require zero human supervision** once installed

## 🎯 Key Features

- **Multi-Tank Support**: Manages cascading tank systems where Tank 1 fills Tank 2, Tank 2 fills Tank 3, etc.
- **Smart Water Detection**: Detects when municipal water becomes available and automatically starts the filling process
- **Dry Run Protection**: Prevents pump damage by verifying source tank has sufficient water before activating
- **Zero Water Wastage**: Automatically stops filling when tanks reach full capacity
- **Low Cost**: Uses affordable, standard components (float sensors, solid-state relays, ESP8266)
- **No Internet Required**: Operates independently without internet connectivity
- **Low Power**: Runs on minimal energy (12V DC)

## 🏗️ System Architecture

### Components Used

- **Microcontroller**: ESP8266
- **Water Level Sensors**: Float sensors (2 per tank - top and bottom)
- **Switching Mechanism**: Solid-state relays (SSR-60DA, 3-32VDC/24-380VAC 60A)
- **Water Control**: 12V DC solenoid valve (normally closed)
- **Power Supply**: 12V DC

### How It Works

1. Float sensors continuously monitor water levels in each tank
2. When a tank's water level drops below threshold, the bottom float sensor signals the microcontroller
3. Microcontroller checks if the source tank has sufficient water
4. If source tank is adequate, the corresponding solid-state relay activates the water pump
5. Pump runs until the destination tank's top float sensor indicates full capacity
6. System automatically shuts off pump and proceeds to next tank if needed

For municipal water:
- Small container with float sensor detects water arrival
- Solenoid valve opens to allow flow
- System fills Tank 1 through the automated process
- Solenoid valve closes when Tank 1 is full, preventing overflow

## 💡 Technical Highlights

- **Real-time Processing**: Sensor data processed in real-time for immediate response
- **Cascading Logic**: Intelligent tank-filling sequence prevents bottlenecks
- **Fail-safe Design**: Multiple safety checks prevent equipment damage
- **Modular Architecture**: Easy to extend for additional tanks
- **Simple Implementation**: Basic programming knowledge sufficient for setup

## 🛠️ Software Requirements

- **Arduino IDE**: For developing and uploading code to ESP8266
- **Programming Language**: C++
- **Libraries**: Standard ESP8266 libraries (included in Arduino IDE)

## 📊 System Benefits

✅ **Zero supervision required** - completely autonomous operation  
✅ **Water conservation** - eliminates overflow and wastage  
✅ **Equipment protection** - prevents pump dry runs and damage  
✅ **Cost-effective** - low implementation and zero operating costs  
✅ **Reliable** - no internet dependency, minimal points of failure  
✅ **Scalable** - easily expandable to more tanks

## 🎓 Credits

**Concept & Innovation**: Aditya Babasaheb Mandlik  
**Co-Inventor**: Akshay Mohan Sawade

*This project was developed as part of a patent filing for an innovative IoT solution addressing water management challenges in multi-tank systems.*

## 📄 Patent Information

This system is protected under patent application filing with innovative approaches to:
- Multi-tank water level automation
- Municipal water arrival detection
- Dry run prevention mechanisms
- Automated solenoid valve control for water conservation

## 🔮 Future Enhancements

- Mobile app integration for remote monitoring
- Water consumption analytics and reporting
- Multiple source support (borewell + municipal)
- Integration with smart home systems
- Leak detection capabilities

## 📝 License

Patent Pending - All rights reserved

---

**Note**: This is an IoT-based automation system designed to address real-world water management challenges. The system has been prototyped and tested successfully.
