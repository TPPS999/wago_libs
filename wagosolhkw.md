# WagoSolHKW v1.0.1.1

## Overview
WAGO PLC library providing WagoSolHKW functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbHKW_WeatherStationCompact
The function block is used for using a HKW weather forecast station WS-K xx via serial interface using MODBUS communication.

### FbHKW_SearchCityID
This functionblock searches cities at global city buffer. Letters which are defined at input ``sSearchCity`` have to be equal to first letters of searched city. The result is copied to output structure``typHKW_City``. If there is no result, a warning occurs at the ``sStatus`` output.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbHKW_WeatherStationCompact: FbHKW_WeatherStationCompact;
END_VAR

// Basic function block usage
fbFbHKW_WeatherStationCompact(
    // Configure inputs as needed
);

// Check status
IF fbFbHKW_WeatherStationCompact.xValid THEN
    // Operation successful
END_IF

IF fbFbHKW_WeatherStationCompact.xError THEN
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

