# WagoSysFifo v1.6.1.0

## Overview
WAGO PLC library providing WagoSysFifo functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbFIFO
**Methods:**

#### Initialize
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EINVAL Null-pointer or size <2 or size >2G ============= ====================================================================================== |

#### ReAttachBufferSpace
#### AdvanceWriteIndex
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success ENOSPC More data skipped than contained in the buffer. ============= ====================================================================================== |

#### AdvanceReadIndex
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success ENODATA More data skipped than contained in the buffer. ============= ====================================================================================== |

#### Reset
#### Read
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENODATA no data in buffer EINVAL null-pointer or size <2 or size >2G ============= ====================================================================================== |

#### Write
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENOSPC not enough buffer space available for new data. EINVAL null-pointer or size <2 or size >2G ============= ====================================================================================== |

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbFIFO: FbFIFO;
END_VAR

// Basic function block usage
fbFbFIFO(
    // Configure inputs as needed
);

// Check status
IF fbFbFIFO.xValid THEN
    // Operation successful
END_IF

IF fbFbFIFO.xError THEN
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

