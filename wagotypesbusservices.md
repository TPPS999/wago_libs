# WagoTypesBusServices v2.0.1.2

## Overview
WAGO PLC library providing WagoTypesBusServices functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbTerminalBaseData
**Methods:**

#### Format
#### getOrderNumberAsString
This method returns the order number as string like 0750-0650/0003-0000

#### getOrderNumber
returns an array[0..3] of uint. Each item holds an integer part of the ordernumber.

## Data Types

### eTerminalType
Enumeration type.

### getModuleType
returns the |eModuleType| of a module.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbTerminalBaseData: FbTerminalBaseData;
END_VAR

// Basic function block usage
fbFbTerminalBaseData(
    // Configure inputs as needed
);

// Check status
IF fbFbTerminalBaseData.xValid THEN
    // Operation successful
END_IF

IF fbFbTerminalBaseData.xError THEN
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

