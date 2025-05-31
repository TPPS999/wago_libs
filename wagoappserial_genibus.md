# WagoAppSerial_GENIbus v1.0.1.3

## Overview
WAGO PLC library providing WagoAppSerial_GENIbus functionality.

**Key Features:**
- Communication protocols
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbGENIbusMagna3_Pump
The FbGENIbusMagna3_Pump function block is used for controlling the GRUNDFOS MAGNA3 circulation pumps via the RS-485 interface (750-652) using the GENIbus protocol. According to the assigned GENIbus ID ``bPortGENIbus``the control commands and the responses are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note:: You should always call this FB cyclic.

### FbGENIbusMagna3_HeatEnergy
The function block Fb_Magna3_HeatEnergy is used to read data provided by heat energy meter. According to the assigned GENIbus ID ``bPortGENIbus``the control commands and the responses are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note:: You should always call this FB cyclic.

### FbGENIbusMagna_Pump
The FbGENIbusMagna_Pump function block is used for controlling the GRUNDFOS MAGNA circulation pumps via the RS-485 interface (750-652) using the GENIbus protocol. According to the assigned GENIbus ID ``bPortGENIbus``the control commands and the responses are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note:: You should always call this FB cyclic.

### FbGenibusMaster
The FbGenibusMaster function block is used for communication via the RS-485 moduel 750-652 with the GENIbus protocol. This function block detects all queued commands of the other function blocks which belogs to the same GENIbus port ``bPortGENIbus`` and initiates their execution. .. note:: You should always call this FB cyclic.

### FbGENIbusUnitRequest
### FbGENIbusSingleUnitRequest_CL2
Function: This function block can be used to read unit info from Class 2 data point via GENIbus According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

### FbGENIbusSingleUnitRequest_CL14
Function: This function block can be used to read unit info from Class 14 data point via GENIbus According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

### FbGENIbusDataRequest
### FbGENIbusMagna3_DataRequest
### FbGENIbusSet_ReferenceValue
The FbGENIbusSet_ReferenceValue function block executes GENIbus SET operations for data class 5. This data class is used for setting reference variables. According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

### FbGENIbusGet_ReferenceValue
The FbGENIbusGet_ReferenceValue function block executes GENIbus GET operations for data class 5. This data class is used for reading reference variables. According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

### FbGENIbusGet_MeasuredData_32Bit
The FbGENIbusGet_MeasuredData_32Bit function block executes GENIbus GET operations for data class 14. This data class is used for reading measured data 32Bit format. According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

### FbGENIbusGet_MeasuredData
The FbGeni_Get_MeasuredData function block executes GENIbus GET operations for data class 2. This data class is used for reading measured data. According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

### FbGENIbusGet_ConfigValue
The FbGENIbusGet_ConfigValue function block executes GENIbus GET operations of data class 4. This data class is used for reading configuration values. According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

### FbGENIbusMagna3_UnitRequest
### FbGENIbusSet_ConfigValue
The FbGENIbusSet_ConfigValue function block executes GENIbus SET operations of data class 4. This data class is used for setting configuration values. According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

### FbGENIbusSet_Command
The FbGENIbusSet_Command function block executes GENIbus SET operations of data class 3. This data class is used for writing GENIbus commands. According to the assigned GENIbus ID ``bPortGENIbus``the control commands are connected to the FbGENIbusMaster with same GENIbus ID assignment. .. note::You should always call this FB cyclic.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbGENIbusMagna3_Pump: FbGENIbusMagna3_Pump;
END_VAR

// Basic function block usage
fbFbGENIbusMagna3_Pump(
    // Configure inputs as needed
);

// Check status
IF fbFbGENIbusMagna3_Pump.xValid THEN
    // Operation successful
END_IF

IF fbFbGENIbusMagna3_Pump.xError THEN
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

