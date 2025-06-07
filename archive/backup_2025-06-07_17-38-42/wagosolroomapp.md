# WagoSolRoomApp v1.1.1.1

## Overview
WAGO PLC library providing WagoSolRoomApp functionality.

**Key Features:**
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbLightingControlSegmentsMultiSensor
Function block can be used for segment control or partition wall control of the lighting multisensor values for 24 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813:

### FbLightingControlSegments
Function block can be used for segment control or partition wall control of the lighting button signals for 24 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813:

### FbDaliConstantLightControlAndSwitch
This function block combines the function blocks FbDaliConstantLightControl and FbDALIDimDoubleButton from WagoAppDALI.

**Description:**
The function blocks either uses the FbDALIConstantLightControl or FbDALIDimDoubleButton, depending on the availability of a multisensor in the segment. If there is a TRUE signal at ``xMultiSensorAvailable``, the function block uses the FbDALIConstantLightControl. Otherwise, it will use the FbDALIDoubleButton. That is needed, because the FbDALIConstantLightControl needs the sensor values. If there are no sensor values (because of the absence of multisensors), the function block can not work correctly in some cases. To feel no difference between the use of FbDALIConstantLightControl or FbDALIDimDoubleButton, the configuration of the FBs is synchronized. So the user just configurate both FBs with ``typConfigParameters``.

### FbDaliAddressingMultiSensors
This function block is used primarily for the addressing of the DALI multisensors. Additionally it has more functionalities like locating DALI multisensors.

### FbHVAC_ControlSegments
Function block can be used for segment control or partition wall control of the HVAC for 24 segments. Segment control is used to evaluate partition wall information and to transfer set value information to the segments.

**Description:**
The function block corresponds to a Room Automation macro (RA-Macro) with the following function(s) from the VDI 3813:

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbLightingControlSegmentsMultiSensor: FbLightingControlSegmentsMultiSensor;
END_VAR

// Basic function block usage
fbFbLightingControlSegmentsMultiSensor(
    // Configure inputs as needed
);

// Check status
IF fbFbLightingControlSegmentsMultiSensor.xValid THEN
    // Operation successful
END_IF

IF fbFbLightingControlSegmentsMultiSensor.xError THEN
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

