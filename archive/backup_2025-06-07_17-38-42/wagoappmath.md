# WagoAppMath v1.1.1.3

## Overview
WAGO PLC library providing WagoAppMath functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Data Types

### exp_r
Enumeration type.

The function value of the exponential function of x (REAL). If the value of the result exceeds the range of the return type, 'cINFTY' is returned.

### exp_L
Enumeration type.

The function value of the exponential function of x (LREAL). If the value of the result exceeds the range of the return type, 'cINFTY' is returned.

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

