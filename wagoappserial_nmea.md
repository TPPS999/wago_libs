# WagoAppSerial_NMEA v1.6.4.0

## Overview
WAGO PLC library providing WagoAppSerial_NMEA functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbNmeaSubscriber
NMEA - Receiver for receiving all NMEA-Sentences and send all given sentences. This FB contains the basic functionality for sending and receiving NMEA sentences. You have to call this function block once for each cycle in your project to process the common functionality. To get sentences from all the internal received sentences this FB provides two methods (see |FbNmeaSubscriber.GetFilteredSentence| and |FbNmeaSubscriber.GetEachSentence| ) For sending any sentence it will supported by the method |FbNmeaSubscriber.WriteSentence| .. note:: You should always call this FB cyclic.

**Methods:**

#### WriteSentence
Write a NMEA sentence to the serial interface. .. note:: For use this method you have to call the |FbNmeaSubscriber| cyclic.

#### GetEachSentence
Get each received sentences. .. note:: For use this method you have to call the |FbNmeaSubscriber| cyclic.

#### GetFilteredSentence
Filters the sentences specified by sentence type and address pattern from all received sentences. Sentence types may be combine by 'OR' to get different types. Address pattern may use wildcards '?' and '*'. + '?' means one of any char + '*' means as many as you like of any char

#### CheckCrc
#### SearchEnd
#### DeleteRxBuffer
#### SearchStart
#### HexToByte
## Usage Examples

### Basic Usage
```iec
VAR
    fbFbNmeaSubscriber: FbNmeaSubscriber;
END_VAR

// Basic function block usage
fbFbNmeaSubscriber(
    // Configure inputs as needed
);

// Check status
IF fbFbNmeaSubscriber.xValid THEN
    // Operation successful
END_IF

IF fbFbNmeaSubscriber.xError THEN
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

