# WagoAppDMX v1.0.1.2

## Overview
WAGO PLC library providing WagoAppDMX functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbDmxSlave
The FbDmxSlave function block serves to receive values from a DMX line. Communication takes place via an RS-485 interface module (750-652). This function block may be used only once per installed serial I/O module. .. note:: The DMX function is only possible using WAGO 750-652 Serial Module from firmware version (06). Maximum 21 DMX value can be read. .. note:: The starting channel ``uiStartChannel`` must be similar with the configuration of the serial I/O module. The serial I/O module can be configured with WAGO-I/O-CHECK. Including the starting channel number, up to 21 consecutive channels can be read.

**Description:**
``bPortDmx`` must be connect to the other functions. ``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.RS232_485_Interface`` The input ``iStartChannel`` specifies the first read DMX channel. This starting channel must be similar with the configuration of the serial I/O module. The serial I/O module can be configured with WAGO-I/O-CHECK. Including the starting channel number, up to 21 consecutive channels can be read. The DMX values are read out starting from the start index specified at the ``iStartChannel`` input. Please note that the value at the ``iStartChannel`` input does not lead to configuration of the start channel number of the serial I/O module. The start channel number must be executed with WAGO-I/O-CHECK.

### FbDmxMaster
The FbDmxMaster function block transmits values to a DMX line. Communication takes place via an RS-485 interface module (750-652). This function block may be used only once per installed serial I/O module. .. note:: The DMX function is only possible using WAGO 750-652 Serial Module from firmware version 03. For FW 03 until FW05, maximum 21 or 45 DMX channel can be sent depends on the Process Image setting of the module. From FW 06 maximum 512 DMX channel can be sent.

**Description:**
``bPortDmx`` must be connect to the other functions. ``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.RS232_485_Interface`` The maximum number of channels to be transmitted can be limited at the ``iNumberOfChannel`` input. The ``xBlackOut`` input activates the Shutdown mode. - ``xBlackOut``

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbDmxSlave: FbDmxSlave;
END_VAR

// Basic function block usage
fbFbDmxSlave(
    // Configure inputs as needed
);

// Check status
IF fbFbDmxSlave.xValid THEN
    // Operation successful
END_IF

IF fbFbDmxSlave.xError THEN
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

