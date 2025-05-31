# WagoSysFileDir_Internal_PFC v1.1.1.2

## Overview
WAGO PLC library providing WagoSysFileDir_Internal_PFC functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSysFsInternal
**Methods:**

#### Stat
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success ENOSYS This functionality is not supported by the target hardware ENOENT The requested file or directory does not exist. ENOTDIR The requested file could not be accessed directly as file and could also not be accessed as directory EACCES Other problems ============= ===================================================================================== |

#### MoveAllFilesInDirectory
#### RemoveDirectoryWithContents
**Result Codes:**
| Code | Description |
|------|-------------|
| ENOSYS | This functionality is not supported by the target hardware EBUSY The directory to be removed is currently in use by the system. ENOTEMPTY The path argument names a directory that is not an empty directory. ENAMETOOLONG The length of the path argument or one of its components exceeds the size limit ENOTDIR A component of path is not a directory. EROFS The directory entry to be removed resides on a read-only file system. ============= ===================================================================================== |

#### ReadFirstEntryInDirectory
#### MoveFile
**Result Codes:**
| Code | Description |
|------|-------------|
| ENOSYS | This functionality is not supported by the target hardware EINVAL Invalid arguments (e.g. empty pathes) ENOENT Source File does not exist EISDIR Source File is a directory EBUSY The directory to be removed is currently in use by the system. ENOTEMPTY The path argument names a directory that is not an empty directory. ENAMETOOLONG The length of the path argument or one of its components exceeds the size limit ENOTDIR A component of path is not a directory. EROFS The directory entry to be removed resides on a read-only file system. ETIME Timeout ============= ===================================================================================== |

#### CheckDirectoryExists
#### CheckFileExists
#### GetFreeSpaceInDirectory
#### NormalizeCanonicalFilename
#### NormalizeCanonicalPath
#### MakeDirectory
#### ChangeWorkingDirectory
#### RemoveEmptyDirectory
**Result Codes:**
| Code | Description |
|------|-------------|
| ENOSYS | This functionality is not supported by the target hardware EBUSY The directory to be removed is currently in use by the system. ENOTEMPTY The path argument names a directory that is not an empty directory. ENAMETOOLONG The length of the path argument or one of its components exceeds the size limit ENOTDIR A component of path is not a directory. EROFS The directory entry to be removed resides on a read-only file system. ETIME Timeout ============= ===================================================================================== |

#### Rename
**Result Codes:**
| Code | Description |
|------|-------------|
| ENOSYS | This Functionality is not supported by the target hardware EINVAL Invalid sourcename EEXIST File or dir exists and may not be overwritten EISDIR the file to be overwritten is a directory ENOTDIR the directory to be overwritten is a file EBUSY The rename fails because oldpath or newpath is a directory that is in use by some process. EINVAL The new STRING contained a path prefix of the old one. ENAMETOOLONG Oldpath or newpath were too long. ENOENT Oldpath does not exist, or a directory component in newpath does not exist or the name is empty. ENOSPC The device containing the file has no room for the new directory entry. ENOTDIR A component used as a directory in oldpath or newpath is not, in fact, a directory. ENOTEMPTY Newpath is a nonempty directory, that is, contains entries other than "." and " |

#### SetAttributes
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success ENOSYS This Functionality is not supported by the target hardware ENOENT File does not exist EPERM Attributes cannot be manipulated ============= ====================================================================================== |

#### RemoveFile
#### MoveDirectory
**Result Codes:**
| Code | Description |
|------|-------------|
| ENOSYS | This functionality is not supported by the target hardware EBUSY The directory to be removed is currently in use by the system. ENOTEMPTY The path argument names a directory that is not an empty directory. ENAMETOOLONG The length of the path argument or one of its components exceeds the size limit ENOTDIR A component of path is not a directory. EROFS The directory entry to be removed resides on a read-only file system. ETIME Timeout ============= ===================================================================================== |

#### RemoveAllFilesInDirectory
#### TranslateNormalizedUrlToSpecific
#### CopyFile
### FbSysDirInternal
**Methods:**

#### Close
#### Read
#### Open
## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSysFsInternal: FbSysFsInternal;
END_VAR

// Basic function block usage
fbFbSysFsInternal(
    // Configure inputs as needed
);

// Check status
IF fbFbSysFsInternal.xValid THEN
    // Operation successful
END_IF

IF fbFbSysFsInternal.xError THEN
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

