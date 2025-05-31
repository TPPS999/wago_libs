WAGO Libraries Documentation Hub
This repository contains comprehensive documentation for WAGO PLC libraries, providing detailed information about function blocks, data types, usage examples, and best practices for industrial automation applications.
📚 Library Documentation Index
Communication & Networking

WagoAppSunspec - SunSpec communication library for solar inverters via Modbus TCP/RTU protocol
WagoAppDLMS - DLMS (Device Language Message Specification) library for intelligent power meter communication
WagoAppCom - Serial communication interface library
WagoAppCanLayer2 - CAN Layer2 communication functionality
WagoAppCanOpen - CANopen protocol implementation
WagoAppCloud - Cloud connectivity and MQTT communication
WagoAppBACnet - BACnet protocol support
WagoAppASi - AS-Interface communication protocols

Building Automation & HVAC

WagoAppBuilding - Building automation control functions
WagoAppBuildingHVAC - Comprehensive HVAC control and monitoring
WagoAppBuildingHVAC_BACnet - HVAC control with BACnet integration
WagoAppDALI - DALI lighting control systems

Energy Management

WagoAppEnergyDevices - Energy device communication and control

Control & Automation

WagoAppControlSuite - Advanced control functions and autotune controllers
WagoAppControl - Application control and management
WagoAppDCDriveController - DC motor drive control

Utilities & Tools

WagoAppTime - Time and date handling operations
WagoAppAppLED - Application LED control and status indication
WagoAppColorConverter - Color management and conversion
WagoAppConfigTool - Configuration and setup tools
WagoAppDatalogger - Data logging functionality

Specialized Interfaces

WagoAppBluetooth - Bluetooth connectivity
WagoAppDMX - DMX lighting protocol
WagoAppDigitalImpulseInterface - Digital impulse processing

🚀 Quick Start Guide
Basic Library Usage Pattern
iecVAR
    fbInstance: FunctionBlockName;
    xEnable: BOOL;
    // Configure other inputs
END_VAR

// Call the function block
fbInstance(
    xEnable := xEnable,
    // Other parameters
);

// Check status
IF fbInstance.xValid THEN
    // Operation successful
    // Access output data
END_IF

IF fbInstance.xError THEN
    // Handle error
    // Check fbInstance.eStatus for specific error codes
END_IF
Error Handling Best Practice
iecIF fbInstance.xError THEN
    CASE fbInstance.eStatus OF
        0: // Success
        1: // Specific error code 1
        2: // Specific error code 2
        // Handle other error codes
    END_CASE
END_IF
🔍 Search Index
By Functionality
Communication Protocols

Modbus TCP/RTU: WagoAppSunspec, WagoAppDLMS, WagoAppEnergyDevices
CAN/CANopen: WagoAppCanLayer2, WagoAppCanOpen
MQTT/Cloud: WagoAppCloud
BACnet: WagoAppBACnet, WagoAppBuildingHVAC_BACnet
DALI: WagoAppDALI
DMX: WagoAppDMX
Serial: WagoAppCom
AS-Interface: WagoAppASi

Building Automation

HVAC Control: WagoAppBuildingHVAC, WagoAppBuildingHVAC_BACnet
Lighting: WagoAppDALI, WagoAppDMX, WagoAppColorConverter
General Building: WagoAppBuilding

Control Systems

PID Controllers: WagoAppControlSuite
Motor Control: WagoAppDCDriveController
Application Control: WagoAppControl

Energy & Metering

Solar Inverters: WagoAppSunspec
Power Meters: WagoAppDLMS
Energy Devices: WagoAppEnergyDevices

Utilities

Time/Date: WagoAppTime
Data Logging: WagoAppDatalogger
Configuration: WagoAppConfigTool
LED Control: WagoAppAppLED

By Device Type
Solar & Energy

Fronius, Kaco, Kostal, SMA, SolarEdge inverters: WagoAppSunspec
Smart meters (DLMS): WagoAppDLMS
Various energy devices: WagoAppEnergyDevices

HVAC Equipment

Fans, pumps, dampers: WagoAppBuildingHVAC
Boilers, heat exchangers: WagoAppBuildingHVAC
Temperature controllers: WagoAppControlSuite

Lighting Systems

DALI devices: WagoAppDALI
DMX fixtures: WagoAppDMX
RGB lighting: WagoAppColorConverter

📖 Documentation Features
Each library documentation includes:

Overview: Key features and capabilities
Function Blocks: Detailed descriptions of all available function blocks
Data Types: Custom data structures and enumerations
Usage Examples: Practical code examples
Best Practices: Recommended implementation patterns
Error Handling: Status codes and troubleshooting
Performance Notes: Optimization tips and considerations

🔧 Common Patterns
Function Block Lifecycle

Declaration: Declare function block instances in VAR section
Configuration: Set up input parameters and configuration structures
Execution: Call function block cyclically in program
Status Check: Monitor xValid, xError, and eStatus outputs
Data Access: Read output values when operation is successful

Error Management

Always check xError output for fault conditions
Use eStatus for specific error identification
Implement retry logic for communication errors
Handle timeouts and connection failures gracefully

Performance Optimization

Use appropriate polling intervals for communication
Consider device response times in timing design
Implement proper error recovery mechanisms
Test thoroughly in target environment

📝 Version Information
All libraries are documented with their respective version numbers. Always refer to the official WAGO documentation for the most current information and compatibility details.
🎯 Target Applications

Industrial Automation Systems
Building Management Systems (BMS)
HVAC Control Systems
Energy Management Systems
Lighting Control Systems
Process Control Applications
Data Acquisition Systems


This documentation hub provides searchable access to WAGO PLC library information. For official support and updates, consult WAGO's technical documentation and support resources.
