# WagoAppTime v1.7.3.5

## Overview
Time and date handling library for WAGO PLCs with unified system time and RTC operations.

**Key Features:**
- Unified absolute time handling
- Standard and high-resolution time operations
- Timezone management with automatic DST
- Calendar calculations and conversions
- Elapsed time and timeout functions

## Core Function Blocks

### FbTimeZoneSetter
**Methods:**

#### SetTimeZone
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENOENT The database key is unknown to the system ENOSYS function not implemented EBUSY The Fb is busy with another request which is still in progress EUNSPECFIC Unexpected other errors from OS ============= ================================================================ |

**Status Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENOENT The database key is unknown to the system EUNSPECFIC Unexpected other errors from OS ============= ================================================================ |

### FbTimeoutWatcher
**Description:**
After a given amount of time this FB indicates a timeout. A timeout condition is normally indicated by the return value of the method

**Methods:**

#### HasTimeoutOccurred
Return value: TRUE when Timeout is reached or elapsed

#### initialize
This has to be called in derived function blocks, in order to initialize the parent FB properly. When FbElapsedTime is used directly, it may be ignored. When this FB is used as parent for inheritance, the child should call SUPER^.initialize() during its own initialization.

#### Retrigger
When using the FB as a 'watchdog', this is the recommended method for 'calming down' the watchdog. When retriggering, the previously set up timeout limit will be used again. No subsequent call of SetTimeout() is necessary.

#### SetTimeout
Timeout will occur after a time interval of 'tTimeOut' has elapsed after start of the FB or retriggering. Note: It is possible to change the timeout limit while the FB is running.

#### SetLTimeout
Timeout will occur after a time interval of 'tTimeOut' has elapsed after start of the FB or retriggering. Note: It is possible to change the timeout limit while the FB is running.

#### GetRemainingMilliseconds
Note: Zero or negative return values indicate that the timout has occurred. If the value would exceed the range of 32-Bits, the return value is clamped to +-16#7FFF.FFFF in order to avoid strange problems with wrap-arounds.

#### GetRemainingNanoseconds
Note: Zero or negative return values indicate that the timout has occurred. If the value would exceed the range of 64-Bits, the return value is clamped to +-16#7FFF.FFFF.FFFFF.FFFF in order to avoid strange problems with wrap-arounds (regarding the usable range of 292 years, this detail has more formal use rather than practical use)

### FbElapsedTime
**Description:**
This FB measures the elapsed time from a an indicated start. The elapsed time my be read as LTIME or as TIME by getter-methods.

**Methods:**

#### initialize
This has to be called in derived function blocks, in order to initialize the parent FB properly. When FbElapsedTime is used directly, it may be ignored. When this FB is used as parent for inheritance, the child should call SUPER^.initialize() during its own initialization.

#### StartNow
#### GetElapsedTime
When more than ~49 days have elapsed, the result would overflow, thus it is clamped to 16#FFFF.FFFF to indicate the overflow.

#### GetElapsedLTime
When more than ~292 years have elapsed, the result would overflow, thus it is clamped to 16#7FFF.FFFF.FFFF.FFFF to indicate the overflow (this is performed for formal reasons rather than for practical ones).

## Compact Function Blocks

### FbTimeZoneSetter_cpt
This fumction block is a time zone setter for use in graphical languages.

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

