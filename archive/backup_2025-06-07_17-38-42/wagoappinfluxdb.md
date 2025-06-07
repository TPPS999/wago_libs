# WagoAppInfluxDB v1.0.2.5

## Overview
WAGO PLC library providing WagoAppInfluxDB functionality.

**Key Features:**
- Time and date operations
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbRealTimeBufferAndWriteInfluxMeasurement
This function block buffers in real time multiple fields of one measurement and including possible tags and send it in an InfluxDB v1.x with HTTP POST commands.

**Description:**
The complete buffer is send, when it is full. Buffering can be done even when sending is in progress. .. note:: The buffer size for the POST command is defined in the ParameterList and can be changed by user. It is preffered to extend the buffer size instead of sending more POSTs. .. note:: This function block allocates more than double of the parameterized buffer size. .. note:: Buffering while sending progress is in action (xTrigger) is possible as far as there are not more data to buffer than the buffer size. If the buffer is to small and sending progress is still active there will may be data loss. Example: .. code-block:: codesys VAR oMyMeasurement : WagoAppInfluxDB.FbBufferAndWriteInfluxMeasurement; xStore : BOOL; //Positive Edge stores values to buffer. Sending values automatically, when buffer is full. xTrigger : BOOL; //internal trigger of influx function block sIP : STRING(16):

### FbRealTimeBufferAndWriteInfluxV2Measurement
This function block buffers in real time multiple fields of one measurement and including possible tags and send it in an InfluxDB v2.0 with HTTP POST commands.

**Description:**
The complete buffer is send, when it is full. Buffering can be done even when sending is in progress. .. note:: The buffer size for the POST command is defined in the ParameterList and can be changed by user. It is preffered to extend the buffer size instead of sending more POSTs. .. note:: This function block allocates more than double of the parameterized buffer size. .. note:: Buffering while sending progress is in action (xTrigger) is possible as far as there are not more data to buffer than the buffer size. If the buffer is to small and sending progress is still active there will may be data loss. Example: .. code-block:: codesys VAR oMyMeasurement : WagoAppInfluxDB.FbBufferAndWriteInfluxV2Measurement; xStore : BOOL; //Positive Edge stores values to buffer. Sending values automatically, when buffer is full. xTrigger : BOOL; //internal trigger of influx function block sIP : STRING(16) :

### FbCreateBucket
This function block creates a bucket in an influx V2.x database. This needs to be done once before any measurement can be written into the bucket.

**Description:**
With empty input ``sRetentionRules`` the bucket will be created without retentionRules so the data never expires. Example for ``sRetentionRules`` declaration: .. code-block:: codesys VAR sRetentionRules : STRING :

### FbBufferAndWriteInfluxMeasurement
This function block buffers multiple fields of one measurement and including possible tags and send it in an InfluxDB v1.x with HTTP POST commands.

**Description:**
The complete buffer is send, when it is full. If the current values can not be buffered completely, the previous values will be send first and the current values get buffered after sending is ready. .. note:: The buffer size for the POST command is defined in the ParameterList and can be changed by user. It is preffered to extend the buffer size instead of sending more POSTs. Example: .. code-block:: codesys VAR oMyMeasurement : WagoAppInfluxDB.FbBufferAndWriteInfluxMeasurement; xStore : BOOL; //Positive Edge stores values to buffer. Sending values automatically, when buffer is full. xTrigger : BOOL; //internal trigger of influx function block sIP : STRING(16):

### FbBufferAndWriteInfluxV2Measurement
This function block buffers multiple fields of one measurement and including possible tags and send it in an InfluxDB v2.0 with HTTP POST commands.

**Description:**
The complete buffer is send, when it is full. If the current values can not be buffered completely, the previous values will be send first and the current values get buffered after sending is ready. .. note:: The buffer size for the POST command is defined in the ParameterList and can be changed by user. It is preffered to extend the buffer size instead of sending more POSTs. Example: .. code-block:: codesys VAR oMyMeasurement : WagoAppInfluxDB.FbBufferAndWriteInfluxV2Measurement; xStore : BOOL; //Positive Edge stores values to buffer. Sending values automatically, when buffer is full. xTrigger : BOOL; //internal trigger of influx function block sIP : STRING(16) :

### FbWriteInfluxMeasurement
This function block writes multiple fields of one measurement including possible tags in an InfluxDB v1.x with HTTP POST commands.

**Description:**
Example: .. code-block:: codesys VAR oMyMeasurement : WagoAppInfluxDB.FbWriteInfluxMeasurement; xWrite : BOOL; //TRUE triggers writing process with current variables xTrigger : BOOL; //internal trigger of influx function block sIP : STRING(16):

### FbWriteInfluxV2Measurement
This function block writes multiple fields of one measurement including possible tags in an InfluxDB v2.0 with HTTP POST commands.

**Description:**
Example: .. code-block:: codesys VAR oMyMeasurement : WagoAppInfluxDB.FbWriteInfluxV2Measurement; xWrite : BOOL; //TRUE triggers writing process with current variables xTrigger : BOOL; //internal trigger of influx function block sIP : STRING(16):

### FbCreateDatabase
This function block creates a database in an influx database. This needs to be done once before any measurement can be written into the database.

## Data Types

### eTimeStampHandling
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbRealTimeBufferAndWriteInfluxMeasurement: FbRealTimeBufferAndWriteInfluxMeasurement;
END_VAR

// Basic function block usage
fbFbRealTimeBufferAndWriteInfluxMeasurement(
    // Configure inputs as needed
);

// Check status
IF fbFbRealTimeBufferAndWriteInfluxMeasurement.xValid THEN
    // Operation successful
END_IF

IF fbFbRealTimeBufferAndWriteInfluxMeasurement.xError THEN
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

