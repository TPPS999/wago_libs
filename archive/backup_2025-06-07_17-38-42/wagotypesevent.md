# WagoTypesEvent v1.5.2.1

## Overview
WAGO PLC library providing WagoTypesEvent functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Data Types

### typWagoParam_15_CmpAppOEMServiceTag
Structure type.

### typWagoParam_04_CmpAppDenyStop
Structure type.

### typWagoParam_03_CmpAppDenyStart
Structure type.

### typWagoParam_06_CmpAppNameDenyLoadBootproject
Structure type.

### typWagoParam_13_CmpAppDeny
Structure type.

### eWagoEventStopReason
Enumeration type.

### eWagoEventParameterID
Enumeration type.

### eWagoEventID
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

