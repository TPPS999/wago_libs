# WagoAppRTC v1.6.2.0

## Overview
WAGO PLC library providing WagoAppRTC functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbRtcConverter
Functionblock to support the base functions of GPS-DCF-Konverter 2852-7901. .. _manual of the device 2852-7901: https://www.wago.com/de/d/11050 .. _manual of the module 750-640: https://www.wago.com/de/io-systeme/real-time-clock-modul/p/750-640#details For detailed use please read the `manual of the module 750-640`. .. note:: You should always call this FB cyclic.

### FbRtcBaseFunctions
Functionblock to support the base functions of RTC-Module 750-640. .. _manual of the module 750-640: http://www.wago.de/download.esm?file=%5Cdownload%5C00189428_0.pdf&name=m07500640_00000000_0en.pdf For detailed use please read the `manual of the module 750-640`_. .. note:: You should always call this FB cyclic.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbRtcConverter: FbRtcConverter;
END_VAR

// Basic function block usage
fbFbRtcConverter(
    // Configure inputs as needed
);

// Check status
IF fbFbRtcConverter.xValid THEN
    // Operation successful
END_IF

IF fbFbRtcConverter.xError THEN
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

