# WagoAppSiemensS7Protocol v1.7.0.4

## Overview
WAGO PLC library providing WagoAppSiemensS7Protocol functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbISOonTcpClient
This is an ISO On-TCP client

**Description:**
This function block acts as a client for an ``ISO On-TCP`` connection supporting class 0. Once a data message has arrived the output ``xDataReceived`` will be set for one cycle. The size of the data is displayed by ``uiRxIndex``.It is recommended to set this variable to zero once the data has been processed. New data will always start in the receive buffer by index ``uiRxIndex``. Using input ``xTxTrigger`` it is possible to transmit data from the client to the server. The variable ``xTxTrigger`` will be reset after an acknowledge from the server is received. Only than new data may be send. .. note:: TPDU size is always 1024 byte.

### FbISOonTcpSingleServer
This is an ISO OnTCP server

**Description:**
This function block acts as a server for a ``ISO OnTCP`` connection. The server starts waiting for clients, if the input ``xOpen`` is set to TRUE. The server can handle one connection. Using input ``xTxTrigger`` it is possible to transmit data from the server to the client. The variable ``xTxTrigger`` will be reset after an acknowledge from the client is received. Only than new data may be send. Once a data message has arrived the output ``xDataReceived`` will be set for one cycle. The size of the data is displayed by ``uiRxIndex``.It is recommended to set this variable to zero once the data has been processed. New data will always start in the receive buffer by index ``uiRxIndex``.

### Fb_Exit
### Fb_DB_ReadWrite
Data transfer according to S7 protocol

**Description:**
This function block allows to read and write data from a Siemens plc. The maximum amount of data is 200 Byte. The received data will be stored in aReadData. The outputs display either successful execution of the command or error details. oStatus: aReadData array too small->Increase the global constant DB_MAX_DBSIZE in the parameter list Server response error.DB data invalid->the DB in the plc is either not available or the area withhin the DB is too large(DB size is 10 byte and a read command asks for 15 bytes) MAX_SEND_TCP_CLIENT_ToSmall->reduce wDB_Length or increase global constant DB_MAX_DBSIZE Write command failed ->the DB in the plc is either not available or the area withhin the DB is too large ..note: | Using Siemens TIA Portal may need the following settings | | In the DB preferences the ‘Optimized block access’ has to be disabled. | Depending on the PLC, e.g. a S7-1200, the ‘Permit access with | PUT/GET communication from remote partner’ has to be enabled in | the PLC preferences under ‘Protection’.

## Data Types

### eStatus
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbISOonTcpClient: FbISOonTcpClient;
END_VAR

// Basic function block usage
fbFbISOonTcpClient(
    // Configure inputs as needed
);

// Check status
IF fbFbISOonTcpClient.xValid THEN
    // Operation successful
END_IF

IF fbFbISOonTcpClient.xError THEN
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

