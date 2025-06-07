# WagoSolThies v1.0.2.4

## Overview
WAGO PLC library providing WagoSolThies functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbThiesWeatherstationCompactWSC11
The function block reads the measured values from the Thies Compact WSC11 weather station and presents them as a structure. .. note:: You should always call this FB cyclic.

### FbThiesPyranometerGSM
The function block reads the measured values from the Thies Pyranometer GSM 10.7 weather station and presents them as a structure. .. note:: You should always call this FB cyclic.

### FbThiesClimaSensorUS
The function block reads the measured values from the Thies Clima Sensor US weather station and presents them as a structure. .. note:: You should always call this FB cyclic.

**Description:**
Type of Precipitation for Clima Sensor US:

### FbThiesMaster
The function block is used for Thies wheather sensors communication via serial interface using MODBUS communication. .. note:: You should always call this FB cyclic.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbThiesWeatherstationCompactWSC11: FbThiesWeatherstationCompactWSC11;
END_VAR

// Basic function block usage
fbFbThiesWeatherstationCompactWSC11(
    // Configure inputs as needed
);

// Check status
IF fbFbThiesWeatherstationCompactWSC11.xValid THEN
    // Operation successful
END_IF

IF fbFbThiesWeatherstationCompactWSC11.xError THEN
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

