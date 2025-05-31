# WagoAppTOPASS v1.6.5.1

## Overview
WAGO PLC library providing WagoAppTOPASS functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbTOPASS_Client_3
Access to a TO-PASS web server

**Description:**
This function block may be used to exchange data with a TO-Pass web server, e.g. www.to-pass.com or a Wago TopassWebConnector running on a controller. If a special port is required the following syntax must be used,e.g.: 'http://192.168.1.96:1024' Access to scripts like 'wago/saveTO-PASS.php' is supported. If used with the WebConnector, no script is needed. Other than the FbTOPASS_Client the amount of data for analog and digital values (maximum 31) may be adjusted by the parameterlist: TOPASS_AI_DATACOUNT : BYTE :

### FbTOPASS_Client_2
Access to a TO-PASS web server

**Description:**
This function block extends the functionality of the FbTOPASS_Client by two additional inputs | ``sUserName`` | ``sPassword ``

### FbTOPASS_Client
Access to a TO-PASS web server

**Description:**
This function block may be used to exchange data with a TO-Pass web server, e.g. www.to-pass.com or a Wago TopassWebConnector running on a controller. If a special port is required the following syntax must be used,e.g.: 'http://192.168.1.96:1024' Access to scripts like 'wago/saveTO-PASS.php' is supported. If used with the WebConnector, no script is needed.

## Data Types

### eStatus
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbTOPASS_Client_3: FbTOPASS_Client_3;
END_VAR

// Basic function block usage
fbFbTOPASS_Client_3(
    // Configure inputs as needed
);

// Check status
IF fbFbTOPASS_Client_3.xValid THEN
    // Operation successful
END_IF

IF fbFbTOPASS_Client_3.xError THEN
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

