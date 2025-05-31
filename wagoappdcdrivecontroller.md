# WagoAppDCDriveController v1.8.1.2

## Overview
WAGO PLC library providing WagoAppDCDriveController functionality.

**Key Features:**
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbControlBasic
This function block handles the DC module 750-636 and its derivates

**Description:**
The function block supports one operation mode at a time, which is either: - speed mode (xMovePos or xMoveNeg) - positioning mode (xTriggerPositioning) - info show error details (xExtendedInfoOn) - read module configuration - write module configuration - restore factory default values - store actual ram values in flash as user data set - restore user data Therefore it is necessary, in case of an error, to deactivate any other mode than info mode. This function block also allows to read and write the module configuration. The input ``xRestoreFactoryDefault`` allows to set the parameters to the factory values. The PWM mode is performed by either ``xMoveNeg`` or ``xMovePos`` . The speed is set by the input ``bMoveSpeed``. This parameter defines the puls duration ratio of the PWM mode. Accelerating from zero to ``bMoveSpeed`` in PWM modes assumes parameter CurrentLimitTime>0. Positioning is started by the input ``xStartPositioning``. The drive will take the input ``diTargetPosition`` as target position. The positioning job is perfomed according to the configuration values. If the positioning job is finished with the actual position within the positioning target window, the function block will reset the variable ``xStartPositioning``. To stop the motor the input ``xStartPositioning`` needs to be false. If ``xEnable`` is reset while the motor is moving in either PWM mode or positioning mode the motor will stop.

### FbPWM
This function block allows velocity control by means of PWM mode

## Data Types

### eStatus
Enumeration type.

### typVisu
Structure type.

### typConfiguration
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbControlBasic: FbControlBasic;
END_VAR

// Basic function block usage
fbFbControlBasic(
    // Configure inputs as needed
);

// Check status
IF fbFbControlBasic.xValid THEN
    // Operation successful
END_IF

IF fbFbControlBasic.xError THEN
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

