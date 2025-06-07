# WagoAppSerial_Sms v1.6.3.2

## Overview
WAGO PLC library providing WagoAppSerial_Sms functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSimpleSms_8207
This module supports the receiving and the sending of short messages using the internal GSM-Modem of a WAGO controller 750-8207. The length of messages is limited to 160 characters per message. .. note:: For the limit of 160 characters there count each char from the GSM Extended Table as 2 chars. .. hint:: This function block is designed special for the WAGO contoller 750-8207 and the use of the internal modem. Other modems may have problems by working with this fb. Please prefer |FbGsmSms| for other modems. .. note:: The input parameter ``sPin`` is ignored because it is not possible to set set the pin from plc. To set the pin please use the WBM. .. warning:: You may use only one instance of this functionblock for each modem. It is not allowed to use different instances for the same modem.

### FbUcpSms
This module supports the sending of a SMS with Universal Computer Protocol (UCP) from the landline via a modem connection. The used Short Message Service Center (SMSC) must provide a modem access with UCP protocol. Operation types 01; 30 und 51 as per EMI specification are supported. All required interface call-ups are encapsulated in this module, therefore, only the module "FbUcpSms" must be called up cyclic. .. note:: It's not supported to receive SMS

### FbTapSms
This module supports the sending of a SMS with Telocator Alphanumeric Protocol (TAP) from the landline via a modem connection. The used Short Message Service Center (SMSC) must provide a modem access with TAP protocol. All required interface call-ups are encapsulated in this module, therefore, only the module "FbTapSms" must be called up cyclic. .. note:: It's not supported to receive SMS

### FbGsmSms
This module supports the receiving and the sending of short messages using a GSM-Modem. The length of messages is limited to 160 characters per message. .. note:: For the limit of 160 characters there count each char from the GSM Extended Table as 2 chars. .. warning:: You may use only one instance of this functionblock for each modem. It is not allowed to use different instances for the same modem.

**Methods:**

#### Cp1252_To_GsmChar
#### getItemFromBuffer
## Data Types

### eAction
Enumeration type.

### typStatusSms
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSimpleSms_8207: FbSimpleSms_8207;
END_VAR

// Basic function block usage
fbFbSimpleSms_8207(
    // Configure inputs as needed
);

// Check status
IF fbFbSimpleSms_8207.xValid THEN
    // Operation successful
END_IF

IF fbFbSimpleSms_8207.xError THEN
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

