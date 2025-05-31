# WAGO PLC Libraries Documentation

This repository contains comprehensive documentation for WAGO PLC libraries, providing detailed information about function blocks, data types, and usage examples for industrial automation applications.

## 📚 Available Libraries

### Communication & Networking

- **WagoAppSocket** - Socket communication (TCP/UDP clients/servers, broadcast, multicast)
- **WagoAppHTTP** - HTTP/HTTPS client functionality for web service integration
- **WagoAppFTP** - FTP, FTPS, and SFTP client services for file transfer
- **WagoAppSNMP** - SNMP v1/v3 management and trap functionality
- **WagoAppPlcModbus** - Comprehensive Modbus master/slave implementation
- **WagoAppSiemensS7Protocol** - Siemens S7 protocol communication
- **WagoSysSocket** - Low-level socket operations and BSD socket interface
- **WagoSysBSDSocket** - BSD socket implementation with POSIX-like API
- **WagoSysSSL** - SSL/TLS encryption for secure communications
- **WagoSysCurl** - HTTP client library with cURL functionality
- **WagoSysCloud** - Cloud connectivity and agent communication
- **WagoTypesSocket** - Socket communication type definitions and base classes
- **WagoTypesModbus** - Modbus communication type definitions
- **WagoTypesSNMP** - SNMP protocol type definitions
- **WagoTypesSSL** - SSL/TLS type definitions and structures
- **WagoTypesCurl** - cURL library type definitions

### Serial Communication

- **WagoAppSerial_GENIbus** - GENIbus protocol for GRUNDFOS devices
- **WagoAppSerial_Fitron** - Fitron device communication
- **WagoAppSerial_3964R_RK512** - 3964R and RK512 protocols
- **WagoAppSerial_Modem** - Modem handling and control
- **WagoAppSerial_Scanner** - Barcode scanner integration
- **WagoAppSerial_Sms** - SMS sending/receiving via GSM modems
- **WagoAppSerial_NMEA** - NMEA sentence processing for GPS/marine devices
- **WagoAppSerial_ebmBus** - ebmBus protocol for motor control
- **WagoSysSerial** - Low-level serial communication interface
- **WagoSysModem** - Modem control and AT command interface
- **WagoTypesCom** - Serial communication type definitions (TTY, RS485, handshake)
- **WagoTypesModem** - Modem communication type definitions

### BACnet & Building Automation

- **WagoSysBACnet** - Complete BACnet protocol stack with objects and services
- **WagoSolRoomApp** - Room automation functions for lighting and HVAC control
- **WagoSolWeihenstephan** - Weihenstephan protocol server implementation
- **WagoTypesBACnet** - BACnet protocol type definitions and object structures
- **WagoSysVisuBACnet** - BACnet visualization support

### Industrial Protocols & Standards

- **WagoAppM_Bus** - M-Bus master for utility meter reading
- **WagoAppMP_Bus** - MP-Bus for BELIMO HVAC devices
- **WagoAppSMI** - SMI (Standard Motor Interface) for blind/shutter control
- **WagoAppHART** - HART protocol for process automation
- **WagoAppEnocean** - EnOcean wireless sensor/actuator communication
- **WagoSysDps** - PROFIBUS DP slave functionality

### CANopen & CAN Communication

- **WagoSysCan** - CAN interface and CANopen stack implementation
- **WagoTypesCan** - CAN communication type definitions and enumerations
- **WagoTypesCanExtra** - Extended CAN type definitions

### Hardware Control & Monitoring

- **WagoAppPowerMeasurement** - Power measurement modules (750-493/494/495)
- **WagoAppPowerSupply** - Power supply module control and monitoring
- **WagoAppStepper** - Stepper motor control (750-670/671/672/673)
- **WagoAppSolenoid** - Proportional valve control (750-632/1632)
- **WagoAppFuse** - Electronic fuse management (787-series)
- **WagoAppIOLink** - IO-Link master configuration and device handling
- **WagoAppVibrationMonitoring** - Vibration monitoring systems
- **WagoAppSafety** - Safety system communication and diagnostics
- **WagoSysEdgeController** - Edge computing functionality
- **WagoSysProcessorLoad** - CPU load monitoring and performance analysis
- **WagoTypesProcessorLoad** - Processor load monitoring type definitions

### K-Bus & I/O Module Support

- **WagoSysKbusServices** - K-Bus terminal services and configuration
- **WagoSysKbusTerminalControl** - Terminal control and process data exchange
- **WagoSysKbusAsyncCom** - Asynchronous K-Bus communication
- **WagoSysKbusModule** - Standard K-Bus module function blocks
- **WagoSysFieldbusModule** - Fieldbus-connected module support
- **WagoSysModuleBase** - Base classes for module implementations
- **WagoSysDynamicIoMapping** - Dynamic I/O mapping and configuration
- **WagoTypesModuleBase** - Base classes and common types for module implementations
- **WagoTypesBusServices** - Bus services type definitions and terminal data
- **WagoTypesKbusTerminalControl** - K-Bus terminal control type definitions

### Module-Specific Libraries

#### Temperature & Analog Input Modules
- **WagoSysModule_750_450** - Temperature input module (RTD/TC/Voltage)
- **WagoSysModule_750_451** - Temperature input module (RTD/TC)
- **WagoSysModule_750_463** - Thermocouple input module (2-channel)
- **WagoSysModule_750_464** - Thermocouple input module (4-channel)
- **WagoSysModule_75x_458** - 8-channel analog input
- **WagoSysModule_75x_461** - Analog input module (single-ended)
- **WagoSysModule_75x_469** - High-precision analog input (thermocouple)
- **WagoSysModule_75x_471** - Universal analog input
- **WagoSysModule_75x_481** - Thermocouple input module
- **WagoSysModule_75x_486** - 8-channel voltage/current input
- **WagoSysModule_75x_487** - 8-channel thermocouple input
- **WagoSysModule_75x_489** - 4-channel current/voltage input
- **WagoSysModule_75x_496** - 4-channel RTD input
- **WagoSysModule_75x_497** - 8-channel RTD input
- **WagoSysModule_75x_498** - RTD/resistance input module

#### Analog Output Modules
- **WagoSysModule_75x_562** - 2-channel analog output (voltage/current)
- **WagoSysModule_75x_563** - 4-channel analog output module
- **WagoSysModule_75x_564** - 4-channel current output module
- **WagoSysModule_75x_597** - 8-channel voltage output module

#### Digital I/O & Special Function Modules
- **WagoSysModule_750_630** - RTC module with calendar functions
- **WagoSysModule_750_636** - DeviceNet slave module
- **WagoSysModule_750_642** - Incremental encoder interface
- **WagoSysModule_750_643** - 2-channel encoder interface
- **WagoSysModule_75x_511** - PWM output module
- **WagoSysModule_75x_632** - Proportional valve output (single channel)
- **WagoSysModule_75x_633** - Encoder interface module (SSI/incremental)
- **WagoSysModule_75x_635** - Profibus master module
- **WagoSysModule_75x_640** - 16-channel relay output
- **WagoSysModule_75x_644** - 4-channel relay output
- **WagoSysModule_75x_645** - Digital input/output module
- **WagoSysModule_75x_655** - DeviceNet master module
- **WagoSysModule_75x_657** - Ethernet TCP/IP module
- **WagoSysModule_75x_658** - CAN gateway module
- **WagoSysModule_75x_677** - Incremental encoder interface (multi-channel)

#### Communication & Serial Interface Modules
- **WagoSysModule_75x_49x** - Serial interface modules (RS232/485)
- **WagoSysModule_75x_48x** - Serial communication modules
- **WagoSysModule_75x_65x** - TTY interface modules
- **WagoSysModule_75x_66x** - Safety I/O modules with diagnostics
- **WagoSysModule_75x_67x** - Profibus DP slave modules

#### Specialized Modules
- **WagoSysModule_75x_1491** - Strain gauge input module
- **WagoSysModule_75x_1632** - Multi-channel proportional valve output
- **WagoSysModule_75x_1657** - Ethernet switch module
- **WagoSysModule_753_646** - Profibus master module (753 series)
- **WagoSysModule_753_647** - CAN master module (753 series)
- **WagoSysModule_753_649** - Ethernet switch module (753 series)
- **WagoSysModule_753_163x** - Fieldbus coupler modules
- **WagoSysModule_753_1646** - Advanced communication module

### Data Management & Cloud

- **WagoAppInfluxDB** - InfluxDB v1.x/v2.0 time-series database integration
- **WagoAppSQL_MySQL** - MySQL database connectivity
- **WagoAppSQL_MsSQL** - Microsoft SQL Server integration
- **WagoAppJSON** - JSON parsing, creation, and manipulation
- **WagoAppSparkplug** - Eclipse Sparkplug MQTT specification
- **WagoAppTOPASS** - TO-PASS web service integration
- **WagoAppPvForecast** - Photovoltaic forecast data from WAGO Cloud
- **WagoSysSQL_SQLite** - SQLite database support
- **WagoTypesSQL_SQLite** - SQLite database type definitions

### System & Utilities

- **WagoAppTime** - Time/date operations, timezones, elapsed time, timeouts
- **WagoAppScheduler** - Time-based scheduling with holiday/special period support
- **WagoAppEvent** - Event handling and catching system
- **WagoAppMem** - Shared memory management for inter-process communication
- **WagoAppFileDir** - File and directory operations
- **WagoAppMath** - Mathematical functions (exponential, etc.)
- **WagoAppString** - String manipulation utilities
- **WagoAppWString** - Wide string (Unicode) operations
- **WagoAppProcessorLoad** - CPU load monitoring
- **WagoAppRTC** - Real-time clock and GPS-DCF converter support
- **WagoSysTime** - Core time handling and calendar functions
- **WagoSysFileDir** - Low-level file and directory operations
- **WagoSysString** - Core string manipulation functions
- **WagoSysStandard** - Standard system functions and utilities
- **WagoSysPlainMem** - Plain memory operations and data type conversions
- **WagoSysFifo** - FIFO buffer implementation
- **WagoSysLog** - System logging and message handling
- **WagoSysErrorBase** - Error handling and result management
- **WagoSysAsync** - Asynchronous operation framework
- **WagoSysBehaviourModels** - Behavior model base classes
- **WagoSysAtomic** - Atomic operations for thread safety
- **WagoSysProcess** - Process control and management
- **WagoSysUtils** - System utilities and exclusivity handling
- **WagoSysVirtualBuffer** - Virtual buffer management for data streaming
- **WagoSysVersion** - System version information
- **WagoSysTouchPanel** - Touch panel interface support
- **WagoSysTree** - Tree structure data management
- **WagoTypesCommon** - Common type definitions and utilities
- **WagoTypesErrorBase** - Error handling base types
- **WagoTypesEvent** - Event handling type definitions
- **WagoTypesLog** - Logging system type definitions
- **WagoTypesTree** - Tree data structure types
- **WagoSysTypedefs_Debugging** - Debugging support type definitions
- **WagoSysTypedefs_Pointer** - Pointer manipulation utilities
- **WagoSysTypedefs_Internal_32Bit** - 32-bit internal system types
- **WagoTypesAsync_Internal_PFC** - PFC-specific asynchronous types
- **WagoTypesAsync_Internal_Template** - Template for asynchronous operations

### Application LED Control

- **WagoSysAppLED** - Application LED control with patterns and sequences
- **WagoTypesAppLED** - Application LED control type definitions with color and pattern support

### Visualization & User Interface

- **WagoVisuIcons** - Standard visualization icons
- **WagoVisuIconsMaterialDesign** - Material Design icons for visualization
- **WagoSysVisuStandard** - Standard visualization components
- **WagoSysVisuTree** - Tree view visualization components

### Security & DRM

- **WagoSysDRM** - Digital Rights Management functionality
- **WagoSysDrmInterface** - DRM interface definitions

### Solution-Specific Libraries

- **WagoSolOppermann** - Oppermann HVAC sensor integration
- **WagoSolEAP** - EAP room operating units (RBG1)
- **WagoSolElsner** - Elsner weather station integration
- **WagoSolHKW** - HKW weather forecast stations
- **WagoSolMennekes** - Mennekes charging point control
- **WagoAppWeatherForecast** - Weather data from multiple providers
- **WagoAppMail** - SMTP email functionality with attachments
- **WagoAppRFIDReader_phg** - PHG RFID reader integration
- **WagoSolThies** - Thies weather station integration
- **WagoSolThermokon** - Thermokon room automation devices
- **WagoSolRomutec** - Romutec LED control and communication
- **WagoSolSplusS** - S+S Regeltechnik sensor integration
- **WagoSolSolutionBuilder** - Solution Builder framework components

## 🚀 Key Features

### Professional Integration
- Comprehensive error handling and status reporting
- Standardized interfaces across all libraries
- Extensive documentation with usage examples
- Compatible with WAGO PLC hardware ecosystem

### Communication Excellence
- Multiple protocol support (Modbus, BACnet, HART, EnOcean, etc.)
- Network communication (TCP/UDP, HTTP/HTTPS, FTP/SFTP)
- Serial communication with various protocols
- Wireless and wired connectivity options
- SSL/TLS encryption support

### Industrial Standards
- Support for major automation protocols
- Energy management and monitoring
- Safety and diagnostics integration
- Real-time data processing capabilities
- Building automation (BACnet, room control)

### Hardware Integration
- Comprehensive K-Bus module support
- Dynamic I/O mapping capabilities
- Module-specific function blocks
- Fieldbus connectivity
- Edge computing functionality

### Advanced Module Support
- Temperature measurement (RTD, thermocouple, voltage)
- Analog I/O with high precision
- Digital I/O with safety functions
- Encoder interfaces (incremental, SSI)
- Communication modules (serial, Ethernet, CAN, Profibus)
- Specialized functions (strain gauge, proportional valves)

## 📖 Documentation Structure

Each library documentation includes:

- **Overview** - Library purpose and key features
- **Core Function Blocks** - Detailed FB descriptions with parameters
- **Data Types** - Enumerations and structures
- **Usage Examples** - Practical implementation samples
- **Best Practices** - Error handling and performance guidelines
- **Important Notes** - Hardware compatibility and limitations

## 🛠 Getting Started

1. Select the appropriate library for your application needs
2. Review the function blocks and their capabilities
3. Study the usage examples to understand implementation
4. Follow best practices for error handling and performance
5. Test thoroughly in your specific environment

## 💡 Best Practices

### Error Handling
```iec
IF fbInstance.xError THEN
    CASE fbInstance.eStatus OF
        // Handle specific error codes
    END_CASE
END_IF
```

### Performance Considerations
- Use appropriate polling intervals
- Handle communication errors gracefully
- Consider device response times
- Test thoroughly in target environment

## ⚠️ Important Notes

- Documentation automatically generated from XML specifications
- Always refer to official WAGO documentation for complete details
- Test thoroughly in your specific application environment
- Check library compatibility with your PLC hardware
- Version requirements may vary between libraries

## 🔧 Hardware Compatibility

These libraries are designed for WAGO PLC systems and require:

- Compatible WAGO controller (750/752/753 series)
- Appropriate I/O modules for specific applications
- Proper network and serial interface configuration
- Required communication modules for protocol-specific libraries

### Supported Module Series

- **750 Series** - Standard I/O modules with K-Bus interface
- **752 Series** - Advanced controller modules
- **753 Series** - Fieldbus coupler and gateway modules
- **75x Series** - Generic notation for multiple compatible modules

---

For detailed information about each library, refer to the individual documentation files in this repository.
