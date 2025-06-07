# WagoSysModule_75x_640 v1.9.1.0

## Overview
WAGO PLC library providing WagoSysModule_75x_640 functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbModule_75x_640
This function block represents a RTC-Module 750-640. If you get one of this module from the toolbox and place it to your local k-bus an global instance of this FB will be automaticly generated. You may change the name of the instance and give it your own identification. After this you can use the given methods to configure your module. To get the actual time you have only to read the output parameter ``<myFbName>.todLocalTime``. This variable will be automaticly updated in the background. Also you can get some further information from the module. .. _manual of the module 750-640: http://www.wago.de/download.esm?file=%5Cdownload%5C00189428_0.pdf&name=m07500640_00000000_0en.pdf For detailed use please read the `manual of the module 750-640`_.

**Methods:**

#### ClearChannels
This method clears the channels. Each bit represents one channel. You have to connect the input parameter ``xTrigger`` with an own bool variable. To clear the channels specified by ``dwChannels`` you have to set the variable at ``xTrigger`` once to TRUE. If the job was delivered then the variable is set to FALSE by the method. .. _manual of the module 750-640: http://www.wago.de/download.esm?file=%5Cdownload%5C00189428_0.pdf&name=m07500640_00000000_0en.pdf For detailed use please read the `manual of the module 750-640`_.

#### SetToManufacturerSettings
#### SetAntenna
This method set the decoder scheme for time signal reception. See the manual for further information. Possible values for 'bAntenna' ===== ===== ========================================== Byte Bit Function ===== ===== ========================================== 0 0..1 | 0: No time signal reception | 1: DCF77 Decoder activated | 2: WWVB Decoder activated ----- ----- ------------------------------------------ 0 2 | DCF77 Polarity reversed | 0 = Low-active | 1 = High-active ===== ===== ========================================== You have to connect the input parameter ``xTrigger`` with an own bool variable. To transmit the value from ``bAntenna`` to the module you have to set the variable at ``xTrigger`` once to TRUE. If the method has delivered the value then the variable is set to FALSE by the method. .. Note:: On setting the time zone and summer time using different antennas. * The DCF77 transmitter sends CET (Central European Time) or CEST (Central European Summer Time), the summer time setting (DstBias) remains set to zero. The time zone for Germany is 0. * The WWVB transmitter sends in UTC. If the module is operated at the US east coast (Eastern Time) for example, an offset of 5 hours (0xFFFFB9B0) must be entered in the TimeZone. The transition from winter time to summer time is done using a status bit within the time telegram. By setting this bit, one more hour will be transmitted by the module. Within the module, the transition is always performed at 00:00.

#### SetDstBias
#### SetTimeZone
#### SetAuto
This method switch the automatic mode on / off for the channels. Each bit represents one channel. The automatic mode of the relevant switching channel is switched off for each bit set in Auto. The off switching channel can only be changed using the methods SetChannels() and ClearChannels(). .. _manual of the module 750-640: http://www.wago.de/download.esm?file=%5Cdownload%5C00189428_0.pdf&name=m07500640_00000000_0en.pdf For detailed use please read the `manual of the module 750-640`_.

#### SetDateAndTime
## Usage Examples

### Basic Usage
```iec
VAR
    fbFbModule_75x_640: FbModule_75x_640;
END_VAR

// Basic function block usage
fbFbModule_75x_640(
    // Configure inputs as needed
);

// Check status
IF fbFbModule_75x_640.xValid THEN
    // Operation successful
END_IF

IF fbFbModule_75x_640.xError THEN
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

