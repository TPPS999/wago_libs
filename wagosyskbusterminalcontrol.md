# WagoSysKbusTerminalControl v2.2.2.2

## Overview
WAGO PLC library providing WagoSysKbusTerminalControl functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbGetKbusDrvRef
### FbSetTerminalRef
**Methods:**

#### AllocateProcessData_SD
#### FreeProcessData
#### AllocateProcessData_PS
#### Stop_PDE
#### Start_PDE_In_CurrentTask
### FbGetTerminalRef
**Methods:**

#### FreeProcessData
#### AllocateProcessData
#### ManualInitialize
## Data Types

### ePARTICULAR_CODES
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbGetKbusDrvRef: FbGetKbusDrvRef;
END_VAR

// Basic function block usage
fbFbGetKbusDrvRef(
    // Configure inputs as needed
);

// Check status
IF fbFbGetKbusDrvRef.xValid THEN
    // Operation successful
END_IF

IF fbFbGetKbusDrvRef.xError THEN
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

