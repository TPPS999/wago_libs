# WagoAppPvForecast v1.0.0.1

## Overview
WAGO PLC library providing WagoAppPvForecast functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbReceiveForecast
This function block receives the forecast data from the Wago Cloud for each PV system as an array element.

**Description:**
The function block has no inputs and receives the forecast data as an array from the Wago Cloud. The maximum number of supported PV system is defined by the parameter MAX_PV_SYSTEMS. After a specific period of time, the forecast data expires and is deleted from the list. The number of days before expiration can be set in the parameter list with the variable EXPIRY_DAYS.

### FbDiagram
This function block converts the incoming forecast data and generates the output for the diagram in the visualization.

**Description:**
The received forecast data from FbReceiveForecast is taken as Input. The whole function block can then be passed to the visualization frame of the diagram. The visualization is only updated when there is a change in the incoming forecast data. Once a day the x-axis is updated with the correct date. {attribute 'hide_all_locals'}

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbReceiveForecast: FbReceiveForecast;
END_VAR

// Basic function block usage
fbFbReceiveForecast(
    // Configure inputs as needed
);

// Check status
IF fbFbReceiveForecast.xValid THEN
    // Operation successful
END_IF

IF fbFbReceiveForecast.xError THEN
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

