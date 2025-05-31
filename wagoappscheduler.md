# WagoAppScheduler v1.1.2.17

## Overview
WAGO PLC library providing WagoAppScheduler functionality.

**Key Features:**
- Time and date operations
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbPublicHoliday
The function block includes the following time-switching functions: #. Detection of public holiday .. note:: Version of WagoAppTime > 1.7.2.4 is nesseccary.

### FbTemporalExpression
**Methods:**

#### CalculateTimeBeforeOperation
#### getActualDate
#### getActualTime
### FbBaseHolidaySwitch
### FbBaseTimeSwitch
### FbBasePriorityTimeSwitch
### FbSpecialPeriod
The function block includes the following time-switching functions: #. Scheduling on weekly basis within specified special period. .. note:: Version of WagoAppTime >= 1.7.2.5 is nesseccary.

### FbMultipleSpecialPeriod
The function block includes the following time-switching functions: #. Multiple scheduling on weekly basis within specified special period. .. note:: Version of WagoAppTime >= 1.7.2.5 is nesseccary.

### FbMultipleScheduleWeekly
The function block includes the following time-switching functions: #. Multiple scheduling on weekly basis .. note:: Version of WagoAppTime >= 1.7.2.5 is nesseccary.

### FbScheduleWeekly
The function block includes the following time-switching functions: #. Scheduling on weekly basis .. note:: Version of WagoAppTime >= 1.7.2.5 is nesseccary.

### FbWeekend
The function block check for weekend or any extended weekend due to public holiday.

### FbScheduler
The function block includes the following time-switching functions: #. Manual switching function #. Party mode function #. Public Holiday #. weekly special periods #. weekly time switches

**Description:**
The switching priorities are as follows: #. Manual operation mode. As long as this mode actives, only manual signal will be fowarded to the switch channel. #. Party mode. Active as long as the set duration. Retriggering the input prolongs the switch output signal. #. Public holiday time switch. #. Special periods. #. Schedule weekly. .. note:: The Party mode can be reset by using the method ResetPartySwitch. .. note:: Version of WagoAppTime >

## Data Types

### typStatusByte
Structure type.

### eStatusByte
Enumeration type.

### typSingleSpecialPeriod
Structure type.

### typMultipleSpecialPeriod
Structure type.

### typSingleScheduleWeekly
Structure type.

### typMultipleScheduleWeekly
Structure type.

### typHolidaySwitch
Structure type.

### typSpecialPeriod
Structure type.

### typEvent
Structure type.

### typScheduleWeekly
Structure type.

### typScheduler
Structure type.

### typCustomPublicHolidayList
Structure type.

### typPublicHolidayList
Structure type.

### eRecurrenceType
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbPublicHoliday: FbPublicHoliday;
END_VAR

// Basic function block usage
fbFbPublicHoliday(
    // Configure inputs as needed
);

// Check status
IF fbFbPublicHoliday.xValid THEN
    // Operation successful
END_IF

IF fbFbPublicHoliday.xError THEN
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

