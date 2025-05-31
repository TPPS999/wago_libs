# WagoTypesAppLED v1.5.2.1

## Overview
Application LED control library for WAGO PLCs providing comprehensive LED management functionality.

**Key Features:**
- Complete LED control with multiple operating modes
- Sequence-based blink patterns for status indication
- Static, flash, and blink operations
- Hardware-independent color management
- Channel-based access control model
- Support for PFC100/PFC200 controllers

## Data Types

### eLedID
Enumeration type.

This enumeration identifies one of the LEDs which can be operated with ``FbAppLED``. .. note:: On some PLCs only a subset of this enumeration, e.g. ``AppLED_1`` ... ``AppLED_4`` or ``AppLED_1`` ... ``AppLED_6``, is physically available.

### eLedColor
Enumeration type.

This enumeration specifies one of the colors which the LED could display. .. note:: For the PFCX00-System are only the Colors Green, Red and Yello supported. .. note:: Prefix-Notations like ``LED_COLOR_OFF`` as known from v2.3 is not necessary here, because in V3 the type-name itself serves as sub-namespace.

## Usage Examples

### Basic LED Control
```iec
PROGRAM LED_Control
VAR
    fbStatusLED: FbAppLED;
    fbErrorLED: FbAppLED;
    xSystemOK: BOOL;
    xSystemError: BOOL;
END_VAR

// Initialize LEDs
fbStatusLED(eID := eLedID.AppLED_1, xOpen := TRUE);
fbErrorLED(eID := eLedID.AppLED_2, xOpen := TRUE);

// Status indication
IF xSystemOK THEN
    fbStatusLED.SetStatic(eLedColor.Green);
ELSE
    fbStatusLED.SetBlink(
        tTime1 := T#500ms, eColor1 := eLedColor.Yellow,
        tTime2 := T#500ms, eColor2 := eLedColor.Off
    );
END_IF

// Error indication
IF xSystemError THEN
    fbErrorLED.SetStatic(eLedColor.Red);
ELSE
    fbErrorLED.SetOff();
END_IF
```

### Sequence-Based Status Codes
```iec
VAR
    fbStatusLED: FbAppLED;
    aStartupSeq: ARRAY[1..6] OF typLedSequenceStep := [
        (tDuration := T#100ms, eColor := eLedColor.Red),
        (tDuration := T#100ms, eColor := eLedColor.Off),
        (tDuration := T#100ms, eColor := eLedColor.Yellow),
        (tDuration := T#100ms, eColor := eLedColor.Off),
        (tDuration := T#100ms, eColor := eLedColor.Green),
        (tDuration := T#0s, eColor := eLedColor.Green)  // End + final state
    ];
END_VAR

fbStatusLED(eID := eLedID.AppLED_1, xOpen := TRUE);

// Startup sequence
IF startup_phase THEN
    fbStatusLED.SetSequence(ADR(aStartupSeq), 6);
END_IF

// Wait for sequence completion
IF NOT fbStatusLED.xBusy THEN
    // Sequence completed, LED now in static mode
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

