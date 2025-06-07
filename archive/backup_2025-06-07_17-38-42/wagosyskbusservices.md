# WagoSysKbusServices v2.0.2.3

## Overview
WAGO PLC library providing WagoSysKbusServices functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbTerminalScanner
**Methods:**

#### EventCallback
#### BuildTerminalList
Inits the TerminalManager and reads out the node configuration of all available terminals. .. note:: This method will be called automaticly by a daemon.

#### getTerminalByType
If the wanted terminal exist it returns an interface reference to the wanted terminal otherwise it returns 0. usiIndex specifies the number of the amount terminals with the specified terminal type. Different terminal types my combined with or

#### getTerminalBySlotNo
If the wanted terminal exist it returns an interface reference to the wanted terminal otherwise it returns 0.

#### getTerminalByOrderNumber
This method returns an interface reference of a kbus module (terminal) specified by ``usiIndex`` and ``sPattern``. The index indicates the number of terminal in the amount of terminals that match the given pattern. If no specified terminal exist it returns 0.

#### getTerminalById
If the wanted terminal exist it returns an interface reference to the wanted terminal otherwise it returns 0. usiIndex specifies the number of the amount terminals with the specified udiId.

#### getTerminalQuantityByType
returns the quantity of existing terminals with the wanted type. Different terminal types my combined with or

#### getTerminalQuantityByOrderNumber
returns the quantity of existing terminals that match the pattern

#### getTerminalQuantityById
returns the quantity of existing terminals with the wanted id

#### getTerminalQuantity
returns the quantity of all scanned terminals

#### getChannelQuantityByType
returns the quantity of all existing channels with the wanted type. Different terminal types my combined with or

### FbKbusTerminalData
### FbKbusService
**Methods:**

#### WriteParameterList
| Write the value``uiValue`` at terminal parameter specified by ``usiParameterNo``.

#### ReadParameterList
| Read a terminal parameter specified by ``usiParameterNo``.

#### WriteParameter
| Write the value``uiValue`` at terminal parameter specified by ``usiParameterNo``.

#### ReadParameter
| Read a terminal parameter specified by ``usiParameterNo``.

#### WriteRegister
| Write the value``uiValue`` at terminal register specified by ``usiChannel`` and ``usiRegisterNo``.

#### SetRegisterFillBytes
#### ReadRegister
| Read a terminal register specified by ``usiChannel`` and ``usiRegisterNo``.

#### GetRegisterFillBytes
Get Quantity of used fillbytes betwen C/S and VALUE for register communication

#### isReadyForUse
#### GetSlotNumber
returns the slot number for this service

#### GetBusType
returns always WagoTypesBusServices.eBusType.KBUS

### FbKbusParameterService
**Methods:**

#### WriteParameterList
| Write the value``uiValue`` at terminal parameter specified by ``usiParameterNo``.

#### ReadParameterList
| Read a terminal parameter specified by ``usiParameterNo``.

#### WriteRegister
| Write the value``uiValue`` at terminal register specified by ``usiChannel`` and ``usiRegisterNo``.

#### SetRegisterFillBytes
#### ReadRegister
| Read a terminal register specified by ``usiChannel`` and ``usiRegisterNo``.

#### GetRegisterFillBytes
Get Quantity of used fillbytes betwen C/S and VALUE for register communication

#### WriteParameter
| Write the value``uiValue`` at terminal parameter specified by ``usiParameterNo``.

#### ReadParameter
| Read a terminal parameter specified by ``usiParameterNo``.

#### isReadyForUse
#### GetSlotNumber
returns the slot number for this service

#### GetBusType
returns always WagoTypesBusServices.eBusType.KBUS

## Data Types

### getTerminalByType
If the wanted terminal exist it returns an interface reference to the wanted terminal otherwise it returns 0. usiIndex specifies the number of the amount terminals with the specified terminal type. Different terminal types my combined with or

### getTerminalQuantityByType
returns the quantity of existing terminals with the wanted type. Different terminal types my combined with or

### getChannelQuantityByType
returns the quantity of all existing channels with the wanted type. Different terminal types my combined with or

### GetBusType
returns always WagoTypesBusServices.eBusType.KBUS

### GetBusType
returns always WagoTypesBusServices.eBusType.KBUS

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbTerminalScanner: FbTerminalScanner;
END_VAR

// Basic function block usage
fbFbTerminalScanner(
    // Configure inputs as needed
);

// Check status
IF fbFbTerminalScanner.xValid THEN
    // Operation successful
END_IF

IF fbFbTerminalScanner.xError THEN
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

