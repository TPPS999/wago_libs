# WagoAppColorConverter v1.0.1.6

## Overview
WAGO PLC library providing WagoAppColorConverter functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbColorMixer
The FbColorMixer function block is used for setting the color of an RGB light. Color mixer

**Description:**
The respective color components are specified by the ``bRed``, ``bGreen`` and ``bBlue`` inputs. The values are transmitted to ``typRGB`` by a rising edge at the ``Write`` input. If the ``AutoWrite`` input variable is set to TRUE, the inputs ``bRed``, ``bGreen`` and ``bBlue`` are monitored for value shifting. As soon as a value changes, it is transmitted to ``typRGB``. The color is displayed at the ``dwColour`` output. Representation is as a hexadecimal character in the order B (Blue) G (Green) R (Red). Yellow, for example, in this form has the value 16#00FFFF and white the value 16#FFFFFF.

### FbCalculateStepFader
This function calculates step fader

### FbSaveColorPalette
Ten (10) color palettes can be stored using the FbSaveColorPalette function block.

**Description:**
The respective color palette can be configured via the ``bRed``, ``bGreen`` and ``bBlue`` inputs. At a rising edge at the ``xColour_1`` to ``xColour_10`` inputs, the color palette is saved in the corresponding element of the ``atypRGB`` array. Using a rising edge at the ``xReset`` input, the contents of the ``atypRGB`` array can be deleted. The color is displayed at the ``dwColour`` output. Representation is as a hexadecimal character in the order B (Blue) G (Green) R (Red). Yellow, for example, in this form has the value 16#00FFFF and white the value 16#FFFFFF. The current color index is displayed at the ``bIndex`` output. .. note:: The variables at the ``atypRGB`` input should be declared as RETAIN PERSISTENT so that the list of color palettes is retained after a controller reset and after a download.

### FbSEQ_GEN
function block for generating some periodic functions. Taken from util.lib

### FbChaser
The FbChaser function block copies the chaser value for a channel (A) to a different chase (B) for a given number of chase channels. The value for channel (A) is then reset to zero. A chaser effect can be created using this function.

**Description:**
The function block is activated via the ``xEnable`` variable. The chaser can be stopped using the ``xPause`` variable. The chaser value to be copied is configured at the ``bChaserValue`` input. The chaser channel for which the copying process is to be started is assigned at the ``iStartChannel`` input. Copying of the chaser value is ended at the ``iEndChannel`` channel. The ``iOffset`` variable defines the increment for copying to a different channel. The ``tDelay`` delay period indicates the delay or waiting period between each step. Using a rising edge at the ``xReset`` input, the contents of the ``abChaserChannel`` array can be deleted. The current chaser channel index is displayed at the ``iChannel`` output.

### FbColorCrossFader
A cross fade sequence can be generated using the FbColorCrossFader function block. Cross fade up to 10 Colors. The sequence can be run in two ways namely: #. Repeat: the sequence of Colors repeats itself #. to and fro: the sequence of Colors moves to and fro

**Description:**
The sequence is activated via the ``xEnable`` input. Cross fading between the sequences is defined by the ``tFadeTime`` delay time. The hold time of the recalled color is assigned at the ``tHoldTime`` input. The fade sequence colors can be configured via the ``typColour_1`` to ``typColour_10`` inputs. The number of fade sequence colors is defined at the ``iNumberOfColours`` input. A TRUE signal at the ``xToAndFro`` input activates a cross fade sequence that runs continuously back and forth. A FALSE must be configured at the input if the fade sequence is to start over from the beginning when a maximum number of fade sequence colors is reached. The color is displayed in the ``typRGB`` variable. The current color index is displayed at the ``iIndex`` output.

### FbFadeGenerator
A light scene can be generated using the FbFadeGenerator function block. This function block generates fade value.

**Description:**
The function block is activated via the ``xEnable`` variable. The ``tPeriod`` input defines the duration of the light scene. The ``bMaximumValue`` defines the maximum achievable value for the light scene. If one of the following variables is set to TRUE, the corresponding function is generated: #. Triangle #. Square #. Sawtooth rise #. Sawtooth fall

### FbColorFader
Color fader for single RGB Color

### FbRecallColorPalette
Using the FbRecallColorPalette function block, stored color palettes can be called from the ``atypRGB`` array. Recall up to 10 Colors and assigned its value to addressed RGB.

**Description:**
The ``atypRGB`` input can be linked with the variables of the same name of the FbSaveColourPalette function block and contains the stored color palettes. At a rising edge at the ``xRecallColour_1`` to ``xRecallColour_10`` inputs, the color palettes are called up from the corresponding element of the ``atypRGB`` array. The color is displayed at the ``dwColour`` output. Representation is as a hexadecimal character in the order B (Blue) G (Green) R (Red). Yellow, for example, in this form has the value 16#00FFFF and white the value 16#FFFFFF. The current color index is displayed at the ``bIndex`` output.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbColorMixer: FbColorMixer;
END_VAR

// Basic function block usage
fbFbColorMixer(
    // Configure inputs as needed
);

// Check status
IF fbFbColorMixer.xValid THEN
    // Operation successful
END_IF

IF fbFbColorMixer.xError THEN
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

