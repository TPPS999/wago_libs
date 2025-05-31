# WagoSysShm_Internal_PFC v1.0.2.3

## Overview
WAGO PLC library providing WagoSysShm_Internal_PFC functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSharedMemory_Internal
**Methods:**

#### OpenByAddress
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENOSYS This functionality is not supported by the target hardware EEXIST The shared memory did exist previously at different physical address EACCES The shared memory object cannot be created ============= ====================================================================================== |

#### OpenByName
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EALREADY FB is already open with compatible parameters (regular operation may carry on) EBUSY FB is already open with incompatible parameters. (usage with old parameters may carry on) EBADSLT Problems with opening existing SHM object EACCES Problems with creating the SHM object. ENOSYS This functionality is not supported by the target hardware ENOENT The shared memory object does not exist and cannot be created EUNATCH The shared memory is expected to be attached and initialized but it was not attached. ENOMEM The requested amount of memory cannot be granted EINVAL Invalid Parameter (e.g. name= is empty or size=0) ============= ====================================================================================== |

#### Close
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENOSYS This functionality is not supported by the target hardware ENOLINK Closing fails due to internal errors (e.g. becatse the object has gone inbetween) EBADF The object is not open ============= ====================================================================================== |

#### GetDataPointer
## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSharedMemory_Internal: FbSharedMemory_Internal;
END_VAR

// Basic function block usage
fbFbSharedMemory_Internal(
    // Configure inputs as needed
);

// Check status
IF fbFbSharedMemory_Internal.xValid THEN
    // Operation successful
END_IF

IF fbFbSharedMemory_Internal.xError THEN
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

