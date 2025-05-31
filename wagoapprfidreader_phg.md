# WagoAppRFIDReader_phg v1.0.3.3

## Overview
WAGO PLC library providing WagoAppRFIDReader_phg functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbPhgKeypadInput
This function block send command "TASTATUR_INPUT (0x54)" Mit diesem Kommando kann eine Tastatur Eingabe vom Slave angefordert werden. Falls die Eingabe nicht innerhalb des Timeout beendet wird, wird eine Tastaturtimeout Meldung an den Master gesendet. Nach dem Kommando wartet der Slave entsprechend auf die Tastatureingabe, die Daten, bzw. Statusmeldungen werden dann als Polling Antwort an den Master gesendet. Status falls keine Tastatur vorhanden ist : 0x3F Status falls die Parameter nicht korrekt sind : 0x47 For this the application have to fill the struct utKeypadFunction. +---------------+-------------------+--------------------------------------------------------+ | Name | Value(s) | Description | +===============+===================+========================================================+ | bCommand | 16#54 | command "TASTATUR_INPUT (0x54)" | +---------------+-------------------+--------------------------------------------------------+ | bKeyCount | 1...7 | Number of keys to read | +---------------+-------------------+--------------------------------------------------------+ | bTimeout | 16#00 | Timeout(Default) start with first key | | +-------------------+--------------------------------------------------------+ | | 1..255 | Timeout in seconds after execution | +---------------+-------------------+-------------+-----------------+------+-----------------+ | bInputCtrl | bitcoded | Bit 8/7 | Always | 00 | fix | | | +-------------+-----------------+------+-----------------+ | | | Bit 6/5 | Keypad-Layout | 00 | Telefon | | | | | +------+-----------------+ | | | | | 01 | PC | | | | | +------+-----------------+ | | | | | 10 | Scramble | | | +-------------+-----------------+------+-----------------+ | | | Bit 4 | Scramble-Mode | 0 | Enable | | | | | +------+-----------------+ | | | | | 1 | Standby | | | +-------------+-----------------+------+-----------------+ | | | Bit 3 | Always | 00 | fix | | | +-------------+-----------------+------+-----------------+ | | | Bit 2 | Scramble-Mode | 0 | Imidiedly Enable| | | | | +------+-----------------+ | | | | | 1 | Standby | | | +-------------+-----------------+------+-----------------+ | | | Bit 1 | Send keys | 0 | On key Count | | | | | +------+-----------------+ | | | | | 1 | After key "E" | +---------------+-------------------+-------------+-----------------+------+-----------------+ | bDisplayCtrl | bitcoded | Bit 8..5 | LedDisplay | 0000 | Toggle GREN/RED | | | | | +------+-----------------+ | | | | | 0001 | Toggle GREEN | | | +-------------+-----------------+------+-----------------+ | | | Bit 4/3 | Backlight | 00 | OFF | | | | | +------+-----------------+ | | | | | 11 | Max. ON | | | +-------------+-----------------+------+-----------------+ | | | Bit 2 | Display | 0 | OFF | | | | | +------+-----------------+ | | | | | 1 | On first key | | | +-------------+-----------------+------+-----------------+ | | | Bit 1 | Optical signal | 0 | OFF | | | | | +------+-----------------+ | | | | | 1 | ON | +---------------+-------------------+-------------+-----------------+------+--+--------------+ | bFeedbackKey | bitcoded | Bit 8..3 | Always | 0000000 | fix | | | +-------------+-----------------+------+--+--------------+ | | | Bit 2 | Optical signal | 0 | OFF | | | | | +------+-----------------+ | | | | | 1 | ON | | | +-------------+-----------------+------+-----------------+ | | | Bit 1 | Akustic signal | 0 | OFF | | | | | +------+-----------------+ | | | | | 1 | ON | +---------------+-------------------+-------------+-----------------+------+-----------------+ .. note:: You should always call this FB cyclic.

### FbPhgSetRelais
This function block controls the relais on "DI/DO-Box"

### FbSimpleReader
This function block provides a simple basic handling for a VOXIO-Reader. .. note:: You need one instance of this fb for each reader and you should call this instance cyclic.

### FbPhgCryptComObject
Communication object for serial base communication with a phg reader. You need this object once for each serial line for use at many |FbSimpleReader|.

### FbPhgReadHwInfo
This function block polls a reader and take data from the reader if there data availble. The data have to interpret by the application. The struct component ``utData.eDataType`` gives information about the type of data.

### FbPhgGetTagData
This function block observes the ``utPollData`` and if it is possible, it converts it to ``utTagData``. So you can use the output ``xDone`` from |FbPhgPoll| to connect the input ``xExecute``. In this case the output ``xDone`` from this function block goes to TRUE when tag data available.

### FbPhgPoll
This function block polls a reader and take data from the reader if there data availble. The data have to interpret by the application. The struct component ``utData.eDataType`` gives information about the type of data.

### FbPhgUserInterface
This function block controls the beeper and the LEDs of the reader. For this the application have to fill the struct utLedFunction. +---------------+-------------------+--------------------------------------------------------+ | Struct | Component | Description | +===============+===================+========================================================+ | utLedFunction | bCommand | for internal use only | | +-------------------+--------------------------------------------------------+ | | | | +-------------------+--------------------------------------------------------+ | | |

### FbPhgFastPoll
Fast Poll is used for ask the reader whether data available. If data available the output ``xDataPresent`` will be TRUE until the start of the next poll. In this case call the |FbPhgPoll| for fetch the data from the reader. .. note:: You should always call this FB cyclic.

### FbPhgCryptCom
Communication object for serial base communication with a phg reader. .. note:: You should always call this FB cyclic.

**Methods:**

#### isPackageComplete
#### FindFirstByte
#### RemoveFromBuffer
### FbPhgReset
Hardware Reset .. note:: You should always call this FB cyclic.

### FbPhgSetParameter
Write the parameter code to reader. You can generate the parameter code as string with the manufacturer tool

## Data Types

### typKeypadFunction
Structure type.

### typRelaisFunction
Structure type.

### typLedFunction
Structure type.

### ePollDataType
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbPhgKeypadInput: FbPhgKeypadInput;
END_VAR

// Basic function block usage
fbFbPhgKeypadInput(
    // Configure inputs as needed
);

// Check status
IF fbFbPhgKeypadInput.xValid THEN
    // Operation successful
END_IF

IF fbFbPhgKeypadInput.xError THEN
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

