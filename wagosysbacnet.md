# WagoSysBACnet v2.0.1.12

## Overview
WAGO PLC library providing WagoSysBACnet functionality.

**Key Features:**
- Time and date operations
- Communication protocols
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbCoVList
### FbBACnetPropertySubordinateList
### FbBACnetPropertyCommandTime
### FbLastError
**Methods:**

#### read
### FbBACnetPropertyBACnetDateAndTime
### FbLedStatus
### FbNotificationClass_large
### FbNotificationClass_medium
### FbBACnetPropertyPriority
### FbBACnetPropertyAckRequired
### FbNotificationClass_small
### FbEventList
**Methods:**

#### AcknowledgeAll
#### AcknowledgeAllByFilter
#### Read
### FbEventEnrollment_large
### FbEventLog_medium
### FbEventLog_large
### FbBACnetPropertyClientCovIncrement
### FbTrendLogMultiple_large
### FbTrendLog_large
### FbTrendLogMultiple_small
### FbRemoteProperty_Any
This functionblock represents an ANY remote property from a remote object. The remote property is specified by the constructor with the remote object and the property identifier. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

### FbTrendLogMultiple_medium
### FbRemoteProperty_BinaryPrioArray
This functionblock represents the priority array of a remote binary object. The remote object is specified by the constructor. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteProperty_MultiStatePrioArray
This functionblock represents the priority array of a remote multistate object. The remote object is specified by the constructor. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteProperty_AlarmValues
This functionblock represents the alarm values of a remote multistate object. The remote object is specified by the constructor. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteProperty_Unsigned
This functionblock represents an UNSIGNED (UDINT) remote property from a remote object. The remote property is specified by the constructor with the remote object and the property identifier. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteObject
This functionblock represents a remote object on a remote device. The remote object is specified by the device instance of the remote device, the object type and instancenumber of the remote object. This parameters are set by the constructor.

### FbRemoteProperty_AnalogPrioArray
This functionblock represents the priority array of a remote analog object. The remote object is specified by the constructor. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteProperty_Units
This functionblock represents the units of a remote object. The remote object is specified by the constructor. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteProperty_Reliability
This functionblock represents the reliability property of a remote object. The remote object is specified by the constructor. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteProperty_LimitEnable
This functionblock represents the limit enable of a remote object. The remote object is specified by the constructor. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteProperty_StatusFlags
This functionblock represents the status flags of a remote object. The remote object is specified by the constructor. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

### FbRemoteProperty_Bool
This functionblock represents a BOOL remote property from a remote object. The remote property is specified by the constructor with the remote object and the property identifier. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbRemoteProperty_Real
This functionblock represents a REAL remote property from a remote object. The remote property is specified by the constructor with the remote object and the property identifier. Before you declare a property instance you have to declare a remote object (see |FbRemoteObject|).

**Methods:**

#### write
Write this remote property. The possible return values are *WagoTypesBACnet.eAsyncStatus.BUSY *WagoTypesBACnet.eAsyncStatus.DONE *WagoTypesBACnet.eAsyncStatus.ERROR .. note:: The application have to call this method cyclic and set the inout parameter `xTrigger` once to start the job. If the job is done (with or without errors) `xTrigger` will be reset by the method.

### FbBACnetPropertyObjectIdentifier
### FbEventLog_small
### FbEventEnrollment_small
### FbTrendLog_medium
### FbTrendLog_small
### FbOutOfServiceValueUnsigned
### FbBACnetPropertyBACnetDate
### FbDevice_small
**Methods:**

#### Create
Creates an BACnet object. In case of successful creation it returns 0. Otherwise an error id <> 0 is returned.

### FbBACnetPropertyActionText
### FbBACnetPropertyActionCommand
### FbCommand_large
### FbCommand_small
### FbOutOfServiceValueBool
### FbBACnetPropertyBitStringAlarmValues
### FbBACnetPropertyBitText
### FbBitStringValue_large
### FbBACnetPropertyBitStringPriorityArray
**Methods:**

#### SetPriority
### FbBitStringValue_medium
### FbBACnetPropertyBitString
### FbBitStringValue_small
### FbLargeAnalogValue_large
### FbLargeAnalogValue_medium
### FbBACnetPropertyLargeAnalogPriorityArray
**Methods:**

#### SetPriority
### FbLargeAnalogValue_small
### FbIntegerValue_large
### FbIntegerValue_medium
### FbBACnetPropertyIntegerPriorityArray
**Methods:**

#### SetPriority
### FbIntegerValue_small
### FbLoop_large
### FbLoop_medium
### FbLoop_small
### FbBACnetPropertyListOfObjectPropertyReferences
### FbBACnetPropertyExceptionSchedule
**Methods:**

#### addCalendarWeekAndDay
#### addCalendarReference
#### addCalendarDateRange
#### addCalendarDate
### FbBACnetPropertyEffectivePeriod
### FbSchedule_large
### FbBACnetPropertyWeeklySchedule
### FbBACnetPropertyScheduleDefault
### FbSchedule_medium
### FbOutOfServiceValueReal
### FbBACnetPropertyPresentValue
### FbBACnetPropertyMultiStatePriorityArray
**Methods:**

#### SetPriority
### FbBACnetPropertyBinaryPriorityArray
**Methods:**

#### SetPriority
### FbBACnetPropertyAnalogPriorityArray
**Methods:**

#### SetPriority
### FbBACnetPropertyLimitEnable
### FbBACnetPropertyEventTimeStamp
### FbBACnetPropertyEventMessageTextsConfig
### FbBACnetPropertyEventMessageTexts
### FbBACnetPropertyEventEnable
### FbBACnetPropertyAckedTransition
### FbBACnetPropertyStatusFlags
### FbSchedule_small
### FbCalendar_large
**Methods:**

#### Create
Creates an BACnet object. In case of successful creation it returns 0. Otherwise an error id <> 0 is returned.

### FbCalendar_small
### FbMultistateValue_large
**Methods:**

#### setStateText
### FbMultistateValue_medium
### FbMultistateValue_small
### FbMultistateOutput_large
**Methods:**

#### setStateText
### FbMultistateOutput_medium
### FbMultistateOutput_small
### FbMultistateInput_large
**Methods:**

#### setStateText
### FbMultistateInput_medium
### FbMultistateInput_small
### FbBinaryValue_large
### FbBinaryValue_medium
### FbBinaryValue_small
Put an Value to an local binary terminal or a plc variable.

### FbBinaryOutput_large
### FbBinaryOutput_medium
### FbBinaryOutput_small
Put an Value to an local binary terminal or a plc variable.

### FbBinaryInput_small
Get an Value from an local binary terminal or a plc variable and send it to the BACnet network.

### FbCommand_medium
### FbBinaryInput_medium
### FbAnalogValue_large
### FbAnalogValue_medium
### FbBinaryInput_large
### FbAnalogInput_large
### FbAnalogOutput_medium
### FbBACnetPropertyDateList
**Methods:**

#### deleteDateListItem
#### addWeekAndDay
#### addDateRange
#### addDate
### FbAnalogInput_small
Get an Value from an local analog terminal or a plc variable and send it to the BACnet network.

### FbAnalogInput_medium
### FbAnalogOutput_large
### FbAnalogOutput_small
### FbAnalogValue_small
## Usage Examples

### Basic Usage
```iec
VAR
    fbFbCoVList: FbCoVList;
END_VAR

// Basic function block usage
fbFbCoVList(
    // Configure inputs as needed
);

// Check status
IF fbFbCoVList.xValid THEN
    // Operation successful
END_IF

IF fbFbCoVList.xError THEN
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

