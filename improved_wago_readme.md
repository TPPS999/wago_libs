# WAGO PLC Libraries Documentation

> **Comprehensive reference for WAGO PLC libraries with 200+ function blocks, detailed examples, and professional integration patterns for industrial automation applications.**

[![Documentation Status](https://img.shields.io/badge/docs-complete-brightgreen.svg)](https://github.com/TPPS999/wago_libs)
[![Libraries](https://img.shields.io/badge/libraries-200%2B-blue.svg)](#available-libraries)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/TPPS999/wago_libs.git

# Generate merged documentation
python3 html_merger.py /path/to/wago/libs -s WagoAppSunspec
```

**Most Popular Categories:**
- 🏢 [Building Automation](#building-automation--knxeib) - KNX/EIB, BACnet, Room Control
- 🔌 [Communication & Networking](#communication--networking) - Modbus, HTTP, SNMP, Socket
- ⚡ [Hardware Control](#hardware-control--monitoring) - I/O Modules, Power Measurement
- 🏭 [Industrial Protocols](#industrial-protocols--standards) - HART, EnOcean, M-Bus

---

## 📚 Available Libraries

### 🏢 Building Automation & KNX/EIB

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoAppKNX** | Complete KNX/EIB TP1 communication with comprehensive DPT support | [📖 Docs](docs/WagoAppKNX.md) |
| **WagoSysBACnet** | Complete BACnet protocol stack with objects and services | [📖 Docs](docs/WagoSysBACnet.md) |
| **WagoSolRoomApp** | Room automation functions for lighting and HVAC control | [📖 Docs](docs/WagoSolRoomApp.md) |
| **WagoSolWeihenstephan** | Weihenstephan protocol server implementation | [📖 Docs](docs/WagoSolWeihenstephan.md) |
| **WagoTypesBACnet** | BACnet protocol type definitions and object structures | [📖 Docs](docs/WagoTypesBACnet.md) |
| **WagoSysVisuBACnet** | BACnet visualization support | [📖 Docs](docs/WagoSysVisuBACnet.md) |

### 🔌 Communication & Networking

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoAppSocket** | Socket communication (TCP/UDP clients/servers, broadcast, multicast) | [📖 Docs](docs/WagoAppSocket.md) |
| **WagoAppHTTP** | HTTP/HTTPS client functionality for web service integration | [📖 Docs](docs/WagoAppHTTP.md) |
| **WagoAppFTP** | FTP, FTPS, and SFTP client services for file transfer | [📖 Docs](docs/WagoAppFTP.md) |
| **WagoAppSNMP** | SNMP v1/v3 management and trap functionality | [📖 Docs](docs/WagoAppSNMP.md) |
| **WagoAppPlcModbus** | Comprehensive Modbus master/slave implementation | [📖 Docs](docs/WagoAppPlcModbus.md) |
| **WagoAppSunspec** | SunSpec communication library for solar inverters | [📖 Docs](docs/WagoAppSunspec.md) |
| **WagoAppSiemensS7Protocol** | Siemens S7 protocol communication | [📖 Docs](docs/WagoAppSiemensS7Protocol.md) |
| **WagoSysSocket** | Low-level socket operations and BSD socket interface | [📖 Docs](docs/WagoSysSocket.md) |
| **WagoSysBSDSocket** | BSD socket implementation with POSIX-like API | [📖 Docs](docs/WagoSysBSDSocket.md) |
| **WagoSysSSL** | SSL/TLS encryption for secure communications | [📖 Docs](docs/WagoSysSSL.md) |
| **WagoSysCurl** | HTTP client library with cURL functionality | [📖 Docs](docs/WagoSysCurl.md) |
| **WagoSysCloud** | Cloud connectivity and agent communication | [📖 Docs](docs/WagoSysCloud.md) |

### 📡 Serial Communication

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoAppSerial_GENIbus** | GENIbus protocol for GRUNDFOS devices | [📖 Docs](docs/WagoAppSerial_GENIbus.md) |
| **WagoAppSerial_Fitron** | Fitron device communication | [📖 Docs](docs/WagoAppSerial_Fitron.md) |
| **WagoAppSerial_3964R_RK512** | 3964R and RK512 protocols | [📖 Docs](docs/WagoAppSerial_3964R_RK512.md) |
| **WagoAppSerial_Modem** | Modem handling and control | [📖 Docs](docs/WagoAppSerial_Modem.md) |
| **WagoAppSerial_Scanner** | Barcode scanner integration | [📖 Docs](docs/WagoAppSerial_Scanner.md) |
| **WagoAppSerial_Sms** | SMS sending/receiving via GSM modems | [📖 Docs](docs/WagoAppSerial_Sms.md) |
| **WagoAppSerial_NMEA** | NMEA sentence processing for GPS/marine devices | [📖 Docs](docs/WagoAppSerial_NMEA.md) |
| **WagoAppSerial_ebmBus** | ebmBus protocol for motor control | [📖 Docs](docs/WagoAppSerial_ebmBus.md) |
| **WagoAppDLMS** | DLMS communication for smart meters | [📖 Docs](docs/WagoAppDLMS.md) |
| **WagoSysSerial** | Low-level serial communication interface | [📖 Docs](docs/WagoSysSerial.md) |
| **WagoSysModem** | Modem control and AT command interface | [📖 Docs](docs/WagoSysModem.md) |

### 🏭 Industrial Protocols & Standards

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoAppM_Bus** | M-Bus master for utility meter reading | [📖 Docs](docs/WagoAppM_Bus.md) |
| **WagoAppMP_Bus** | MP-Bus for BELIMO HVAC devices | [📖 Docs](docs/WagoAppMP_Bus.md) |
| **WagoAppSMI** | SMI (Standard Motor Interface) for blind/shutter control | [📖 Docs](docs/WagoAppSMI.md) |
| **WagoAppHART** | HART protocol for process automation | [📖 Docs](docs/WagoAppHART.md) |
| **WagoAppEnocean** | EnOcean wireless sensor/actuator communication | [📖 Docs](docs/WagoAppEnocean.md) |
| **WagoSysDps** | PROFIBUS DP slave functionality | [📖 Docs](docs/WagoSysDps.md) |

### 🚗 CANopen & CAN Communication

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysCan** | CAN interface and CANopen stack implementation | [📖 Docs](docs/WagoSysCan.md) |
| **WagoTypesCan** | CAN communication type definitions and enumerations | [📖 Docs](docs/WagoTypesCan.md) |
| **WagoTypesCanExtra** | Extended CAN type definitions | [📖 Docs](docs/WagoTypesCanExtra.md) |

### ⚡ Hardware Control & Monitoring

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoAppPowerMeasurement** | Power measurement modules (750-493/494/495) | [📖 Docs](docs/WagoAppPowerMeasurement.md) |
| **WagoAppPowerSupply** | Power supply module control and monitoring | [📖 Docs](docs/WagoAppPowerSupply.md) |
| **WagoAppStepper** | Stepper motor control (750-670/671/672/673) | [📖 Docs](docs/WagoAppStepper.md) |
| **WagoAppSolenoid** | Proportional valve control (750-632/1632) | [📖 Docs](docs/WagoAppSolenoid.md) |
| **WagoAppFuse** | Electronic fuse management (787-series) | [📖 Docs](docs/WagoAppFuse.md) |
| **WagoAppIOLink** | IO-Link master configuration and device handling | [📖 Docs](docs/WagoAppIOLink.md) |
| **WagoAppVibrationMonitoring** | Vibration monitoring systems | [📖 Docs](docs/WagoAppVibrationMonitoring.md) |
| **WagoAppSafety** | Safety system communication and diagnostics | [📖 Docs](docs/WagoAppSafety.md) |
| **WagoSysEdgeController** | Edge computing functionality | [📖 Docs](docs/WagoSysEdgeController.md) |
| **WagoSysProcessorLoad** | CPU load monitoring and performance analysis | [📖 Docs](docs/WagoSysProcessorLoad.md) |

### 🔌 K-Bus & I/O Module Support

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysKbusServices** | K-Bus terminal services and configuration | [📖 Docs](docs/WagoSysKbusServices.md) |
| **WagoSysKbusTerminalControl** | Terminal control and process data exchange | [📖 Docs](docs/WagoSysKbusTerminalControl.md) |
| **WagoSysKbusAsyncCom** | Asynchronous K-Bus communication | [📖 Docs](docs/WagoSysKbusAsyncCom.md) |
| **WagoSysKbusModule** | Standard K-Bus module function blocks | [📖 Docs](docs/WagoSysKbusModule.md) |
| **WagoSysFieldbusModule** | Fieldbus-connected module support | [📖 Docs](docs/WagoSysFieldbusModule.md) |
| **WagoSysModuleBase** | Base classes for module implementations | [📖 Docs](docs/WagoSysModuleBase.md) |
| **WagoSysDynamicIoMapping** | Dynamic I/O mapping and configuration | [📖 Docs](docs/WagoSysDynamicIoMapping.md) |

### 🌡️ Temperature & Analog Input Modules

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysModule_750_450** | Temperature input module (RTD/TC/Voltage) | [📖 Docs](docs/WagoSysModule_750_450.md) |
| **WagoSysModule_750_451** | Temperature input module (RTD/TC) | [📖 Docs](docs/WagoSysModule_750_451.md) |
| **WagoSysModule_750_463** | Thermocouple input module (2-channel) | [📖 Docs](docs/WagoSysModule_750_463.md) |
| **WagoSysModule_750_464** | Thermocouple input module (4-channel) | [📖 Docs](docs/WagoSysModule_750_464.md) |
| **WagoSysModule_75x_458** | 8-channel analog input | [📖 Docs](docs/WagoSysModule_75x_458.md) |
| **WagoSysModule_75x_461** | Analog input module (single-ended) | [📖 Docs](docs/WagoSysModule_75x_461.md) |
| **WagoSysModule_75x_469** | High-precision analog input (thermocouple) | [📖 Docs](docs/WagoSysModule_75x_469.md) |
| **WagoSysModule_75x_471** | Universal analog input | [📖 Docs](docs/WagoSysModule_75x_471.md) |
| **WagoSysModule_75x_481** | Thermocouple input module | [📖 Docs](docs/WagoSysModule_75x_481.md) |
| **WagoSysModule_75x_486** | 8-channel voltage/current input | [📖 Docs](docs/WagoSysModule_75x_486.md) |
| **WagoSysModule_75x_487** | 8-channel thermocouple input | [📖 Docs](docs/WagoSysModule_75x_487.md) |
| **WagoSysModule_75x_489** | 4-channel current/voltage input | [📖 Docs](docs/WagoSysModule_75x_489.md) |
| **WagoSysModule_75x_496** | 4-channel RTD input | [📖 Docs](docs/WagoSysModule_75x_496.md) |
| **WagoSysModule_75x_497** | 8-channel RTD input | [📖 Docs](docs/WagoSysModule_75x_497.md) |
| **WagoSysModule_75x_498** | RTD/resistance input module | [📖 Docs](docs/WagoSysModule_75x_498.md) |

### 📤 Analog Output Modules

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysModule_75x_562** | 2-channel analog output (voltage/current) | [📖 Docs](docs/WagoSysModule_75x_562.md) |
| **WagoSysModule_75x_563** | 4-channel analog output module | [📖 Docs](docs/WagoSysModule_75x_563.md) |
| **WagoSysModule_75x_564** | 4-channel current output module | [📖 Docs](docs/WagoSysModule_75x_564.md) |
| **WagoSysModule_75x_597** | 8-channel voltage output module | [📖 Docs](docs/WagoSysModule_75x_597.md) |

### 🔌 Digital I/O & Special Function Modules

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysModule_750_630** | RTC module with calendar functions | [📖 Docs](docs/WagoSysModule_750_630.md) |
| **WagoSysModule_750_636** | DeviceNet slave module | [📖 Docs](docs/WagoSysModule_750_636.md) |
| **WagoSysModule_750_642** | Incremental encoder interface | [📖 Docs](docs/WagoSysModule_750_642.md) |
| **WagoSysModule_750_643** | 2-channel encoder interface | [📖 Docs](docs/WagoSysModule_750_643.md) |
| **WagoSysModule_75x_511** | PWM output module | [📖 Docs](docs/WagoSysModule_75x_511.md) |
| **WagoSysModule_75x_632** | Proportional valve output (single channel) | [📖 Docs](docs/WagoSysModule_75x_632.md) |
| **WagoSysModule_75x_633** | Encoder interface module (SSI/incremental) | [📖 Docs](docs/WagoSysModule_75x_633.md) |
| **WagoSysModule_75x_635** | Profibus master module | [📖 Docs](docs/WagoSysModule_75x_635.md) |
| **WagoSysModule_75x_640** | 16-channel relay output | [📖 Docs](docs/WagoSysModule_75x_640.md) |
| **WagoSysModule_75x_644** | 4-channel relay output | [📖 Docs](docs/WagoSysModule_75x_644.md) |
| **WagoSysModule_75x_645** | Digital input/output module | [📖 Docs](docs/WagoSysModule_75x_645.md) |
| **WagoSysModule_75x_655** | DeviceNet master module | [📖 Docs](docs/WagoSysModule_75x_655.md) |
| **WagoSysModule_75x_657** | Ethernet TCP/IP module | [📖 Docs](docs/WagoSysModule_75x_657.md) |
| **WagoSysModule_75x_658** | CAN gateway module | [📖 Docs](docs/WagoSysModule_75x_658.md) |
| **WagoSysModule_75x_677** | Incremental encoder interface (multi-channel) | [📖 Docs](docs/WagoSysModule_75x_677.md) |

### 🏗️ KNX/EIB Communication Modules

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysModule_753_646** | KNX/EIB TP1 master module for building automation | [📖 Docs](docs/WagoSysModule_753_646.md) |
| **WagoSysModule_753_647** | CAN master module (753 series) with DALI functionality | [📖 Docs](docs/WagoSysModule_753_647.md) |
| **WagoSysModule_753_649** | Ethernet switch module (753 series) | [📖 Docs](docs/WagoSysModule_753_649.md) |
| **WagoSysModule_753_163x** | Fieldbus coupler modules | [📖 Docs](docs/WagoSysModule_753_163x.md) |
| **WagoSysModule_753_1646** | Advanced communication module | [📖 Docs](docs/WagoSysModule_753_1646.md) |

### 🔬 Specialized Modules

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysModule_75x_1491** | Strain gauge input module | [📖 Docs](docs/WagoSysModule_75x_1491.md) |
| **WagoSysModule_75x_1632** | Multi-channel proportional valve output | [📖 Docs](docs/WagoSysModule_75x_1632.md) |
| **WagoSysModule_75x_1657** | Ethernet switch module | [📖 Docs](docs/WagoSysModule_75x_1657.md) |

### ☁️ Data Management & Cloud

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoAppInfluxDB** | InfluxDB v1.x/v2.0 time-series database integration | [📖 Docs](docs/WagoAppInfluxDB.md) |
| **WagoAppSQL_MySQL** | MySQL database connectivity | [📖 Docs](docs/WagoAppSQL_MySQL.md) |
| **WagoAppSQL_MsSQL** | Microsoft SQL Server integration | [📖 Docs](docs/WagoAppSQL_MsSQL.md) |
| **WagoAppJSON** | JSON parsing, creation, and manipulation | [📖 Docs](docs/WagoAppJSON.md) |
| **WagoAppSparkplug** | Eclipse Sparkplug MQTT specification | [📖 Docs](docs/WagoAppSparkplug.md) |
| **WagoAppTOPASS** | TO-PASS web service integration | [📖 Docs](docs/WagoAppTOPASS.md) |
| **WagoAppPvForecast** | Photovoltaic forecast data from WAGO Cloud | [📖 Docs](docs/WagoAppPvForecast.md) |
| **WagoSysSQL_SQLite** | SQLite database support | [📖 Docs](docs/WagoSysSQL_SQLite.md) |

### 🛠️ System & Utilities

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoAppTime** | Time/date operations, timezones, elapsed time, timeouts | [📖 Docs](docs/WagoAppTime.md) |
| **WagoAppScheduler** | Time-based scheduling with holiday/special period support | [📖 Docs](docs/WagoAppScheduler.md) |
| **WagoAppEvent** | Event handling and catching system | [📖 Docs](docs/WagoAppEvent.md) |
| **WagoAppMem** | Shared memory management for inter-process communication | [📖 Docs](docs/WagoAppMem.md) |
| **WagoAppFileDir** | File and directory operations | [📖 Docs](docs/WagoAppFileDir.md) |
| **WagoAppMath** | Mathematical functions (exponential, etc.) | [📖 Docs](docs/WagoAppMath.md) |
| **WagoAppString** | String manipulation utilities | [📖 Docs](docs/WagoAppString.md) |
| **WagoAppWString** | Wide string (Unicode) operations | [📖 Docs](docs/WagoAppWString.md) |
| **WagoAppProcessorLoad** | CPU load monitoring | [📖 Docs](docs/WagoAppProcessorLoad.md) |
| **WagoAppRTC** | Real-time clock and GPS-DCF converter support | [📖 Docs](docs/WagoAppRTC.md) |
| **WagoSysTime** | Core time handling and calendar functions | [📖 Docs](docs/WagoSysTime.md) |
| **WagoSysFileDir** | Low-level file and directory operations | [📖 Docs](docs/WagoSysFileDir.md) |
| **WagoSysString** | Core string manipulation functions | [📖 Docs](docs/WagoSysString.md) |
| **WagoSysStandard** | Standard system functions and utilities | [📖 Docs](docs/WagoSysStandard.md) |
| **WagoSysPlainMem** | Plain memory operations and data type conversions | [📖 Docs](docs/WagoSysPlainMem.md) |
| **WagoSysFifo** | FIFO buffer implementation | [📖 Docs](docs/WagoSysFifo.md) |
| **WagoSysLog** | System logging and message handling | [📖 Docs](docs/WagoSysLog.md) |
| **WagoSysErrorBase** | Error handling and result management | [📖 Docs](docs/WagoSysErrorBase.md) |
| **WagoSysAsync** | Asynchronous operation framework | [📖 Docs](docs/WagoSysAsync.md) |

### 💡 Application LED Control

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysAppLED** | Application LED control with patterns and sequences | [📖 Docs](docs/WagoSysAppLED.md) |
| **WagoTypesAppLED** | Application LED control type definitions | [📖 Docs](docs/WagoTypesAppLED.md) |

### 🖥️ Visualization & User Interface

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoVisuIcons** | Standard visualization icons | [📖 Docs](docs/WagoVisuIcons.md) |
| **WagoVisuIconsMaterialDesign** | Material Design icons for visualization | [📖 Docs](docs/WagoVisuIconsMaterialDesign.md) |
| **WagoSysVisuStandard** | Standard visualization components | [📖 Docs](docs/WagoSysVisuStandard.md) |
| **WagoSysVisuTree** | Tree view visualization components | [📖 Docs](docs/WagoSysVisuTree.md) |

### 🔒 Security & DRM

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSysDRM** | Digital Rights Management functionality | [📖 Docs](docs/WagoSysDRM.md) |
| **WagoSysDrmInterface** | DRM interface definitions | [📖 Docs](docs/WagoSysDrmInterface.md) |

### 🏭 Solution-Specific Libraries

| Library | Description | Documentation |
|---------|-------------|---------------|
| **WagoSolOppermann** | Oppermann HVAC sensor integration | [📖 Docs](docs/WagoSolOppermann.md) |
| **WagoSolEAP** | EAP room operating units (RBG1) | [📖 Docs](docs/WagoSolEAP.md) |
| **WagoSolElsner** | Elsner weather station integration | [📖 Docs](docs/WagoSolElsner.md) |
| **WagoSolHKW** | HKW weather forecast stations | [📖 Docs](docs/WagoSolHKW.md) |
| **WagoSolMennekes** | Mennekes charging point control | [📖 Docs](docs/WagoSolMennekes.md) |
| **WagoAppWeatherForecast** | Weather data from multiple providers | [📖 Docs](docs/WagoAppWeatherForecast.md) |
| **WagoAppMail** | SMTP email functionality with attachments | [📖 Docs](docs/WagoAppMail.md) |
| **WagoAppRFIDReader_phg** | PHG RFID reader integration | [📖 Docs](docs/WagoAppRFIDReader_phg.md) |
| **WagoSolThies** | Thies weather station integration | [📖 Docs](docs/WagoSolThies.md) |
| **WagoSolThermokon** | Thermokon room automation devices | [📖 Docs](docs/WagoSolThermokon.md) |
| **WagoSolRomutec** | Romutec LED control and communication | [📖 Docs](docs/WagoSolRomutec.md) |
| **WagoSolSplusS** | S+S Regeltechnik sensor integration | [📖 Docs](docs/WagoSolSplusS.md) |
| **WagoSolSolutionBuilder** | Solution Builder framework components | [📖 Docs](docs/WagoSolSolutionBuilder.md) |

---

## 🚀 Key Features

### 💼 Professional Integration
- ✅ Comprehensive error handling and status reporting
- ✅ Standardized interfaces across all libraries
- ✅ Extensive documentation with usage examples
- ✅ Compatible with WAGO PLC hardware ecosystem

### 🌐 Communication Excellence
- 📡 Multiple protocol support (Modbus, BACnet, HART, EnOcean, KNX/EIB)
- 🔗 Network communication (TCP/UDP, HTTP/HTTPS, FTP/SFTP)
- 📞 Serial communication with various protocols
- 🔒 SSL/TLS encryption support

### 🏢 Building Automation Excellence
- 🏠 **KNX/EIB TP1** - Complete building automation protocol support
- 📊 **Comprehensive DPT Library** - All standard KNX data point types
- 🌡️ **HVAC Control** - Temperature, humidity, air quality monitoring
- 💡 **Lighting Control** - Switching, dimming, scene management
- ⚡ **Energy Management** - Power measurement and monitoring
- 📅 **Time Scheduling** - Calendar and timer functions
- 🚨 **Safety Integration** - Window/door sensors, occupancy detection

### 🏭 Industrial Standards
- ⚙️ Support for major automation protocols
- 📈 Energy management and monitoring
- 🛡️ Safety and diagnostics integration
- ⚡ Real-time data processing capabilities

### 🔧 Hardware Integration
- 🔌 Comprehensive K-Bus module support
- 🗺️ Dynamic I/O mapping capabilities
- 🧩 Module-specific function blocks
- 🌐 Fieldbus connectivity
- 🖥️ Edge computing functionality

---

## 📖 Documentation Structure

Each library documentation includes:

- **📋 Overview** - Library purpose and key features
- **🔧 Core Function Blocks** - Detailed FB descriptions with parameters
- **📝 Data Types** - Enumerations and structures
- **💡 Usage Examples** - Practical implementation samples
- **✅ Best Practices** - Error handling and performance guidelines
- **⚠️ Important Notes** - Hardware compatibility and limitations

---

## 🛠️ Getting Started

1. **🎯 Select Library** - Choose the appropriate library for your application needs
2. **📚 Review Documentation** - Study the function blocks and their capabilities
3. **💻 Study Examples** - Understand implementation through practical samples
4. **✅ Follow Best Practices** - Implement proper error handling and performance optimization
5. **🧪 Test Thoroughly** - Validate in your specific environment

---

## 💡 Best Practices

### ⚠️ Error Handling
```iec
IF fbInstance.xError THEN
    CASE fbInstance.eStatus OF
        // Handle specific error codes
    END_CASE
END_IF
```

### 🎯 Performance Considerations
- ⏱️ Use appropriate polling intervals
- 🛡️ Handle communication errors gracefully
- ⏳ Consider device response times
- 📡 Implement proper telegram throttling for KNX
- 🧪 Test thoroughly in target environment

---

## ⚠️ Important Notes

- 📄 Documentation automatically generated from XML specifications
- 📖 Always refer to official WAGO documentation for complete details
- 🧪 Test thoroughly in your specific application environment
- 🔧 Check library compatibility with your PLC hardware
- 📦 Version requirements may vary between libraries
- 🏗️ KNX/EIB requires proper ETS configuration and group address assignment

---

## 🔧 Hardware Compatibility

These libraries are designed for WAGO PLC systems and require:

- ✅ Compatible WAGO controller (750/752/753 series)
- 🔌 Appropriate I/O modules for specific applications
- 🌐 Proper network and serial interface configuration
- 📡 Required communication modules for protocol-specific libraries
- 🏗️ KNX/EIB TP1 interface module (753-646) for building automation

### 📟 Supported Module Series

| Series | Description | Applications |
|--------|-------------|--------------|
| **750 Series** | Standard I/O modules with K-Bus interface | General purpose I/O, analog/digital |
| **752 Series** | Advanced controller modules | Edge computing, advanced control |
| **753 Series** | Fieldbus coupler and gateway modules | KNX/EIB, Profibus, CAN communication |
| **75x Series** | Generic notation for multiple compatible modules | Cross-platform compatibility |

### 🏗️ KNX/EIB Specific Requirements

| Component | Description | Purpose |
|-----------|-------------|---------|
| **753-646** | KNX/EIB TP1 master module | Building automation communication |
| **ETS Software** | Engineering Tool Software | KNX device configuration and group addressing |
| **KNX Certification** | Device compliance verification | Ensure standard compatibility |
| **Proper Wiring** | TP1 bus topology with termination | Reliable communication |

---

## 🛠️ Tools & Utilities

### 📄 HTML Documentation Merger
```bash
# Merge single library documentation
python3 html_merger.py /path/to/wago/libs -s WagoAppKNX -o output/

# Features:
# ✅ No external dependencies (pure Python)
# ✅ Preserves WAGO formatting
# ✅ Embedded CSS and images
# ✅ Single-file output for easy sharing
```

### 🔍 Library Search & Navigation
- 🏷️ **Category-based organization** - Find libraries by application domain
- 🔗 **Direct documentation links** - Quick access to detailed docs
- 📊 **Comprehensive coverage** - 200+ libraries documented
- 🎯 **Cross-reference support** - Related libraries and dependencies

---

## 🤝 Contributing

We welcome contributions to improve this documentation:

1. **🐛 Report Issues** - Found incorrect information or broken links?
2. **📝 Improve Documentation** - Add examples, clarify descriptions
3. **🔄 Update Libraries** - Keep pace with WAGO releases
4. **🧪 Share Examples** - Real-world implementation patterns

### 📋 Contribution Guidelines
- Follow existing documentation structure
- Include practical examples where possible
- Test all code examples before submission
- Reference official WAGO documentation

---

## 📞 Support & Resources

### 🔗 Official WAGO Resources
- 🌐 **WAGO Website** - [wago.com](https://www.wago.com)
- 📚 **Official Documentation** - WAGO Software Documentation
- 🎓 **Training Materials** - WAGO Academy courses
- 🛠️ **Technical Support** - Official WAGO support channels

### 👥 Community Resources
- 💬 **GitHub Discussions** - Ask questions and share experiences
- 🐛 **Issue Tracker** - Report bugs and request features
- 📖 **Wiki Pages** - Additional tutorials and guides
- 🌟 **Examples Repository** - Real-world implementation examples

---

## 📜 License

This documentation is provided under the MIT License. See [LICENSE](LICENSE) file for details.

---

## 🏆 Acknowledgments

- 🙏 **WAGO Kontakttechnik GmbH** - For creating these comprehensive libraries
- 👥 **WAGO Community** - For feedback and contributions
- 🔧 **Industrial Automation Engineers** - For real-world testing and validation

---

**⭐ Star this repository if you find it useful!**

For detailed information about each library, refer to the individual documentation files linked in the tables above.