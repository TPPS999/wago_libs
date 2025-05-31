# WagoAppMem v1.6.2.2

## Overview
WAGO PLC library providing WagoAppMem functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSharedMemory_WithReadWrite
Provides rudimentary read-write access to shared memory objects.

**Description:**
This function block provides access to named shared memory objects. This FB is an extension to the base FbSharedMemory function block. It provides read and write access with explicite memory boundary checking. Functions for opening and closing and getting properties are inherited from FbSharedMemory. New methods are: - Read() - ReadByte() - Write() - WriteByte() Note: This FB provides just rudimentary methods and protection for data access in simple data structures. For serious structures, it is strongly recommended to derive more specialized FBs in order to obtain type-safety and more convenience. (For a conceptional example see the description of the parent class :ref:`FbSharedMemory_Base <FbSharedMemory_Base>`.)

**Methods:**

#### Write
Writes into a shared memory ('SHM') block.

A number of *udiTxNBytes* data bytes are taken from the location to which *pTxBuffer* points into the local memory and is written to the position in the Shared-Memory-Object, which is indicated by *udiPosition*. Please note that *pTxBuffer* points directly to the first byte which is transferred.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The FB is not open. EINVAL Invalid parameter ENOSYS This functionality is not supported by the target hardware. EFAULT Adressed memory is out of the range of the shared memory object. EACCES Other errors ============= ================================================================ |

#### WriteByte
Writes a single byte to shared memory ('SHM').

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The FB is not open. ENOSYS This functionality is not supported by the target hardware. EFAULT Adressed memory is out of the range of the shared memory object. EACCES Other errors ============= ================================================================ |

#### ReadByte
Reads a single byte from shared memory ('SHM').

A data byte is read from the SHM from the position indicated by udiPosition. If an error occurs then simply 0 is returned. Note: As a consequence of the intentionally shortened interface, no result code is returned here. If full access to proper error handling is required, then use :: myResult :

#### Read
Reads a block of bytes from the shared memory ('SHM').

A portion of the data is read from the SHM starting from the position indicated by udiPosition. It is stored locally into the address indicated by *pRxBuffer* (without any offsets). *udiRxBufferSize* denotes the number of bytes which is to be transferred. Please note that this is not the size of the whole buffer, but the size of the substructure which is transferred.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The FB is not open. EINVAL Invalid Parameters: destination address or size is 2 Gigabyte or more. ENOSYS This functionality is not supported by the target hardware. EFAULT Adressed memory is out of the range of the shared memory object. EACCES Other errors ============= ====================================================================== |

### FbSharedMemory_Base
Provides base access to named shared memory objects.

**Description:**
Shared memory objects ('SHM') are used for inter process communication (IPC) and can be treated like non-persistent files with non-sequential access. For usage, the user is supposed to derive his own shared memory object from this base class, e.g. as shown below. The parent FB provides the general means for accessing the data, while the inherited FB just adds code for type-safety of the access. (See the example below and for a broader introduction also the :ref:`General <.fld-10 Documentation.doc10_General>` section.) Note (1): There is no use in instantiating this base class directly, because all means for data access are protected. Create derived FBs instead. Note (2): There is a predefined FB :ref:`FbSharedMemory_WithReadWrite <FbSharedMemory_WithReadWrite>` derived form this base which does provide generic access to its data. Due to its genericity, data access has to take place via byte-positions instead of type definitions, so this is only intended either as fallback for simple data structures, such as single bytes or strings, or as base FB itself for deriving more specific FBs. In a typical derivation, shared memory is mapped to existing data structures: :: /////////////////////////////////////////////////////////////////////////// // This is the structure of the data , which is shared by our applictations /////////////////////////////////////////////////////////////////////////// TYPE typMySharedStructure : STRUCT // just an example without use in reality bMyByte : BYTE; MyData : ARRAY [0 .. 19] OF typOtherStructures; END_STRUCT END_TYPE /////////////////////////////////////////////////////////////////////////// // For accessing typified data, we extend the shared memory base FB /////////////////////////////////////////////////////////////////////////// FUNCTION_BLOCK FbMySharedMemory : EXTENDS WagoSysMem.FbSharedMemory_Base; PROPERTY pData : POINTER TO typMySharedStructure pData :

**Methods:**

#### GetDataPointer
Returns the pointer to the shared memory resource.

This function returns a null-pointer if the FB is not open. The pointer is mapped into the address space of the calling application and can be used directly for pointing to structures. .. Note:: As this FB is designed as inheritance base, this method is marked PROTECTED, because under normal circumstances the user is not supposed to access the SHM directly. Instead, for user access, a derived FB is supposed to be defined which provides a proper user interface for the specific data access and uses the pointer only internally. (See :ref:`general description <FbSharedMemory_Base>`)

#### Close
Closes the shared memory object.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success ENOSYS This functionality is not supported by the target hardware. EBADF The object is not open. ============= =========================================================== |

#### OpenByName
Opens the Sharedmemory ('SHM') FB for reading and writing.

``sName:`` System-wide unique name of the SHM resource. (The type definition is given in WagoTypesCommon, essentially this is a sized string.) If a resource with this name does not exist, it will be created unless the flag xAssumeExisting forbids this. Any strings which are valid as filenames would also be valid as memory identifiers. An empty string will result in EINVAL. ``udiSize:`` Required size of the resource. If the requested size cannot be granted, ENOMEM is returned. That may happen either if the resource has to be newly allocated and too little memory is available, or if the resource exists with a smaller size and it cannot be upsized. If a size of 0 or a size of 2 Gigabyte or more is requested, EINVAL is returned. ``xRequireSystemMemory:`` TRUE indicates that the memory is to be shared not only with other IEC-Applications, but also with other independent non-IEC-processes on the PLC. (Visibility to other non IEC-Processes is mandatory.) If no interaction with non-IEC-processes is intended, FALSE should be passed here. If you do not know that to enter here, FALSE is almost certainly the best choice. If this property is requested but cannot be granted, the open() call returns ENOSYS when called with this flag set. *Note (1):* If this flag

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success ENOSYS This functionality is not supported by the target hardware. ENOENT The shared memory object does not exist and cannot be created. EUNATCH No memory is attached to the SHM device but a fully initialized SHM was expected. ENOMEM The requested amount of memory cannot be granted. EINVAL Invalid Parameter (e.g. name='' or size=0) ============= ====================================================================================== |

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSharedMemory_WithReadWrite: FbSharedMemory_WithReadWrite;
END_VAR

// Basic function block usage
fbFbSharedMemory_WithReadWrite(
    // Configure inputs as needed
);

// Check status
IF fbFbSharedMemory_WithReadWrite.xValid THEN
    // Operation successful
END_IF

IF fbFbSharedMemory_WithReadWrite.xError THEN
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

