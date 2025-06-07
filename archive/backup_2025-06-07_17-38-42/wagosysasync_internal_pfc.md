# WagoSysAsync_Internal_PFC v1.1.3.4

## Overview
WAGO PLC library providing WagoSysAsync_Internal_PFC functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbAsyncDeferrer
**Methods:**

#### GetRunnerResult
#### RunAsOneShot
#### RunAsDaemon
**Result Codes:**
| Code | Description |
|------|-------------|
| 0=OK | Successful scheduling. ESRCH No such process matching the event specification. EINVAL Invalid combination of input parameters EBUSY The FB is busy with another job which is still active. ECODESYS+X Wago-specific fault (not specified) ============= ====================================================================================== |

#### destroy
#### Remove
**Result Codes:**
| Code | Description |
|------|-------------|
| 0=OK | Success. EBADF The Job handle is invalid. EPIPE The handle does not longer refer to a valid job (broken connection). EBUSY The One-Shot-Job is active and thus will not be attempted to be removed. EPENDING The daemon job is currently running and will be removed after it has finished. ECODESYS+X CoDeSys-specific fault (not specified). ============= ====================================================================================== |

#### Initialize
#### GetState
**Result Codes:**
| Code | Description |
|------|-------------|
| ENOENT | No job to be scheduled, nothing to do. EPENDING The job is waiting for execution. EINPROGRESS The job is running right now. ETERMINATED The job has terminated successfully. EUNSPECIFIC The job terminated with an unspecific error code. ETIMEDOUT The job is timed out (but still running). ECANCELED The job is scheduled for removement. EBADF The FB does not contain a valid handle. ============= ====================================================================================== |

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbAsyncDeferrer: FbAsyncDeferrer;
END_VAR

// Basic function block usage
fbFbAsyncDeferrer(
    // Configure inputs as needed
);

// Check status
IF fbFbAsyncDeferrer.xValid THEN
    // Operation successful
END_IF

IF fbFbAsyncDeferrer.xError THEN
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

