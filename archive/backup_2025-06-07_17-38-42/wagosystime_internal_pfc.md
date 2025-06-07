# WagoSysTime_Internal_PFC v1.1.0.6

## Overview
Time and date handling library for WAGO PLCs with unified system time and RTC operations.

**Key Features:**
- Unified absolute time handling
- Standard and high-resolution time operations
- Timezone management with automatic DST
- Calendar calculations and conversions
- Elapsed time and timeout functions

## Core Function Blocks

### _FbTimeZoneSetter_Internal
**Methods:**

#### GetResult
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | setting the time zone was successfully finished EAGAIN setting is still in progress, try again ENOENT The database key is unknown to the system ENOSYS function not implemented ============= ====================================================================================== |

#### SetTimeZone
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENOENT The database key is unknown to the system ENOSYS function not implemented EINPROGRESS Call was deferred so the result comes later ============= ====================================================================================== |

## Usage Examples

### Basic Time Operations
```iec
VAR
    current_time: DATE_AND_TIME;
    elapsed_time: TIME;
    fbTimeout: FbTimeoutWatcher;
    fbElapsed: FbElapsedTime;
END_VAR

// Get current time
current_time := FuGetDateAndTime();

// Timeout implementation
fbTimeout.StartNow();
fbTimeout.SetTimeout(T#10S);

IF fbTimeout.HasTimeoutOccurred() THEN
    // Handle timeout
END_IF

// Elapsed time measurement
fbElapsed.StartNow();
// ... do work ...
elapsed_time := fbElapsed.GetElapsedTime();
```

### Date Calculations
```iec
VAR
    today: DATE;
    next_monday: DATE;
    days_in_month: UINT;
END_VAR

today := DATE_AND_TIME_TO_DATE(FuGetDateAndTime());
next_monday := FuNextWeekday(today, 1);  // 1 = Monday
days_in_month := FuDaysInMonth(FuMonth(today), FuYear(today));
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

