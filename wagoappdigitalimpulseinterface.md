# WagoAppDigitalImpulseInterface v1.7.1.0

## Overview
WAGO PLC library providing WagoAppDigitalImpulseInterface functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbMainDriver
Reading the actual position from a sensor

**Description:**
This function block allows to read the position from up to 4 magnets mounted on a transonar sensor. Setting the ultrasonic speed as well as the number of mounted magnets is mandatory und must be done each time by power up.

## Data Types

### eStatus
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbMainDriver: FbMainDriver;
END_VAR

// Basic function block usage
fbFbMainDriver(
    // Configure inputs as needed
);

// Check status
IF fbFbMainDriver.xValid THEN
    // Operation successful
END_IF

IF fbFbMainDriver.xError THEN
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

