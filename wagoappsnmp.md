# WagoAppSNMP v1.2.2.0

## Overview
WAGO PLC library providing WagoAppSNMP functionality.

**Key Features:**
- Time and date operations
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSnmpManager_Set_V3_Timed
Sends a SNMP-V1-SET telegram to the given Agent and process the response

**Description:**
This function block sends a SNMP-V1-SET telegram to the given Agent and process the response. The transmitt data are expected as data type universal TypeLengthValue(TLV).

### FbSnmpManager_Set_Timed
Sends a SNMP-V1-SET telegram to the given Agent and process the response

**Description:**
This function block sends a SNMP-V1-SET telegram to the given Agent and process the response. The transmitt data are expected as data type universal TypeLengthValue(TLV).

### FbSnmpManager_Get_V3_Timed
Sends a SNMP-V1-GET telegram to the given Agent and process the response

**Description:**
This function block sends a SNMP-V3-GET telegram to the given Agent and process the response. The response data provided as universal Type-Length-Value (TLV) and have to be converted into the requested datatype.

### FbSnmpManager_Get_Timed
Sends a SNMP-V1-GET telegram to the given Agent and process the response

**Description:**
This function block sends a SNMP-V1-GET telegram to the given Agent and process the response. The response data provided as universal Type-Length-Value (TLV) and have to be converted into the requested datatype.

### FbSnmpTrap_SendInformToAdr
Sends user defined inform to user defined address

**Description:**
This function-block sends user defined inform to user defined address If an additional OID+TLV is not necessary say '' for sOID and create a NULL Value for stData!

### FbSnmpTrap_SendInformToAdr_V3
Sends user defined inform to user defined address

**Description:**
This function-block sends user defined inform to user defined address If an additional OID+TLV is not necessary say '' for sOID and create a NULL Value for stData!

### FbSnmpManager_Set
Sends a SNMP-V1-SET telegram to the given Agent and process the response

**Description:**
This function block sends a SNMP-V1-SET telegram to the given Agent and process the response. The transmitt data are expected as data type universal TypeLengthValue(TLV).

### FbSnmpManager_Get_V3
Sends a SNMP-V1-GET telegram to the given Agent and process the response

**Description:**
This function block sends a SNMP-V3-GET telegram to the given Agent and process the response. The response data provided as universal Type-Length-Value (TLV) and have to be converted into the requested datatype.

### FbSnmpManager_Get
Sends a SNMP-V1-GET telegram to the given Agent and process the response

**Description:**
This function block sends a SNMP-V1-GET telegram to the given Agent and process the response. The response data provided as universal Type-Length-Value (TLV) and have to be converted into the requested datatype.

### FbSnmpManager_Set_V3
Sends a SNMP-V1-SET telegram to the given Agent and process the response

**Description:**
This function block sends a SNMP-V1-SET telegram to the given Agent and process the response. The transmitt data are expected as data type universal TypeLengthValue(TLV).

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSnmpManager_Set_V3_Timed: FbSnmpManager_Set_V3_Timed;
END_VAR

// Basic function block usage
fbFbSnmpManager_Set_V3_Timed(
    // Configure inputs as needed
);

// Check status
IF fbFbSnmpManager_Set_V3_Timed.xValid THEN
    // Operation successful
END_IF

IF fbFbSnmpManager_Set_V3_Timed.xError THEN
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

