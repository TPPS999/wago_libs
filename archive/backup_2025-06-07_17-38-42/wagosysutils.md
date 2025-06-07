# WagoSysUtils v1.5.3.0

## Overview
WAGO PLC library providing WagoSysUtils functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbExclusivityHandler
**Methods:**

#### IsAccessGranted
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, exclusive usage is granted EBUSY Usage is not granted. The device has been attached to another FB already ============= ====================================================================================== |

#### TestExclusivity
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, exclusive usage is granted EUNATCH the device is not attached at all EBUSY Usage is not granted. The device has been attached to another FB already ============= ====================================================================================== |

#### ReleaseExclusivity
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, the device is detached again EBUSY Usage has not been granted to this FB. It is in use by another FB EINVAL Null instance is passed. (Null denotes a detached device) ============= ====================================================================================== |

#### ForceDetachment
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success (this operation does not fail) ============= ====================================================================================== |

#### AttachExclusively
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, exclusive usage is granted EBUSY Usage is not granted. The device has been attached to another user already EINVAL Null instance is passed. (Null denotes a detached device) ============= ====================================================================================== |

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbExclusivityHandler: FbExclusivityHandler;
END_VAR

// Basic function block usage
fbFbExclusivityHandler(
    // Configure inputs as needed
);

// Check status
IF fbFbExclusivityHandler.xValid THEN
    // Operation successful
END_IF

IF fbFbExclusivityHandler.xError THEN
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

