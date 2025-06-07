# WagoAppSolenoid v1.8.0.8

## Overview
WAGO PLC library providing WagoAppSolenoid functionality.

**Key Features:**
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbConfigurationAndStatus_1632
A function block reading status and diagnosis information from module 750-1632. Additional functionality as reading and writing the configuration is supported.

**Description:**
.. note:: This function block must be used once for each module 750-632 and it must be executed cyclic. Only one job is supported at any time, so either read, write or check configuration.

**Methods:**

#### FullConfig
### FbBasicControl_1632
Control a proportional valve

**Description:**
Each solenoid may be controlled by one function block ``FbBasicControl_1632``. Therefore up to two instances may be needed, if two solenoids are connected. A teach in procedure must be done once to adjust the internal settings according to the connected valve.

### FbConfigurationAndStatus
A function block reading status and diagnosis information from module 750-632. Additional functionality as reading and writing the configuration is supported.

**Description:**
.. note:: This function block must be used once for each module 750-632 and it must be executed cyclic. Only one job is supported at any time, so either read, write or check configuration.

**Methods:**

#### FullConfig
### FbBasicControl
Control a proportional valve

**Description:**
Each solenoid may be controlled by one function block ``FbBasicControl``. Therefore up to two instances may be needed, if two solenoids are connected.

## Data Types

### eStatus
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbConfigurationAndStatus_1632: FbConfigurationAndStatus_1632;
END_VAR

// Basic function block usage
fbFbConfigurationAndStatus_1632(
    // Configure inputs as needed
);

// Check status
IF fbFbConfigurationAndStatus_1632.xValid THEN
    // Operation successful
END_IF

IF fbFbConfigurationAndStatus_1632.xError THEN
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

