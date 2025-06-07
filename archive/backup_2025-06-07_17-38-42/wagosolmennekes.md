# WagoSolMennekes v1.0.1.0

## Overview
WAGO PLC library providing WagoSolMennekes functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbChargePoint
Compact function block performing a change configuration request

**Description:**
The charge point will answer either with Accepted or Rejected

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbChargePoint: FbChargePoint;
END_VAR

// Basic function block usage
fbFbChargePoint(
    // Configure inputs as needed
);

// Check status
IF fbFbChargePoint.xValid THEN
    // Operation successful
END_IF

IF fbFbChargePoint.xError THEN
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

