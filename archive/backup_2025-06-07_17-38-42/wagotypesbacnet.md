# WagoTypesBACnet v1.0.9.9

## Overview
WAGO PLC library providing WagoTypesBACnet functionality.

**Key Features:**
- Communication protocols
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbBACnetInternalUnsigned
### FbBACnetInternalSigned
### FbBACnetInternalReal
### FbBACnetInternalEnumerated
### FbBACnetInternalDouble
### FbBACnetInternalCharString
### FbBACnetInternalBool
### FbBACnetCommand
### FbBACnetDailyScheduleList
### FbBACnetInternalBitString
### FbBACnetDataTypeAny
### FbBACnetScheduleDate
### FbBaseValue
**Methods:**

#### fireValueChanged
#### fireUpdateProperty
### FbBACnetObjectIdentifier
### FbBACnetPeriod
### FbBACnetSpecialEvent
### FbDailySchedule
## Data Types

### FbBACnetDataTypeAny
### editDateListItem
Enumeration type.

### eBACnetNotifyType
Enumeration type.

### eBACnetReliabilityType
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbBACnetInternalUnsigned: FbBACnetInternalUnsigned;
END_VAR

// Basic function block usage
fbFbBACnetInternalUnsigned(
    // Configure inputs as needed
);

// Check status
IF fbFbBACnetInternalUnsigned.xValid THEN
    // Operation successful
END_IF

IF fbFbBACnetInternalUnsigned.xError THEN
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

