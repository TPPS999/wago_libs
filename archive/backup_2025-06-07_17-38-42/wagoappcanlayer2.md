# WagoAppCanLayer2 v1.6.1.5

## Overview
WAGO PLC library providing WagoAppCanLayer2 functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbCanRxTotal_29Bit
This function block allows to receive all CAN messages with 29-Bit identifier.

**Description:**
In contrast to FbCanRx29BitFrameAll this function block uses an array for the data to be displayed. The parameter ``CAN_RX_BUFFER_MAX`` from the |ParameterList| allows to adjust the space within the array.

### FbCanRxTotal_11Bit
This function block allows to receive all CAN messages with 11-Bit identifier.

**Description:**
In contrast to FbCanRx11BitFrameAll this function block uses an array for the data to be displayed. The parameter ``CAN_RX_BUFFER_MAX`` from the |ParameterList| allows to adjust the space within the array.

### FbCanRx29BitFrameAll
This function block allows to receive any CAN messages with 11-Bit and 29-Bit identifier.

**Description:**
Either this function block is used or FbCanRx29BitFrame. It is not allowed to use both at the same time.

### FbCanRx11BitFrameAll
This function block allows to receive any CAN messages with 11-Bit identifier. 29-Bit frames are discarded by function block.

**Description:**
Either this function block is used or FbCanRx11BitFrame. It is not allowed to use both at the same time.

### FbCanSetLed
This function block allows to set LEDs on the onboard Can port.

**Description:**
This function block is not supported by the can gateway module 750-658.

### FbCanL2Reset
This function block performs a reset on the Can port if in layer2 mode and resets the error counters

### FbCanL2Close
This function block will close the CAN port in layer2 mode.

**Description:**
If the configuration values, e.g. the baudrate has to be changed, once the Can bus is already started the following steps need to be performed. Disable function block FbCanOpen if used with 750-658. Enable FbCanClose and wait for output done. Then disable FbCanClose. Now the system is prepared to take new values.

### FbCanL2Open
This function block opens a CAN port in layer2 mode and configures at least the CAN baudrate

**Description:**
1) Onboard port is used as CAN layer2 Device This block is optional, since the integrated CAN configurator already opens the port. Input ``dwFlags``: not supported Input ``dwPara``: not supported 2) Module 750-658 is used Input ``dwFlags`` .0: Enable the following bits .1 -.3: 0: Set module mode to mapped mode 1: Set module mode to transparend mode 2: Set module mode to sniffer mode 3: Spare 7: Spare .4: Enable 29-bit COB-IDs .5: Enable SDO transmission over acyclic channel .6: Enable diagnosis over acyclic channel .7 - .31 Spare The bits in dwFlags will only be evaluated by the open function, if the first bit is TRUE. Input ``dwPara``: not supported

### FbCanErrorInfo
This function block shows CAN bus information such as bus off errors or other general status details.

### FbCanTx29BitFrame
This function block allows to transmit a CAN messages with a defined CAN ID. This block supports 29-Bit CAN IDs.

**Description:**
If oStatus shows ``ErrorMode`` then function block FbCanL2Open is disabled.

### FbCanTx11BitFrame
This function block allows to transmit a CAN messages with a defined CAN ID. This block supports only 11 Bit CAN IDs.

**Description:**
If oStatus shows ``ErrorMode`` then function block FbCanL2Open is disabled.

### FbCanRx29BitFrame
This function block allows to receive CAN messages with a defined CAN ID. This block supports 11-Bit and 29-Bit identifier.

### FbCanRx11BitFrame
This function block allows to receive CAN messages with a defined CAN ID. This block supports only 11 Bit CAN IDs.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbCanRxTotal_29Bit: FbCanRxTotal_29Bit;
END_VAR

// Basic function block usage
fbFbCanRxTotal_29Bit(
    // Configure inputs as needed
);

// Check status
IF fbFbCanRxTotal_29Bit.xValid THEN
    // Operation successful
END_IF

IF fbFbCanRxTotal_29Bit.xError THEN
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

