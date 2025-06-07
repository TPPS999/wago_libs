# WagoSolEAP v1.0.0.4

## Overview
WAGO PLC library providing WagoSolEAP functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbRBG1
Function block to communicate with a EAP-RBG1 room operating unit.

**Description:**
Function block to communicate with a EAP-RBG1 slave. For each slave one of those funktion block is needed. The FbRBG1 reads the data from the EAP room control device. A continuous TRUE signal at the ``xEnable`` input activates the readout process, and a FALSE signal deactivates it. If the input is not enabled, the output process starts automatically. The function block is synchronized with the communication module (FbEAP_MasterRTU) via the ``bPortEAP`` input. The device address is specified at the ``bSlaveAddress`` input. By assigning different addresses, you can address multiple devices via one serial I/O module. This input is assigned ``1`` by default. ``dtActualTime`` is used for displaying the date and time on the RBG1. Displaying the current fan stage requires writing to ``bActualValueFan.`` If the inputs ``xSetSetpointFan_In`` and ``xSetSetpointTemp_In`` are TRUE, the setpoint values ``rSetpointFan_In`` and ``rSetpointTemp_In`` will override the setpoint values ``rSetpointFan_Out`` and ``rSetpointTemp_ Out`` on the RBG1. For example to reset the setpoint to a basic setting. Each of the ``typMessage1`` and ``typMessage2`` structures can be used to display its own text (24 characters) with a freely selectable background color on the RBG1. ``eSymbol`` can be used to display specify a symbol that indicates the current room status. The RBG1 configuration is stored in the ``typConfigRBG1`` structure and should therefore be declared RETAIN PERSISTENT in the program. To identify an error, the current error code is displayed at the output ``eMB_Error``. The ``enumMBerror`` enumeration is found in Modb_I05.lib. The current room temperature and humidity values are output on the ``rRoomTemperature`` and ``rRoomHumidity`` outputs. The setpoints for the target temperature and target fan stage that were set via the RBG1 are output on the ``rSetpointTemp_Out`` and ``rSetpointFan_Out`` outputs. ``xButton1`` – ``xButton8`` indicate whether a button is pressed on the RBG1. ``typDeviceInfoRBG1`` outputs the current version information of the RBG1.

### FbEAP_MasterRTU
The function block is used to communicate with RBG1-ROUs via a RS-485 interface (750-652) by using MODBUS communication. .. note:: It is recommended to use maximal 8 EAP units on each serial interface and Master. .. note:: You should always call this FB cyclic.

**Description:**
``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.RS232_485_Interface`` ``bPortEAP`` must be connect to the other function blocks.

## Data Types

### typStandbyConfigRBG1
Structure type.

### typSliderConfigRBG1
Structure type.

### eSymbolRBG1
Enumeration type.

### eSliderConfigRBG1
Enumeration type.

### typEAP_MasterRTU
Structure type.

### typSetDisplayRBG1
Structure type.

### eColorRBG1
Enumeration type.

### typMessageRBG1
Structure type.

### typDeviceInfoRBG1
Structure type.

### typConfigRBG1
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbRBG1: FbRBG1;
END_VAR

// Basic function block usage
fbFbRBG1(
    // Configure inputs as needed
);

// Check status
IF fbFbRBG1.xValid THEN
    // Operation successful
END_IF

IF fbFbRBG1.xError THEN
    // Handle error
END_IF
```

## Best Practices

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

## Important Notes

- This documentation was automatically generated from XML specification
- Always refer to official WAGO documentation for complete details
- Test thoroughly in your specific application environment
- Check library compatibility with your PLC hardware

