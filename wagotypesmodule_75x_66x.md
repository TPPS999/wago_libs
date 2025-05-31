# WagoTypesModule_75x_66x v1.0.1.2

## Overview
WAGO PLC library providing WagoTypesModule_75x_66x functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Data Types

### eState_iParameter
Enumeration type.

### eProtocol_iParameter
Enumeration type.

### eVI
Enumeration type.

### eLogicFunction
Enumeration type.

### eInputFilterTime
Enumeration type.

### eInputDiscepancyTime
Enumeration type.

### eReadBackTime
Enumeration type.

### eTestPulseDuration
Enumeration type.

### eInputSignal
Enumeration type.

### eParameterType
Enumeration type.

### eParameterOffset
Enumeration type.

### eErrorSource
Enumeration type.

### eErrorType
Enumeration type.

### eActiveDischarge
Enumeration type.

### eWireBreakDetection
Enumeration type.

### eTestSequence
Enumeration type.

### eChannelPair
Enumeration type.

### typRawInputChannelPairSettings
Structure type.

### eShortCircuitTest
Enumeration type.

### eRestartInterlock
Enumeration type.

### eOperationMode
Enumeration type.

### ePreEvaluation
Enumeration type.

### typRawOutputChannelSettings
Structure type.

### typRawInputChannelSettings
Structure type.

### typModuleSettings
Structure type.

## Usage Examples

```iec
// Basic usage example
// Refer to function block documentation for specific usage
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

