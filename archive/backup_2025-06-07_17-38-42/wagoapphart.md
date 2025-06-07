# WagoAppHART v1.7.2.4

## Overview
WAGO PLC library providing WagoAppHART functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbHART_CMD9
Read current and percent of range

**Description:**
HART command 9 The function block sends the HART command 9 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD0
Read unique identifier

**Description:**
HART command 0 The function block sends the HART command 0 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_Current
Calculating current from raw process value

**Description:**
Scaling according to: 0

### FbHART_FDT
This function block works as a gateway beetween a Wago controller and a HART-FDT-DTM framework.

**Description:**
If the block is enabled,its waiting for DPV1-requests. An appropriate DPV1-response will be performed. Up to 64 moduls will be supported (the largest slot is 64)

### FbHART_CMD46
Trim primary variable current DAC gain

**Description:**
HART command 46 The function block sends the HART command 46 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD45
Trim primary variable current DAC zero

**Description:**
HART command 45 The function block sends the HART command 45 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD44
Write primary variable units

**Description:**
HART command 44 The function block sends the HART command 44 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD48
Read additional device status

**Description:**
HART command 48 The function block sends the HART command 48 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD53
Write transmitter variable units

**Description:**
HART command 53 The function block sends the HART command 53 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD51
Write dynamic variable assignements

**Description:**
HART command 51 The function block sends the HART command 51 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD50
Read dynamic variable assignements

**Description:**
HART command 50 The function block sends the HART command 50 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD33
Read transmitter variables

**Description:**
HART command 33 The function block sends the HART command 33 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD34
Write primary variable damping value

**Description:**
HART command 34 The function block sends the HART command 34 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD40
Enter/Exit primary variable current mode

**Description:**
HART command 40 The function block sends the HART command 40 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD38
Reset configuration changed flag

**Description:**
HART command 38 The function block sends the HART command 38 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD35
Write primary variable range values

**Description:**
HART command 35 The function block sends the HART command 35 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMDCustom
FbHART_CMDCustom allows the execution of any HART command

**Description:**
The function block sends a HART command request to a HART device and returns the response as an array of byte. The interpretation of the response is up to the user. oStatus: CHANNEL_INVALID

### FbHART_CMD17
Write message

**Description:**
HART command 17 The function block sends the HART command 17 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD16
Read final assmbly number

**Description:**
HART command 16 The function block sends the HART command 16 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD15
Read output information

**Description:**
HART command 15 The function block sends the HART command 15 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD2
Read current and percent of range

**Description:**
HART command 2 The function block sends the HART command 2 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD19
Write final assmbly number

**Description:**
HART command 19 The function block sends the HART command 19 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD18
Write tag, descriptor and date

**Description:**
HART command 18 The function block sends the HART command 18 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD11
Read unique identifier associated with input tag

**Description:**
HART command 11 The function block sends the HART command 11 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD1
Read primary variable

**Description:**
HART command 1 The function block sends the HART command 1 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD14
Read Sensor serial number,Units code for sensor limits and minimum span, Upper sensor limit, Lower sensor limit, Minimum span

**Description:**
HART command 14 The function block sends the HART command 14 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD6
Write polling address

**Description:**
HART command 6 The function block sends the HART command 6 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD13
Read tag, descriptor and date

**Description:**
HART command 13 The function block sends the HART command 13 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD12
Read message

**Description:**
HART command 12 The function block sends the HART command 12 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

### FbHART_CMD3
Read all variables

**Description:**
HART command 3 The function block sends the HART command 3 request to a HART device and processes the response. oStatus: CHANNEL_INVALID

## Data Types

### typHART_CMD9
Structure type.

### eStatus
Enumeration type.

### typHART_CMD3
Structure type.

### typHART_CMD2
Structure type.

### typHART_CMD15
Structure type.

### typHART_FDT
Structure type.

### typHART_CMD48
Structure type.

### typHART_CMD35
Structure type.

### typHART_CMD0
Structure type.

### typHART_2AI_MODE8
Structure type.

### typHART_2AI
Structure type.

### typHART_CMD14
Structure type.

### typHART_CMD1
Structure type.

### typHART_CMD13
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbHART_CMD9: FbHART_CMD9;
END_VAR

// Basic function block usage
fbFbHART_CMD9(
    // Configure inputs as needed
);

// Check status
IF fbFbHART_CMD9.xValid THEN
    // Operation successful
END_IF

IF fbFbHART_CMD9.xError THEN
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

