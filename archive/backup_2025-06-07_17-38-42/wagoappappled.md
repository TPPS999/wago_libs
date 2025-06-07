# WagoAppAppLED v1.7.2.2

## Overview
Application LED control library for WAGO PLCs providing comprehensive LED management functionality.

**Key Features:**
- Complete LED control with multiple operating modes
- Sequence-based blink patterns for status indication
- Static, flash, and blink operations
- Hardware-independent color management
- Channel-based access control model
- Support for PFC100/PFC200 controllers

## Core Function Blocks

### FbAppLED_SetSequence
The functionblock ``FbAppLED_SetSequence_cpt()`` starts the display of a blink code for indicating a specific status or error condition.

**Description:**
Each pulse of the sequence has an individually settable duration and color. If off-phases are required between the pulses, these off-phases have to be represented by an individual sequence step with color ``off``. The input ``pSequence`` points to an array of sequence steps (:ref:`typLedSequenceStep`). This array has a variable length which is denoted by ``udiSequenceSize``. When a sequence step carries a duration of 0, this also denotes the end of the sequence, even if ``udiSequenceSize`` indicates more steps. Once initiated, the sequence cannot be altered - but it can be stopped or restarted instead. While the sequence is in progress, the ``xBusy``-Output of the FB is ``TRUE``. After the sequence has terminated, the LED transits to the ``static`` mode and displays the color of the last sequence step (i.e. the one with ``T#0s``, when the sequence contains such a step). A falling edge at ``xEnable`` stop the execution and switch off th LED, for a new execution or a parameter change a rising edge at ``xEnable`` is necessary. The stauts output ``xBusy`` is set, while ``xEnable`` is set and the functionblock is still in progress. The status output ``xValid`` indicate a successful operation, it will be rest with a falling edge at ``xEnable``. The status output ``xError`` indicate a problem in the execution of the functionblock, it will be reset one cycle after ``xBusy`` was reset.

**Status Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The Fb is not in the Open (=Enabled) state EBADR Requested Color is not suported EINVAL Illegal sequence description or no sequence given ============= ================================================= |

### FbAppLED_SetStatic
The functionblock ``FbAppLED_SetStatic_cpt()`` makes the LED continuosly display a given color or switches the LED off.

**Description:**
If the requested color is not supported by the hardware, this method fails with ``EBADR`` ('Bad Request'); A falling edge at ``xEnable`` stop the execution and switch off th LED, for a new execution or a parameter change a rising edge at ``xEnable`` is necessary. The stauts output ``xBusy`` is set, while ``xEnable`` is set and the functionblock is still in progress. The status output ``xValid`` indicate a successful operation, it will be rest with a falling edge at ``xEnable``. The status output ``xError`` indicate a problem in the execution of the functionblock, it will be reset one cycle after ``xBusy`` was reset.

**Status Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The Fb is not in the Open (=Enabled) state EBADR Requested Color is not suported EINVAL invalid arguments ============= ====================================================================================== |

### FbAppLED_SetOn
The functionblock ``FbAppLED_SetOn_cpt()`` switches the LED to a device specific color which is guaranteed to be visible.

**Description:**
This functionblock is similar to ``FbAppLED_SetStatic_cpt()``, but it guarantees that the LED will turn on in some default color. When using ``FbAppLED_SetStatic_cpt()`` in contrast, the user may select the color, but the LED will not turn on if he selects a color which cannot be displayed (e.g. ``blue`` on a red-green-LED). A falling edge at ``xEnable`` stop the execution and switch off th LED, for a new execution or a parameter change a rising edge at ``xEnable`` is necessary. The stauts output ``xBusy`` is set, while ``xEnable`` is set and the functionblock is still in progress. The status output ``xValid`` indicate a successful operation, it will be rest with a falling edge at ``xEnable``. The status output ``xError`` indicate a problem in the execution of the functionblock, it will be reset one cycle after ``xBusy`` was reset. .. note:: Which color is used as default color depends on the target hardware and on the type of the LED. It is hardcoded in the target depending internal libraries and cannot be changed by the user. It is ensured that the default color is visible for the addressed target hardware. On error, no change of the LED state takes place.

**Status Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The FB is not in the Open (=Enabled) state ============= ====================================================================================== |

### FbAppLED_SetBlink
The functionblock ``FbAppLED_SetBlink_cpt()`` makes the LED toggle periodically between two colors.

**Description:**
If ``xEnable`` true, then ``eColor1`` is displayed for the duration ``tTime1``. After that on-time has elapsed, the second color (``eColor2``) appears for a duration of ``tTime2``. After that second time, this process repeats with ``eColor1``. A falling edge at ``xEnable`` stop the execution and switch off th LED, for a new execution or a parameter change a rising edge at ``xEnable`` is necessary. The stauts output ``xBusy`` is set, while ``xEnable`` is set and the functionblock is still in progress. The status output ``xValid`` indicate a successful operation, it will be rest with a falling edge at ``xEnable``. The status output ``xError`` indicate a problem in the execution of the functionblock, it will be reset one cycle after ``xBusy`` was reset. .. figure:: ../../Images/__diag_ledblink.png :align: center :alt: Timing Diagram On error, no change of the LED state takes place.

**Status Codes:**
| Code | Description |
|------|-------------|
| 0 | Success ENOENT The desired LED-ID does not exist on this PLC EBADR Requested Color is not supported EINVAL invalid parameters ============= ====================================================================================== |

### FbAppLED_SetFlash
The functionblock ``FbAppLED_SetFlash_cpt()`` displays a color for a short time and displays a second color statically afterwards.

**Description:**
If ``xEnable`` true, then the color of this 'flash' is given by ``eColor1`` and its duration is given by ``tFlashTime``. After ``tFlashTime`` has elapsed, the LED displays the other color ``eColor2`` (which may be a visible color as well as simply ``off``). A falling edge at ``xEnable`` stop the execution and switch off th LED, for a new execution or a parameter change a rising edge at ``xEnable`` is necessary. The stauts output ``xBusy`` is set, while ``xEnable`` is set and the functionblock is still in progress. The status output ``xValid`` indicate a successful operation, it will be rest with a falling edge at ``xEnable``. The status output ``xError`` indicate a problem in the execution of the functionblock, it will be reset one cycle after ``xBusy`` was reset. .. figure:: ../../Images/__diag_ledflash.png :align: center :alt: Timing Diagram While the first phase of the flash is in progress, the ``xBusy``-Output of the FB is ``TRUE``. When applying this function while the LED is still 'flash'ing, the flash time will be retriggered. When the flash time is expired, the LED transits into the ``static`` mode. .. note:: Some legacy libraries require the LED to be driven into in certain other operating modes (namely 'static') before the LED could be driven to flash mode. This FB, however, has no such restriction. On error, no change of the LED state takes place.

**Status Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The Fb is not in the Open (=Enabled) state EBADR Requested Color is not suported EINVAL Invalid parameters ============= ====================================================================================== |

### FbAppLED
The Function Blocks ``FbAppLED`` provides access to one of the App-LEDs of the controller in various operating modes.

**Description:**
This Fb implements the behaviour model :ref:`WagoChannel <FbBehaviourModel_WagoAppChannel>` in order to coordinate access to the LEDs from different places within the application program. A ``TRUE`` state at the input ``xOpen`` opens the access to the LED and a ``FALSE`` state closes it again. (For a general description of this model, please refer to :ref:`FbBehaviourModel_WagoChannel`). Before using a App-LED, the ID of the App LED has to be passed to the input ``FbAppLED.eID``. While using a App-LED, the ``xOpen``-Input has to be kept ``TRUE``. If ``eID`` denotes an LED which does not exist on the given hardware, the result code ``ENOENT`` and ``xError

**Methods:**

#### SetSequence
The method ``SetSequence()`` starts the display of a blink code for indicating a specific status or error condition.

Each pulse of the sequence has an individually settable duration and color. If off-phases are required between the pulses, these off-phases have to be represented by an individual sequence step with color ``off``. The input ``pSequence`` points to an array of sequence steps (:ref:`typLedSequenceStep`). This array has a variable length which is denoted by ``udiSequenceSize``. When a sequence step carries a duration of 0, this also denotes the end of the sequence, even if ``udiSequenceSize`` indicates more steps. Once initiated, the sequence cannot be altered - but it can be stopped or restarted instead. While the sequence is in progress, the ``xBusy``-Output of the FB is ``TRUE``. After the sequence has terminated, the LED transits to the ``static`` mode and displays the color of the last sequence step (i.e. the one with ``T#0s``, when the sequence contains such a step).

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The Fb is not in the Open (=Enabled) state EBADR Requested Color is not suported EINVAL Illegal sequence description or no sequence given ============= ================================================= |

#### UpdateSequence
The method ``UpdateSequence()`` assigns a new :ref:`typLedSequenceStep <typLedSequenceStep>`-pointer to the ``FbAppLED`` while the blink sequence is still in progress.

If a null pointer is given for the new sequence address, the sequence will be aborted. This method does not fail and thus does not return any result code. It may also be called while no sequence is in progress, but it has no immediate effect then until the new sequence starts. .. note :: This method must be called at Online-Change by the embedding FB it it uses blink sequences, because at Online-Change absolute locations may change and pointers have to be updated afterwards. .. note :: This Method may be called even if the FB is not open, because it does not initiate any action. .. note:: For the PFCX00-System are only the Colors Green, Red and Yello supported.

#### SetOff
The method ``SetOff()`` sets the LED to a static ``off`` operating state. In case of any errors, no change of the LED state takes place.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The Fb is not in the Open (=Enabled) state ============= ====================================================================================== |

#### SetOn
The method ``SetOn()`` switches the LED to a device specific color which is guaranteed to be visible.

This method is similar to ``setStatic()``, but it guarantees that the LED will turn on in some default color. When using ``setStatic()`` in contrast, the user may select the color, but the LED will not turn on if he selects a color which cannot be displayed (e.g. ``blue`` on a red-green-LED). .. note:: Which color is used as default color depends on the target hardware and on the type of the LED. It is hardcoded in the target depending internal libraries and cannot be changed by the user. It is ensured that the default color is visible for the addressed target hardware. On error, no change of the LED state takes place.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The FB is not in the Open (=Enabled) state ============= ====================================================================================== |

#### SetBlink
The method ``SetBlink()`` makes the LED toggle periodically between two colors.

In the beginning, ``eColor1`` is displayed for the duration ``tTime1``. After that on-time has elapsed, the second color (``eColor2``) appears for a duration of ``tTime2``. After that second time, this process repeats with ``eColor1``. .. figure:: ../../Images/__diag_ledblink.png :align: center :alt: Timing Diagram On error, no change of the LED state takes place.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The Fb is not in the Open (=Enabled) state EBADR Requested Color is not supported EINVAL invalid parameters ============= ====================================================================================== |

#### SetFlash
The method ``SetFlash()`` displays a color for a short time and displays a second color statically afterwards.

The color of this 'flash' is given by ``eColor1`` and its duration is given by ``tFlashTime``. After ``tFlashTime`` has elapsed, the LED displays the other color ``eColor2`` (which may be a visible color as well as simply ``off``). .. figure:: ../../Images/__diag_ledflash.png :align: center :alt: Timing Diagram While the first phase of the flash is in progress, the ``xBusy``-Output of the FB is ``TRUE``. When applying this function while the LED is still 'flash'ing, the flash time will be retriggered. When the flash time is expired, the LED transits into the ``static`` mode. .. note:: Some legacy libraries require the LED to be driven into in certain other operating modes (namely 'static') before the LED could be driven to flash mode. This FB, however, has no such restriction. On error, no change of the LED state takes place.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The Fb is not in the Open (=Enabled) state EBADR Requested Color is not suported EINVAL Invalid parameters ============= ====================================================================================== |

#### SetStatic
The method ``SetStatic()`` makes the LED continuosly display a given color or switches the LED off.

If the requested color is not supported by the hardware, this method fails with ``EBADR`` ('Bad Request'); On error, no change of the LED state takes place.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The Fb is not in the Open (=Enabled) state EBADR Requested Color is not suported EINVAL invalid arguments ============= ====================================================================================== |

## Data Types

### typLedSequenceStep
Structure type.

One step of a sequence of blink codes. *Context:* An array of variables of this type will be passed to the FB when a sequence of flashes is started (:ref:`SetSequence <FbAppLED.SetSequence>`). The length of the sequence will be passed in an extra ``UDINT``. As an additional feature, a duration time of ``T#0s`` in a ``typLedSequenceStep`` will also denote the end of the sequence.

### eLedMode
Enumeration type.

This enumeration reflects the operating mode, which an LED is in according to the ``SetXxxx()``-method.

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

