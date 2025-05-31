# WagoTypesCan v1.0.2.1

## Overview
WAGO PLC library providing WagoTypesCan functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Data Types

### eCanFnReturn
Enumeration type.

### eCanOpenState
Enumeration type.

### eCanFlagRegister
Enumeration type.

### eCanFlagReset
Enumeration type.

### eCanDeviceError
Enumeration type.

### typCanDeviceInfo
Structure type.

### typCanBusInfo
Structure type.

### eCanMode
Enumeration type.

### eCanInternalState
Enumeration type.

### eCanLedMode
Enumeration type.

## Usage Examples

```iec
// Basic usage example
// Refer to function block documentation for specific usage
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

