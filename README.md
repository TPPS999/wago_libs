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

### BACnet & Building Automation

- **WagoSysBACnet** - Complete BACnet protocol stack with objects and services
- **WagoSolRoomApp** - Room automation functions for lighting and HVAC control
- **WagoSolWeihenstephan** - Weihenstephan protocol server implementation

### Industrial Protocols & Standards

- **WagoAppM_Bus** - M-Bus master for utility meter reading
- **WagoAppMP_Bus** - MP-Bus for BELIMO HVAC devices
- **WagoAppSMI** - SMI (Standard Motor Interface) for blind/shutter control
- **WagoAppHART** - HART protocol for process automation
- **WagoAppEnocean** - EnOcean wireless sensor/actuator communication
- **WagoSysDps** - PROFIBUS DP slave functionality

### CANopen & CAN Communication

- **WagoSysCan** - CAN interface and CANopen stack implementation

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

### K-Bus & I/O Module Support

- **WagoSysKbusServices** - K-Bus terminal services and configuration
- **WagoSysKbusTerminalControl** - Terminal control and process data exchange
- **WagoSysKbusAsyncCom** - Asynchronous K-Bus communication
- **WagoSysKbusModule** - Standard K-Bus module function blocks
- **WagoSysFieldbusModule** - Fieldbus-connected module support
- **WagoSysModuleBase** - Base classes for module implementations
- **WagoSysDynamicIoMapping** - Dynamic I/O mapping and configuration

### Module-Specific Libraries

- **WagoSysModule_750_451** - Temperature input module (RTD/TC)
- **WagoSysModule_750_630** - RTC module with calendar functions
- **WagoSysModule_75x_658** - CAN gateway module
- **WagoSysModule_75x_632** - Proportional valve output
- **WagoSysModule_75x_461** - Analog input module
- **WagoSysModule_75x_481** - Thermocouple input module
- **WagoSysModule_75x_471** - Universal analog input
- **WagoSysModule_75x_469** - High-precision analog input
- **WagoSysModule_75x_458** - 8-channel analog input
- **WagoSysModule_75x_497** - 8-channel RTD input
- **WagoSysModule_75x_496** - 4-channel RTD input
- **WagoSysModule_75x_511** - PWM output module
- **WagoSysModule_75x_563** - Analog output module
- **WagoSysModule_75x_564** - Current output module
- **WagoSysModule_75x_597** - Voltage output module
- **WagoSysModule_75x_633** - Encoder interface module
- **WagoSysModule_75x_645** - Digital input/output
- **WagoSysModule_75x_655** - DeviceNet master module
- **WagoSysModule_75x_657** - Ethernet TCP/IP module
- **WagoSysModule_75x_677** - Incremental encoder interface

### Data Management & Cloud

- **WagoAppInfluxDB** - InfluxDB v1.x/v2.0 time-series database integration
- **WagoAppSQL_MySQL** - MySQL database connectivity
- **WagoAppSQL_MsSQL** - Microsoft SQL Server integration
- **WagoAppJSON** - JSON parsing, creation, and manipulation
- **WagoAppSparkplug** - Eclipse Sparkplug MQTT specification
- **WagoAppTOPASS** - TO-PASS web service integration
- **WagoAppPvForecast** - Photovoltaic forecast data from WAGO Cloud
- **WagoSysSQL_SQLite** - SQLite database support

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

### Application LED Control

- **WagoSysAppLED** - Application LED control with patterns and sequences

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

- Compatible WAGO controller (750/752 series)
- Appropriate I/O modules for specific applications
- Proper network and serial interface configuration
- Required communication modules for protocol-specific libraries

---

For detailed information about each library, refer to the individual documentation files in this repository.
