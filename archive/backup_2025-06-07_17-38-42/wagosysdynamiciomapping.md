# WagoSysDynamicIoMapping v1.0.4.4

## Overview
WAGO PLC library providing WagoSysDynamicIoMapping functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbModule_75x_677
### FbModule_75x_67x
### FbModule_75x_645
### FbModule_750_636
### FbModule_75x_633
### FbModule_75x_511
### FbModule_75x_493
### FbOutputChannelSubsetByType
Build a subset of output channels from all actual placed modules specified by the constructor with a type. Different terminal types may combined with 'OR'

### FbOutputChannelSubsetByFilter
Build a subset (collection) of output channels from all actual placed modules specified by the constructor with a filter. Filter is a list of pattern seperated by ',' or ';'

### FbInputChannelSubsetByFilter
Build a subset (collection) of input channels from all actual placed modules specified by the constructor with a filter. Filter is a list of pattern seperated by ',' or ';'

### FbInputChannelSubsetByType
Build a subset of input channels from all actual placed modules specified by the constructor with a type. Different terminal types may combined with 'OR'

### FbModuleSubsetByType
Build a subset of modules from all actual placed modules specified by the constructor with a type. Different terminal types may combined with 'OR'

### FbModuleSubsetByFilter
Build a subset (collection) of modules from all actual placed modules specified by the constructor with a filter. Filter is a list of pattern seperated by ',' or ';'

## Data Types

### FbOutputChannelSubsetByType
Build a subset of output channels from all actual placed modules specified by the constructor with a type. Different terminal types may combined with 'OR'

### FbInputChannelSubsetByType
Build a subset of input channels from all actual placed modules specified by the constructor with a type. Different terminal types may combined with 'OR'

### FbModuleSubsetByType
Build a subset of modules from all actual placed modules specified by the constructor with a type. Different terminal types may combined with 'OR'

### getModuleByType
This method returns an Interface of an object from aIModules[] specified by ``usiNumber`` and ``eType``. The ``usiNumber`` indicates the number of module in the amount of modules that match the given type. Different terminal types may combined with or

### getModuleIndexByType
This method returns the index at aIModules[] from the module specified by ``usiNumber`` and ``eType``. The ``usiNumber`` indicates the number of module in the amount of modules that match the given type. Different terminal types may combined with or

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbModule_75x_677: FbModule_75x_677;
END_VAR

// Basic function block usage
fbFbModule_75x_677(
    // Configure inputs as needed
);

// Check status
IF fbFbModule_75x_677.xValid THEN
    // Operation successful
END_IF

IF fbFbModule_75x_677.xError THEN
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

