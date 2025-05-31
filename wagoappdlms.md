# WagoAppDLMS v1.0.0.3

## Overview
DLMS (Device Language Message Specification) library for intelligent power meter communication.

**Key Features:**
- Serial communication with smart meters
- OBIS (Object Identification System) code support
- Single and multiple data record reading
- Authentication support
- Compact interface for graphical languages

## Compact Function Blocks

### FbMultipleData_cpt
This is a serial communication FB with *compact*-type interface for use with intelligent power meters in graphical languages. It is used to read the standard output data from the meter.

**Description:**
This Fb implements the whole communication for reading the standard value list with code and value.

### FbSingleData_cpt
This is a serial communication FB with *compact*-type interface for use with intelligent power meters in graphical languages. It is used to read a single data record from the meter.

**Description:**
This Fb implements the whole communication for reading a single OBIS-Datarecord with code and value.

## Data Types

### eStatus
Enumeration type.

This is a data type for the possible errors of the DLMS - Library.

## Usage Examples

### DLMS Meter Reading
```iec
VAR
    fbSingle: FbSingleData_cpt;
    obis_code: typOBIS;
    data_record: typDataRecord;
    execute: BOOL;
END_VAR

// Read total active energy import
obis_code.bA := 1;  obis_code.bB := 0;  obis_code.bC := 1;
obis_code.bD := 8;  obis_code.bE := 0;  obis_code.bF := 255;

fbSingle(
    xExecute := execute,
    sInterface := 'COM1',
    typOBIS := obis_code,
    eAuthLevel := NO_AUTH,
    sPassword := '',
    typDataRecord => data_record
);

IF fbSingle.xDone AND NOT fbSingle.xError THEN
    energy_total := data_record.fValue;
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

