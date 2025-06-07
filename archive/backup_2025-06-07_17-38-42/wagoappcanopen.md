# WagoAppCanOpen v1.6.1.4

## Overview
WAGO PLC library providing WagoAppCanOpen functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbCanOpenDiag
This function block collects the diagnostic information of a node an prepares strings for diagnostic outputs.

**Description:**
.. note:: This function block is not supported by module 750-658 and Layer2 device

### FbCanOpenGuardErrorDev
This function block tests for a guarding or a heartbeat control error of a configured device.

**Description:**
.. note:: This function block is only supported by onboard CAN interface in master mode

### FbCanOpenGuardError
This function block tests for node guarding or a heartbeat control error on any configured device.

**Description:**
.. note:: This function block is only supported by onboard CAN interface in master mode

### FbCanOpenSdoWrite4
This function block writes a SDO object with up to 4 bytes

**Description:**
Supported by onboard Can interface in master and slave mode as well as by module 750-658 .. note:: If used with module 750-658, function block FbCanL2Open from WagoAppCanLayer2 must be activated first Input ``bChannel`` without use for module 750-658

### FbCanOpenSdoWrite
This function block writes a SDO object with up to 246 bytes

**Description:**
.. note:: This function block is not supported by module 750-658 and Layer2 device

### FbCanOpenSdoRead4
This function block reads a SDO object with up to 4 bytes

**Description:**
Supported by onboard Can interface in master and slave mode as well as by module 750-658 .. note:: If used with module 750-658, function block FbCanL2Open from WagoAppCanLayer2 must be activated first Input ``bChannel`` without use for module 750-658

### FbCanOpenRecvEmcyDev
This function block receives emergency object from a special slave

**Description:**
Supported by onboard CAN interface in master mode and by module 750-658 .. note:: If used with module 750-658, function block FbCanL2Open from WagoAppCanLayer2 must be activated first

### FbCanOpenSdoRead
This function block reads a SDO object with up to 246 bytes

**Description:**
.. note:: This function block is not supported by module 750-658 and Layer2 device

### FbCanOpenRecvEmcy
This function block receives emergency object from any device

**Description:**
.. note:: This function block is only supported by onboard CAN interface in master mode

### FbCanOpenGetKernelState
This function block returns the actual state of the CANopen stack

**Description:**
.. note:: This function block is not supported by module 750-658 and Layer2 device

### FbCanOpenGetLocalNodeId
This function block returns the own node ID

**Description:**
.. note:: This function block is not supported by module 750-658 and Layer2 device

### FbCanOpenSendNmt
This function block sends a NMT command

**Description:**
Supported by onboard CAN interface in master and slave mode as well as by module 750-658 .. note:: If used with module 750-658, function block FbCanL2Open from WagoAppCanLayer2 must be activated first .. note:: In slave mode only own node device id can be used

### FbCanOpenGetState
This function block returns the current state of a device

**Description:**
.. note:: This function block is not supported by module 750-658 and Layer2 device

## Data Types

### typCanOpenEmcyError
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbCanOpenDiag: FbCanOpenDiag;
END_VAR

// Basic function block usage
fbFbCanOpenDiag(
    // Configure inputs as needed
);

// Check status
IF fbFbCanOpenDiag.xValid THEN
    // Operation successful
END_IF

IF fbFbCanOpenDiag.xError THEN
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

