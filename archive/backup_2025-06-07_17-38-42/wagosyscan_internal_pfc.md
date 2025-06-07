# WagoSysCan_Internal_PFC v1.0.1.6

## Overview
WAGO PLC library providing WagoSysCan_Internal_PFC functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbCanOpenInterface
**Methods:**

#### GetTimestamp
#### SdoWriteSync
#### SdoWriteData
#### SdoWriteAsync
#### SdoReadSync
#### SdoReadData
#### SdoReadAsync
read CANopen SDOs without blocking process =========== ================================== Returnvalue Description ----------- ---------------------------------- < 0 // Error Codes from eCanFnReturn 0..udiBytes // call finished / bytes received > 16#10000 // SDO abort code =========== ==================================

#### SdoAdd
#### GuardErrorNode
#### GuardError
#### SendTimestamp
#### ChangeState
#### GetEmcy
#### GetNodeId
#### GetNodeEmcy
#### GetLastNode
#### SendEmcy
#### GetNodeDiag
### FbCanInterface
**Methods:**

#### RegisterAll
#### RegisterId
#### SetDeviceInfo
#### GetDeviceInfo
#### CloseLayer2
#### OpenLayer2
#### GetFrame
#### SendFrame
#### SetCanLed
#### ResetLayer2
#### GetFrameCounter
#### GetBusInfo
#### GetCanMode
#### LibVersion
#### GetFrameBuffer
## Usage Examples

### Basic Usage
```iec
VAR
    fbFbCanOpenInterface: FbCanOpenInterface;
END_VAR

// Basic function block usage
fbFbCanOpenInterface(
    // Configure inputs as needed
);

// Check status
IF fbFbCanOpenInterface.xValid THEN
    // Operation successful
END_IF

IF fbFbCanOpenInterface.xError THEN
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

