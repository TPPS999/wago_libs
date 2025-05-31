# WagoSysVirtualBuffer v1.6.1.0

## Overview
WAGO PLC library providing WagoSysVirtualBuffer functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbVirtualReadBuffer_base
**Methods:**

#### protRead
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENODATA no data in buffer EINVAL null-pointer or size <2 or size >2G ============= ====================================================================================== |

#### protAcquireData
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | received data ENODATA no data available others: specific error messages ============= ====================================================================================== |

#### ReadOut
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | complete success EINVAL invalid call parameters (null-pointer or size>2G) EBUSY new data cannot be accepted. EACCES processing returned with EINVAL or EBUSY or FIFO is not operational ENOSYS There is no method 'protProcessDataOut' specified. others: specific error messages ============= ====================================================================================== |

#### CyclicService
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, data transferred ENODATA there is no data in the FB others specific error messages ============= ====================================================================================== |

#### privAcquireDataWrapper
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | all data successfully processed EWOULDBLOCK not all data could be processed, but no further errors ERANGE process returned more processed bytes than fed in others: specific error messages ============= ====================================================================================== |

#### AttachBuffer
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EINVAL Null-pointer or size <2 or size >2G ============= ====================================================================================== |

#### Clear
#### ReAttachBuffer
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EINVAL Invalid parameters (size beyond plausibility). EFBIG New buffer is too small for data which is already contained in the previous buffer. ============= ====================================================================================== |

#### Initialize_base
### FbVirtualWriteBuffer_base
**Methods:**

#### privProcessDataWrapper
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | all data successfully processed EWOULDBLOCK not all data could be processed, but no further errors ERANGE process returned more processed bytes than fed in others: specific error messages ============= ====================================================================================== |

#### ReAttachBuffer
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EINVAL Invalid parameters (size beyond plausibility). EFBIG New buffer is too small for data which is already contained in the previous buffer. ============= ====================================================================================== |

#### Initialize_base
#### AttachBuffer
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EINVAL Null-pointer or size <2 or size >2G ============= ====================================================================================== |

#### CyclicService
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | complete success EWOULDBLOCK there is still data in the FB others specific error messages ============= ====================================================================================== |

#### Clear
#### protProcessData
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | all data successfully processed EWOULDBLOCK not all data could be processed, but no further errors others: specific error messages ============= ====================================================================================== |

#### FillIn
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | complete success EINVAL invalid call parameters (null-pointer or size>2G) EBUSY new data cannot be accepted. EACCES processing returned with EINVAL or EBUSY or FIFO is not operational ENOSYS There is no method 'protProcessDataOut' specified. others: specific error messages ============= ====================================================================================== |

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbVirtualReadBuffer_base: FbVirtualReadBuffer_base;
END_VAR

// Basic function block usage
fbFbVirtualReadBuffer_base(
    // Configure inputs as needed
);

// Check status
IF fbFbVirtualReadBuffer_base.xValid THEN
    // Operation successful
END_IF

IF fbFbVirtualReadBuffer_base.xError THEN
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

