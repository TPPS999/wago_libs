# WagoSysFileDir_Internal_PFC v1.1.1.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysFileDir_Internal_PFC
- **Version:** 1.1.1.2
- **Categories:** WAGO Internal|Target|PFC
- **Namespace:** WagoSysFileDirInternal
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated.

Target specific FileDir library for PFC

This document is automatically generated. Target specific FileDir library for PFC

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks FbSysDirInternal (FB) - FbSysFsInternal (FB) - fbExclusiveFileHandling (FB) - fbSysFileInternal (FB) Functions - ObsWrappedSysFileGetSize (FUN) - ObsWrappedSysFileGetTime (FUN) - SysCheckDirectoryExists (FUN) - SysCheckFileExists (FUN) - SysExt_FileGetStat (FUN) - SysExt_GetFreeSize (FUN) Methods - FbSysDirInternal.Close (METH) - FbSysDirInternal.Open (METH) - FbSysDirInternal.Read (METH) - FbSysFsInternal.ChangeWorkingDirectory (METH) - FbSysFsInternal.CheckDirectoryExists (METH) - FbSysFsInternal.CheckFileExists (METH) - FbSysFsInternal.CheckSDCardStatus (METH) - FbSysFsInternal.CopyFile (METH) - FbSysFsInternal.GetFreeSpaceInDirectory (METH) - FbSysFsInternal.MakeDirectory (METH) - ... and 26 more Program Organization Internal Components - 90 Internal - FbSysDirInternal.EofReached (PROP) - FbSysDirInternal.IsOpen (PROP) - FbSysDirInternal.LastResult (PROP) - FbSysFsInternal.LastResult (PROP) - FbSysFsInternal.WorkingDirectory (PROP) - WagoSysFileDir_Internal_PFC Library Documentation - fbSysFileInternal.EofReached (PROP) - fbSysFileInternal.IsOpen (PROP) - fbSysFileInternal.IsReadable (PROP) - ... and 4 more Global Variable Lists - GVL (GVL) - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components - 91 TSC - eFileType (ENUM) - typFileStat (STRUCT)

### Indices and tables ¶


Based on WagoSysFileDir_Internal_PFC.library, last modified 29.05.2024, 19:51:33. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysFileDir_Internal_PFC.library, last modified 29.05.2024, 19:51:33. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysFileDir_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:51:34 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:51:33 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysFileDirInternal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysFileDir_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.1.1.2 |
| Title | string | WagoSysFileDir_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysDir Library Identification : Placeholder: SysDir Default Resolution: SysDir, * (System) Namespace: SysDir Library Properties : SysFile Library Identification : Placeholder: SysFile Default Resolution: SysFile, * (System) Namespace: SysFile Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysFileDir_Internal_Common Library Identification : Placeholder: WagoSysFileDir_Internal_Common Default Resolution: WagoSysFileDir_Internal_Common, * (WAGO) Namespace: WagoSysFileDirInternalCommon Library Properties : WagoSysFileDir_Internal_ITF Library Identification : Placeholder: WagoSysFileDir_Internal_ITF Default Resolution: WagoSysFileDir_Internal_ITF, * (WAGO) Namespace: WagoSysFileDir_Internal_ITF Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : Library Parameter : Parameter: MAX_STRING_LENGTH = 255 Parameter: MAX_WSTRING_LENGTH = 255 WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Function Blocks


## FbSysDirInternal (FB)


- FbSysDirInternal.Close (METH) - FbSysDirInternal.EofReached (PROP) - FbSysDirInternal.IsOpen (PROP) - FbSysDirInternal.LastResult (PROP) - FbSysDirInternal.Open (METH) - FbSysDirInternal.Read (METH)

## FbSysFsInternal (FB)


- FbSysFsInternal.ChangeWorkingDirectory (METH) - FbSysFsInternal.CheckDirectoryExists (METH) - FbSysFsInternal.CheckFileExists (METH) - FbSysFsInternal.CheckSDCardStatus (METH) - FbSysFsInternal.CopyFile (METH) - FbSysFsInternal.GetFreeSpaceInDirectory (METH) - FbSysFsInternal.LastResult (PROP) - FbSysFsInternal.MakeDirectory (METH) - FbSysFsInternal.MoveAllFilesInDirectory (METH) - FbSysFsInternal.MoveDirectory (METH) - FbSysFsInternal.MoveFile (METH) - FbSysFsInternal.NormalizeCanonicalFilename (METH) - FbSysFsInternal.NormalizeCanonicalPath (METH) - FbSysFsInternal.ReadFirstEntryInDirectory (METH) - FbSysFsInternal.RemoveAllFilesInDirectory (METH) - FbSysFsInternal.RemoveDirectoryWithContents (METH) - FbSysFsInternal.RemoveEmptyDirectory (METH) - FbSysFsInternal.RemoveFile (METH) - FbSysFsInternal.Rename (METH) - FbSysFsInternal.SetAttributes (METH) - FbSysFsInternal.Stat (METH) - FbSysFsInternal.TranslateNormalizedUrlToSpecific (METH) - FbSysFsInternal.WorkingDirectory (PROP) - FbSysFsInternal.copyFileCrossDevices (METH)

## fbExclusiveFileHandling (FB)


- fbExclusiveFileHandling.IsInUseByAnyExclusiveAccess (METH) - fbExclusiveFileHandling.IsInUseByExclusiveWriteAccess (METH) - fbExclusiveFileHandling.MarkExclusiveReadAccess (METH) - fbExclusiveFileHandling.MarkExclusiveWriteAccess (METH) - fbExclusiveFileHandling.ReleaseExclusiveAccess (METH)

## fbSysFileInternal (FB)


- fbSysFileInternal.Close (METH) - fbSysFileInternal.EofReached (PROP) - fbSysFileInternal.IsOpen (PROP) - fbSysFileInternal.IsReadable (PROP) - fbSysFileInternal.IsWritable (PROP) - fbSysFileInternal.LastResult (PROP) - fbSysFileInternal.Open (METH) - fbSysFileInternal.PaddWithZeroes (METH) - fbSysFileInternal.Pos (PROP) - fbSysFileInternal.Read (METH) - fbSysFileInternal.Seek (METH) - fbSysFileInternal.Write (METH) - fbSysFileInternal.actualSize (PROP)

### Functions


## ObsWrappedSysFileGetSize (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ObsWrappedSysFileGetSize | SysFile.RTS_IEC_RESULT |
| Input | sname | WagoTypes.Filename |
| Inout | udiSize | UDINT |

## ObsWrappedSysFileGetTime (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ObsWrappedSysFileGetTime | SysFile.RTS_IEC_RESULT |
| Input | sname | WagoTypes.Filename |
| Inout | FileTime | SysFile.SYS_FILETIME |

## SysCheckDirectoryExists (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SysCheckDirectoryExists | WagoTypes.eResultCode |  |
| Input | sSysDirName | WagoTypes.Filename | The name of the directory |

| Result codes |
| OK | The ressource denoted an existing directory |
| ENOENT | The ressource name is unknown |
| ENOTDIR | The ressource is known, but it denotes not a directory |

Checks, if a given ressource name denotes an existing directory on the PLC. The native pathes must be given. Prefixes and working-directories are not automatically resolved.

Interface variables Checks, if a given ressource name denotes an existing directory on the PLC. The native pathes must be given. Prefixes and working-directories are not automatically resolved.

## SysCheckFileExists (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SysCheckFileExists | WagoTypes.eResultCode |
| Input | sSysFileName | WagoTypes.Filename |

| Result codes |
| OK | The ressource denoted an existing file |
| ENOENT | The ressource name is unknown |
| EISDIR | The ressource is known, but it denotes a directory |

Checks, if a given ressource name denotes an existing file on the PLC. The native pathes must be given. Prefixes and working-directories are not automatically resolved.

Interface variables Checks, if a given ressource name denotes an existing file on the PLC. The native pathes must be given. Prefixes and working-directories are not automatically resolved.

## SysExt_FileGetStat (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SysExt_FileGetStat | SysFile.RTS_IEC_RESULT |  |
| Input | szName | WagoTypes.FileName | name of the resource to be investigated |
| Output | stat | typFileStat | structure containing resource information |

| Return values of SysExt_FileGetStat (RTS_IEC_RESULT) |
| 0 | = ERR_OK | sucessful operation |
| 16 | = ERR_NO_OBJECT | A component of the path does not exist, or a component of the path prefix is not a directory, or the path is an empty string. |
| 50 | = ERR_FILE_ERROR | the path is too long. |
| other | ... | other internal errors |
| ? | EACCES | Search permission is denied for one of the directories in the path prefix |
| ? | ELOOP | Too many symbolic links encountered while traversing the path. |
| ? | ENOMEM | Out of memory (i.e., kernel memory). |
| ? | EOVERFLOW | path or fd refers to a file whose size, inode number, or number of blocks cannot be represented [...] |

Reports the information about a file or a directory

If the resource is a directory, the name may or may not contain a trailing slash (‘/’), both variants are valid.

If the resource is a symbolic link, that link will be silently followed and the link status will be completely hidden from the caller.

When the returned RTS_IEC_RESULT is any other than ‘0=OK’, the output (including the field ‘filetype’) is an undefined state. Thus, evaluation of the result code is strictly mandatory when using this function.

Interface variables Reports the information about a file or a directory If the resource is a directory, the name may or may not contain a trailing slash (‘/’), both variants are valid. If the resource is a symbolic link, that link will be silently followed and the link status will be completely hidden from the caller. When the returned RTS_IEC_RESULT is any other than ‘0=OK’, the output (including the field ‘filetype’) is an undefined state. Thus, evaluation of the result code is strictly mandatory when using this function.

## SysExt_GetFreeSize (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SysExt_GetFreeSize | SysDir.RTS_IEC_RESULT |  |
| Input | szName | WagoTypes.FileName | Name of the directory which is to be investigated |
| Output | udiBlockSize | UDINT | Block size of the given directory (bytes) |
| udiAmountOfBlocks | UDINT | Number of free blocks in the directory (bytes) |

| Return values of SysExt_GetFreeSize (RTS_IEC_RESULT) |
| 0 | = ERR_OK | sucessful operation |
| 16 | = ERR_NO_OBJECT | named directory does not exist or invalid argument is given |
| other | [...] | internal errors |

SysExt_GetFreeSize() reports the free space in the filesystem which contains the directory named by the input parameter.

The named directory may or may not contain a trailing slash (‘/’), both variants are valid.

If the name denotes a regular file instead of a directory, the prefix path to that file will be used for calculation.

If a directory contains mountpoints to other file systems, the free space in these other file systems will be ignored for the calculation.

If the resource is a link to another file system, that link will be followed and the free space in the other FS will be reported.

When the returned RTS_IEC_RESULT is any other than ‘0=OK’, the output variables are in undefined states. Thus, evaluation of the return value is strictly mandatory when using this function.

Interface variables SysExt_GetFreeSize() reports the free space in the filesystem which contains the directory named by the input parameter. The named directory may or may not contain a trailing slash (‘/’), both variants are valid. If the name denotes a regular file instead of a directory, the prefix path to that file will be used for calculation. If a directory contains mountpoints to other file systems, the free space in these other file systems will be ignored for the calculation. If the resource is a link to another file system, that link will be followed and the free space in the other FS will be reported. When the returned RTS_IEC_RESULT is any other than ‘0=OK’, the output variables are in undefined states. Thus, evaluation of the return value is strictly mandatory when using this function.

### Methods


## FbSysDirInternal.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | WagoTypes.eResultCode |

| return codes |
| 0 | success |
| EBADF | Directory-FB was not open |

Closes the Directory scan.

corresponds to “closedir(3)”

This Method takes no arguments.

If a directory-FB is not open, an additional close() does no harm, but it ensures that the FB is closed in every case.

Interface variables Closes the Directory scan. corresponds to “closedir(3)” This Method takes no arguments. If a directory-FB is not open, an additional close() does no harm, but it ensures that the FB is closed in every case.

## FbSysDirInternal.Open (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Open | WagoTypes.eResultCode |  |
| Input | sDirName | WagoTypes.FileName | Name of the Directory to be scanned |

| return codes |
| 0 | success |
| ENOTDIR | name is not a directory. |

Starts the scanning of a directory

Interface variables Starts the scanning of a directory corresponds to “opendir(3)”

## FbSysDirInternal.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | WagoTypes.eResultCode |  |
| Inout | FileStatus | WagoTypes.typFileProperties | Output Buffer for file Status. |

| return codes |
| 0 | success |
| EBADFD | Directory not Open |
| ENODATA | No data available (end of directory reached) |
| other | specific reasons |

Reads the next entry of a directory

corresponds to “readdir(3)”

The user must provide a data structure “FileStatus : typFileStat” which is filled on success. On Failure or no more data, the structure is cleared, esp. the Name holds an empty string;

Special system entries, such as ”.” and ”..” are generally skipped.

On success, the method returns 0, on Failure an appropriate error code is returned. When the last entry has been read or the directory is empty, the following Read() returns ENODATA := 61 : No data available

On other faults, the specific fault code is returned.

ToDo: Support of attribute “archive”, “readonly”, “exclusive”

Interface variables Reads the next entry of a directory corresponds to “readdir(3)” The user must provide a data structure “FileStatus : typFileStat” which is filled on success. On Failure or no more data, the structure is cleared, esp. the Name holds an empty string; Special system entries, such as ”.” and ”..” are generally skipped. On success, the method returns 0, on Failure an appropriate error code is returned. When the last entry has been read or the directory is empty, the following Read() returns ENODATA := 61 : No data available On other faults, the specific fault code is returned. ToDo: Support of attribute “archive”, “readonly”, “exclusive”

## FbSysFsInternal.ChangeWorkingDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ChangeWorkingDirectory | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | Path of the working Directory |
| xForce | BOOL | if set, the path will be created, if it does not exist. |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EDQUOT | The user’s quota of disk blocks or inodes on the file system has been exhausted. |
| EEXIST | STRING already exists (not necessarily as a directory). |
| EFAULT | STRING points outside your accessible address space. (e.g. wrong prefix) |
| ENAMETOOLONG | STRING was too long. |
| ENOENT | A directory component in STRING does not exist or is a dangling symbolic link. |
| ENOSPC | The device containing STRING has no room for the new directory. |
| ENOTDIR | A component used as a directory in STRING is not, in fact, a directory. |
| EPERM | The file system containing STRING does not support the creation of directories. |
| EROFS | STRING refers to a file on a read-only file system. |
| others | specific to hardware |

Sets the current Working Directory

corresponds to “cd (1)”

Interface variables Sets the current Working Directory corresponds to “cd (1)”

## FbSysFsInternal.CheckDirectoryExists (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | CheckDirectoryExists | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | name of the questioned directory |

Checks if a name denotes a directory.

Interface variables Checks if a name denotes a directory.

## FbSysFsInternal.CheckFileExists (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | CheckFileExists | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | name of the questioned File |

Checks if a name denotes a file.

Interface variables Checks if a name denotes a file.

## FbSysFsInternal.CheckSDCardStatus (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | CheckSDCardStatus | BOOL |

## FbSysFsInternal.CopyFile (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | CopyFile | WagoTypes.eResultCode |  |
| Input | sSourceName | WagoTypes.FileName | the name of the source file |
| sDestinationName | WagoTypes.FileName | the name of the destination name or ~file |
| xOverwrite | BOOL | TRUE= overwrite of existing file is ok. |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| ENOENT | the source file does not exist |
| EISDIR | The source file names a directory |
| EBUSY | the destination file cannot be overwritten, because it is open. |
| EACCES | Destination Path cannot be created |
| EEXIST | The destination file exists and must not be overwritten. |
| ENOSPC | The device containing the file has no room for the new directory entry. |

Copies a file.

Copies one file to a second loaction.

corresponds to “cp(1)” and “link(2)”

The destination file my denote a filename or also a directory name, in which case the name of the file remains the same but only the path changes.

If the new file name needs creation of parent directories, those will be crated.

Note: whenever possible hardlinks were placed instead of a real binary copy, depending on the target hardware. This detail may result in substantial increase of performance. However, it is hidden from the application.

Interface variables Copies a file. Copies one file to a second loaction. corresponds to “cp(1)” and “link(2)” The destination file my denote a filename or also a directory name, in which case the name of the file remains the same but only the path changes. If the new file name needs creation of parent directories, those will be crated. Note: whenever possible hardlinks were placed instead of a real binary copy, depending on the target hardware. This detail may result in substantial increase of performance. However, it is hidden from the application.

## FbSysFsInternal.GetFreeSpaceInDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetFreeSpaceInDirectory | LINT |  |
| Input | sDirectoryName | WagoTypes.FileName | Name of the investigated directory |

Returns the free space in the File system.

As a PLC may handle multiple physical file systems, the FileName indicates which file system is meant.

Interface variables Returns the free space in the File system. As a PLC may handle multiple physical file systems, the FileName indicates which file system is meant.

## FbSysFsInternal.MakeDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MakeDirectory | WagoTypes.eResultCode |  |
| Input | sDirname | WagoTypes.FileName | the Name of the new directory |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EINVAL | Bad Name or Prefix |
| EEXIST | The Directory already exists |
| EACCES | A Component of the path could not be created |
| ENOTDIR | A component used as a directory in the name is not, in fact, a directory. |

creates a new directory

Interface variables creates a new directory corresponds to “mkdir (2)”

## FbSysFsInternal.MoveAllFilesInDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MoveAllFilesInDirectory | WagoTypes.eResultCode |  |
| Input | sDirName | WagoTypes.Filename | Source directory |
| sTargetDir | WagoTypes.FileName | Where to move |

Moves a complete directory branch.

Interface variables Moves a complete directory branch.

## FbSysFsInternal.MoveDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MoveDirectory | WagoTypes.eResultCode |  |
| Input | sOldName | WagoTypes.FileName | The File which is to be moved |
| sNewLocation | WagoTypes.FileName | the new name or path of that file |

| result codes |
| ENOSYS | This functionality is not supported by the target hardware |
| EBUSY | The directory to be removed is currently in use by the system. |
| ENOTEMPTY | The path argument names a directory that is not an empty directory. |
| ENAMETOOLONG | The length of the path argument or one of its components exceeds the size limit |
| ENOTDIR | A component of path is not a directory. |
| EROFS | The directory entry to be removed resides on a read-only file system. |
| ETIME | Timeout |

Removes a directory.

corresponds to “rmdir(2)”

In the regular case, it is necessary for a directory to be empty for removal.

When xRecursive is set, this function removes the directory including all its contents. As this process may take a significant amount of time on large structures, a timeout limit is also passed to this function. When the recursive removal takes too long, the function returns with “ETIME:= 62, // Timer expired” after at least one item ist removed.

When the directory to be removed is currently accessed by any open file- or dir-FB, this function fails with EBUSY.

Interface variables Removes a directory. corresponds to “rmdir(2)” In the regular case, it is necessary for a directory to be empty for removal. When xRecursive is set, this function removes the directory including all its contents. As this process may take a significant amount of time on large structures, a timeout limit is also passed to this function. When the recursive removal takes too long, the function returns with “ETIME:= 62, // Timer expired” after at least one item ist removed. When the directory to be removed is currently accessed by any open file- or dir-FB, this function fails with EBUSY.

## FbSysFsInternal.MoveFile (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MoveFile | WagoTypes.eResultCode |  |
| Input | sOldName | WagoTypes.FileName | The File which is to be moved |
| sNewLocation | WagoTypes.FileName | the new name or path of that file |

| result codes |
| ENOSYS | This functionality is not supported by the target hardware |
| EINVAL | Invalid arguments (e.g. empty pathes) |
| ENOENT | Source File does not exist |
| EISDIR | Source File is a directory |
| EBUSY | The directory to be removed is currently in use by the system. |
| ENOTEMPTY | The path argument names a directory that is not an empty directory. |
| ENAMETOOLONG | The length of the path argument or one of its components exceeds the size limit |
| ENOTDIR | A component of path is not a directory. |
| EROFS | The directory entry to be removed resides on a read-only file system. |
| ETIME | Timeout |

Moves a file.

Interface variables Moves a file.

## FbSysFsInternal.NormalizeCanonicalFilename (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | NormalizeCanonicalFilename | WagoTypes.Filename |
| Input | sName | WagoTypes.FileName |

Transforms a filename into a canonical form.

Converts backslashes and other strange characters.

Interface variables Transforms a filename into a canonical form. Converts backslashes and other strange characters.

## FbSysFsInternal.NormalizeCanonicalPath (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | NormalizeCanonicalPath | WagoTypes.FileName |
| Input | sName | WagoTypes.FileName |

Transforms a path into a canonical form.

Converts backslashes and other strange characters. Converts prefix (e.g. “HOME://”) into device specific internal mount point.

Interface variables Transforms a path into a canonical form. Converts backslashes and other strange characters. Converts prefix (e.g. “HOME://”) into device specific internal mount point.

## FbSysFsInternal.ReadFirstEntryInDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReadFirstEntryInDirectory | WagoTypes.eResultCode |  |
| Input | sname | WagoTypes.Filename | Name of the directory |
| Inout | FileStatus | WagoTypes.typFileProperties | Output Buffer for file Status. |

Reads the first entry in a given directory.

Interface variables Reads the first entry in a given directory.

## FbSysFsInternal.RemoveAllFilesInDirectory (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | RemoveAllFilesInDirectory | WagoTypes.eResultCode |
| Input | sDirName | WagoTypes.Filename |

Erases a complete directory branch.

Interface variables Erases a complete directory branch.

## FbSysFsInternal.RemoveDirectoryWithContents (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RemoveDirectoryWithContents | WagoTypes.eResultCode |  |
| Input | sDirName | WagoTypes.FileName | The name of the Directory to be deleted |

| result codes |
| ENOSYS | This functionality is not supported by the target hardware |
| EBUSY | The directory to be removed is currently in use by the system. |
| ENOTEMPTY | The path argument names a directory that is not an empty directory. |
| ENAMETOOLONG | The length of the path argument or one of its components exceeds the size limit |
| ENOTDIR | A component of path is not a directory. |
| EROFS | The directory entry to be removed resides on a read-only file system. |

removes a directory

corresponds to “rmdir(2)”

In the regular case, it is necessary for a directory to be empty for removal.

When xRecursive is set, this function removes the directory including all its contents. As this process may take a significant amount of time on large structures, a timeout limit is also passed to this function. When the recursive removal takes too long, the function returns with “ETIME:= 62, // Timer expired” after at least one item ist removed.

When the directory to be removed is currently accessed by any open file- or dir-FB, this function fails with EBUSY.

Interface variables removes a directory corresponds to “rmdir(2)” In the regular case, it is necessary for a directory to be empty for removal. When xRecursive is set, this function removes the directory including all its contents. As this process may take a significant amount of time on large structures, a timeout limit is also passed to this function. When the recursive removal takes too long, the function returns with “ETIME:= 62, // Timer expired” after at least one item ist removed. When the directory to be removed is currently accessed by any open file- or dir-FB, this function fails with EBUSY.

## FbSysFsInternal.RemoveEmptyDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RemoveEmptyDirectory | WagoTypes.eResultCode |  |
| Input | sDirName | WagoTypes.FileName | The name of the Directory to be deleted |

| result codes |
| ENOSYS | This functionality is not supported by the target hardware |
| EBUSY | The directory to be removed is currently in use by the system. |
| ENOTEMPTY | The path argument names a directory that is not an empty directory. |
| ENAMETOOLONG | The length of the path argument or one of its components exceeds the size limit |
| ENOTDIR | A component of path is not a directory. |
| EROFS | The directory entry to be removed resides on a read-only file system. |
| ETIME | Timeout |

removes a directory

corresponds to “rmdir(2)”

In the regular case, it is necessary for a directory to be empty for removal.

When xRecursive is set, this function removes the directory including all its contents. As this process may take a significant amount of time on large structures, a timeout limit is also passed to this function. When the recursive removal takes too long, the function returns with “ETIME:= 62, // Timer expired” after at least one item ist removed.

When the directory to be removed is currently accessed by any open file- or dir-FB, this function fails with EBUSY.

Interface variables removes a directory corresponds to “rmdir(2)” In the regular case, it is necessary for a directory to be empty for removal. When xRecursive is set, this function removes the directory including all its contents. As this process may take a significant amount of time on large structures, a timeout limit is also passed to this function. When the recursive removal takes too long, the function returns with “ETIME:= 62, // Timer expired” after at least one item ist removed. When the directory to be removed is currently accessed by any open file- or dir-FB, this function fails with EBUSY.

## FbSysFsInternal.RemoveFile (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | RemoveFile | WagoTypes.eResultCode |
| Input | sFilename | WagoTypes.FileName |

| return code: |
| 0 | : success; |
| EINVAL | : Invalid Filename |
| ENOSYS | : This functionality is not supported by the target hardware |
| EBUSY | : The file cannot be removed because it is being used by the system or another process |
| EISDIR | : STRING refers to a directory. |
| EACCESS | : the file cannot be removed due to wrong attributes |

removes a file

Interface variables removes a file corresponds to “rm(1)” and “unlink/ulink(2)”

## FbSysFsInternal.Rename (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Rename | WagoTypes.eResultCode |  |
| Input | sOldPath | WagoTypes.FileName | The Directory which is to be moved |
| sNewName | WagoTypes.FileName | the new name of that directory |
| xAllowOverwrite | BOOL | allows overwriting of existing Entities. |

| result codes |
| ENOSYS | This Functionality is not supported by the target hardware |
| EINVAL | Invalid sourcename |
| EEXIST | File or dir exists and may not be overwritten |
| EISDIR | the file to be overwritten is a directory |
| ENOTDIR | the directory to be overwritten is a file |
| EBUSY | The rename fails because oldpath or newpath is a directory that is in use by some process. |
| EINVAL | The new STRING contained a path prefix of the old one. |
| ENAMETOOLONG | Oldpath or newpath were too long. |
| ENOENT | Oldpath does not exist, or a directory component in newpath does not exist or the name is empty. |
| ENOSPC | The device containing the file has no room for the new directory entry. |
| ENOTDIR | A component used as a directory in oldpath or newpath is not, in fact, a directory. |
| ENOTEMPTY | Newpath is a nonempty directory, that is, contains entries other than ”.” and ”..”. |
| EROFS | The file is on a read-only file system. |
| EXDEV | Oldpath and newpath are not on the same mounted file system. |

Renames a file or directory within the same location.

corresponds to “mv(1)”

Interface variables Renames a file or directory within the same location. corresponds to “mv(1)”

## FbSysFsInternal.SetAttributes (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetAttributes | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | name of the File or directory |
| Inout | eNewProperties | WagoTypes.typFileProperties |  |

| result codes |
| 0 | success |
| ENOSYS | This Functionality is not supported by the target hardware |
| ENOENT | File does not exist |
| EPERM | Attributes cannot be manipulated |

Set File Attributes.

Interface variables Set File Attributes.

## FbSysFsInternal.Stat (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Stat | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | name of the stat’ed ressource |
| pFileStatus | POINTER TO WagoTypes.typFileProperties | Output Buffer for file Status. |

| result codes |
| 0 | Success |
| ENOSYS | This functionality is not supported by the target hardware |
| ENOENT | The requested file or directory does not exist. |
| ENOTDIR | The requested file could not be accessed directly as file and could also not be accessed as directory |
| EACCES | Other problems |

retrieves the status if a named file or directory

complement to “stat(2)”

This is recommended for determining, if a file exists at all. If a Pointer to a previously allocated filestatus structure is applied, that structure will be filled with the file information. Otherwise it will be simply checked, if the ressource exists or not.

Interface variables retrieves the status if a named file or directory complement to “stat(2)” This is recommended for determining, if a file exists at all. If a Pointer to a previously allocated filestatus structure is applied, that structure will be filled with the file information. Otherwise it will be simply checked, if the ressource exists or not.

## FbSysFsInternal.TranslateNormalizedUrlToSpecific (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | TranslateNormalizedUrlToSpecific | WagoTypes.FileName |
| Input | sNormalizedPath | WagoTypes.FileName |

Translates a normalized path to a hardwarespecific form.

(Attn: input MUST be in canonical form.) Returns en empty string on error, (such as: unknown prefix).

Interface variables Translates a normalized path to a hardwarespecific form. (Attn: input MUST be in canonical form.) Returns en empty string on error, (such as: unknown prefix).

## FbSysFsInternal.copyFileCrossDevices (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | copyFileCrossDevices | WagoTypes.eResultCode |
| Input | pSourceName | POINTER TO WagoTypes.Filename |
| pDestName | POINTER TO WagoTypes.Filename |

## fbExclusiveFileHandling.IsInUseByAnyExclusiveAccess (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IsInUseByAnyExclusiveAccess | BOOL |
| Input | sName | WagoTypes.FileName |

Checks for concurrent exclusive access.

Returns TRUE if any exclusive process is registered to have this file open.

Interface variables Checks for concurrent exclusive access. Returns TRUE if any exclusive process is registered to have this file open.

## fbExclusiveFileHandling.IsInUseByExclusiveWriteAccess (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IsInUseByExclusiveWriteAccess | BOOL |
| Input | sName | WagoTypes.FileName |

Checks for concurrent exclusive write access.

Returns TRUE if an exclusive write process is registered to have this file open.

Interface variables Checks for concurrent exclusive write access. Returns TRUE if an exclusive write process is registered to have this file open.

## fbExclusiveFileHandling.MarkExclusiveReadAccess (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MarkExclusiveReadAccess | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | which name is to be locked |
| ID | POINTER TO BYTE | identifies the calling FB |

| result codes |
| 0 | Success |
| ENOSYS | The Function is not implemented |
| EACCES | Exclusive Read Access cannot be granted |

Marks a file for exclusive read access.

Interface variables Marks a file for exclusive read access.

## fbExclusiveFileHandling.MarkExclusiveWriteAccess (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MarkExclusiveWriteAccess | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | which name is to be locked |
| ID | POINTER TO BYTE | identifies the calling FB |

| result codes |
| 0 | success |
| ENOSYS | The Function is not implemented |
| EACCES | Exclusive Read Access cannot be granted |

Marks a file for exclusive write access.

Interface variables Marks a file for exclusive write access.

## fbExclusiveFileHandling.ReleaseExclusiveAccess (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReleaseExclusiveAccess | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | which name is to be locked |
| ID | POINTER TO BYTE | identifies the calling FB |

| result codes |
| 0 | success |
| ENOSYS | The Function is not implemented |
| EACCES | Exclusive Read Access cannot be granted |

releases a file for exclusive read access.

Interface variables releases a file for exclusive read access.

## fbSysFileInternal.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | WagoTypes.eResultCode |

| return codes |
| 0 | success |
| EBADF | Directory-FB was not open |
| EIO | final flush reported an error. |

Closes the File

corresponds to “close(2)”

This Method takes no arguments.

If a file FB is not open, an additional close() does no harm, but it ensures that the FB is closed in every case.

Interface variables Closes the File corresponds to “close(2)” This Method takes no arguments. If a file FB is not open, an additional close() does no harm, but it ensures that the FB is closed in every case.

## fbSysFileInternal.Open (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Open | WagoTypes.eResultCode |  |
| Input | sName | WagoTypes.FileName | the name of the File |
| eAccMode | WagoTypes.eFileAccessMode | Access-Mode of the file |
| eSyncMode | WagoTypes.eFileSyncMode | Controls the synchronization between FS and physical modia |
| xExclusive | BOOL | TRUE = Exclusive access, FALSE = multiple access |

| return codes |
| 0 | success |
| EINVAL | Invalid Filename or Invalid Access Mode |
| EPERM | The File cold not be opened in desired access-mode or exclusivity mode. |
| ENOENT | the File was opened for reading but does not exist |
| EBUSY | The exclusivity-restrictions would be violated. |
| ENOTDIR | A component of the path prefix is not a directory. |
| EACCES | File cannot be accessed or a Component of the path could not be created |
| EISDIR | The Filename denotes a directory |

Opens a file for reading.

corresponds to “open(2)”

Un success, the FILE-fb transits to the state ‘xIsOpen’ and further operations (such as write, read, close, flush) may be performed on this instance.

Besides the filename, the user has to specify the access mode and the exclusivity mode. If the xExclusive-Flag is set, the file is granted to have - no other write-acces if opened for reading and - no other access at all if opened for writing. If that cannot be granted on opening, then open() fails with EBUSY. When a file is opened exclusively , subsequent opens() from other instances would fail, if that would collide with the previous restrictions.

If an open File-FB will encounter a second Open(), it will be cosed first before the new Open() will be performed.

Interface variables Opens a file for reading. corresponds to “open(2)” Un success, the FILE-fb transits to the state ‘xIsOpen’ and further operations (such as write, read, close, flush) may be performed on this instance. Besides the filename, the user has to specify the access mode and the exclusivity mode. If the xExclusive-Flag is set, the file is granted to have - no other write-acces if opened for reading and - no other access at all if opened for writing. If that cannot be granted on opening, then open() fails with EBUSY. When a file is opened exclusively , subsequent opens() from other instances would fail, if that would collide with the previous restrictions. If an open File-FB will encounter a second Open(), it will be cosed first before the new Open() will be performed.

## fbSysFileInternal.PaddWithZeroes (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PaddWithZeroes | WagoTypes.eResultCode |  |
| Input | liDesiredSize | LINT | to which size |

| return codes |
| 0 | success |
| EBADF | The file is not open for write access |
| EINVAL | Desired Size < 0; |
| EPERM | Desired Size beyond 4G |
| EACCES | The Operation could not be executed as desired, possibly because the file is too large |

Enlarges the file up to a given size

known bugs: due to technical limitations the usable filesize is limited to 4G.

Interface variables Enlarges the file up to a given size known bugs: due to technical limitations the usable filesize is limited to 4G.

## fbSysFileInternal.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | WagoTypes.eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | points to a buffer for read data |
| udiRxBufferSize | UDINT | Size of the Buffer |
| Inout | udiRxNBytes | UDINT | number of actually read bytes |

| return codes |
| 0 | success |
| EBADF | The file is not open for read access |
| EINVAL | Null-Pointer applied for buffer or zero buffer size was applied |
| ENODATA | No further data available |
| EACCES | Internal Error while reading data |

reads data from an open file

corresponds to “read(2)”

if the end of the file is reached, subsequent read() will return ENODATA

Interface variables reads data from an open file corresponds to “read(2)” if the end of the file is reached, subsequent read() will return ENODATA

## fbSysFileInternal.Seek (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Seek | WagoTypes.eResultCode |  |
| Input | liPos | LINT | desired relative position |
| whence | WagoTypes.eSeekMode | relative to what? |

| return codes |
| 0 | success |
| ENODATA | Attempt to position behind End of File (exactly at EOF will still produce ‘OK’). This is not an error. |
| EBADF | The file is not open or not seekable |
| EINVAL | Invalid argument for new position or seek mode “whence” |
| ENOSYS | The Function is not implemented |
| EPERM | The Operation could not be executed as desired |
| EACCES | Attempt to access positions before Start of File or behind the 4G-Border. |

| Parameter “whence” (seek Mode) |
| fromStart | 0 | (SEEK_SET) positiopn the file pointer relative to start of file |
| fromEnd | 1 | (SEEK_END) position the file ponter relative to file end (negative values!) |
| fromActualPosition | 2 | (SEEK_CUR) positioning reletive to actual position |

sets the filepointer to the desired position

corresponds to ‘fseek(3)’

Known Bugs:

Filepositions behind the 4G-Border could not be accesses due to technical limitations of the underlying

Interface variables sets the filepointer to the desired position corresponds to ‘fseek(3)’ Known Bugs: Filepositions behind the 4G-Border could not be accesses due to technical limitations of the underlying

## fbSysFileInternal.Write (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Write | WagoTypes.eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | points to the write data |
| udiTxBufferSize | UDINT | Size of the write data |

| return codes |
| 0 | success |
| EBADF | The file is not open for write access |
| EINVAL | Null-Pointer applied for data |
| EACCES | Internal Problems while writing data |
| EINTR | Only Parts of the Data could be written. |
| ENOSPC | There was no free space remaining on the device containing the file. |
| ECONNRESET | SyncedWrite failed. |
| ENOTRECOVERABLE | Seek failed when executing SyncedWrite. |

writes to an opened file

Interface variables writes to an opened file corresponds to “write(2)”

### Program Organization


## 20 Program Organization Units


- FbSysDirInternal (FB) FbSysDirInternal.Close (METH) - FbSysDirInternal.EofReached (PROP) - FbSysDirInternal.IsOpen (PROP) - FbSysDirInternal.LastResult (PROP) - FbSysDirInternal.Open (METH) - FbSysDirInternal.Read (METH) FbSysFsInternal (FB) - FbSysFsInternal.ChangeWorkingDirectory (METH) - FbSysFsInternal.CheckDirectoryExists (METH) - FbSysFsInternal.CheckFileExists (METH) - FbSysFsInternal.CheckSDCardStatus (METH) - FbSysFsInternal.CopyFile (METH) - FbSysFsInternal.GetFreeSpaceInDirectory (METH) - FbSysFsInternal.LastResult (PROP) - FbSysFsInternal.MakeDirectory (METH) - FbSysFsInternal.MoveAllFilesInDirectory (METH) - FbSysFsInternal.MoveDirectory (METH) - FbSysFsInternal.MoveFile (METH) - FbSysFsInternal.NormalizeCanonicalFilename (METH) - FbSysFsInternal.NormalizeCanonicalPath (METH) - FbSysFsInternal.ReadFirstEntryInDirectory (METH) - FbSysFsInternal.RemoveAllFilesInDirectory (METH) - FbSysFsInternal.RemoveDirectoryWithContents (METH) - FbSysFsInternal.RemoveEmptyDirectory (METH) - FbSysFsInternal.RemoveFile (METH) - FbSysFsInternal.Rename (METH) - FbSysFsInternal.SetAttributes (METH) - FbSysFsInternal.Stat (METH) - FbSysFsInternal.TranslateNormalizedUrlToSpecific (METH) - FbSysFsInternal.WorkingDirectory (PROP) - FbSysFsInternal.copyFileCrossDevices (METH) fbExclusiveFileHandling (FB) - fbExclusiveFileHandling.IsInUseByAnyExclusiveAccess (METH) - fbExclusiveFileHandling.IsInUseByExclusiveWriteAccess (METH) - fbExclusiveFileHandling.MarkExclusiveReadAccess (METH) - fbExclusiveFileHandling.MarkExclusiveWriteAccess (METH) - fbExclusiveFileHandling.ReleaseExclusiveAccess (METH) fbSysFileInternal (FB) - fbSysFileInternal.Close (METH) - fbSysFileInternal.EofReached (PROP) - fbSysFileInternal.IsOpen (PROP) - fbSysFileInternal.IsReadable (PROP) - fbSysFileInternal.IsWritable (PROP) - fbSysFileInternal.LastResult (PROP) - fbSysFileInternal.Open (METH) - fbSysFileInternal.PaddWithZeroes (METH) - fbSysFileInternal.Pos (PROP) - fbSysFileInternal.Read (METH) - fbSysFileInternal.Seek (METH) - fbSysFileInternal.Write (METH) - fbSysFileInternal.actualSize (PROP)

### Internal Components


## 90 Internal


- ObsWrappedSysFileGetSize (FUN) - ObsWrappedSysFileGetTime (FUN) - SysCheckDirectoryExists (FUN) - SysCheckFileExists (FUN)

## FbSysDirInternal.EofReached (PROP)


indicates that no more data can be read from this directory.

Note: It’s also set, when the directory is not or never has been open.

indicates that no more data can be read from this directory. Note: It’s also set, when the directory is not or never has been open.

## FbSysDirInternal.IsOpen (PROP)


indicates whether the directory-FB is open for reading.

indicates whether the directory-FB is open for reading.

## FbSysDirInternal.LastResult (PROP)


represents the result code of the last method

corresponds to “errno”

represents the result code of the last method corresponds to “errno”

## FbSysFsInternal.LastResult (PROP)


represents the result code of the last method

corresponds to “errno”

represents the result code of the last method corresponds to “errno”

## FbSysFsInternal.WorkingDirectory (PROP)


Retrieves the name of the current working directory.

If the working directory is not set, an empty string is returned.

Note: although the workung directory can as well be retrieved and set, the setter-function is designed as method “ChangWorkingDirectory (cd)”, because it could potentially fail. The getter-function instead is designed as property get, because it does not return a status result.

Retrieves the name of the current working directory. complement to “pwd” If the working directory is not set, an empty string is returned. Note: although the workung directory can as well be retrieved and set, the setter-function is designed as method “ChangWorkingDirectory (cd)”, because it could potentially fail. The getter-function instead is designed as property get, because it does not return a status result.

## WagoSysFileDir_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysFileDir_Internal_PFC |
| Version: | 1.1.1.2 |
| Categories: | WAGO Internal\|Target\|PFC |
| Namespace: | WagoSysFileDirInternal |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated.

Target specific FileDir library for PFC

This document is automatically generated. Target specific FileDir library for PFC

### Contents:


- 20 Program Organization Units FbSysDirInternal (FB) - FbSysFsInternal (FB) - fbExclusiveFileHandling (FB) - fbSysFileInternal (FB) 90 Internal - ObsWrappedSysFileGetSize (FUN) - ObsWrappedSysFileGetTime (FUN) - SysCheckDirectoryExists (FUN) - SysCheckFileExists (FUN) 91 TSC - SysExt_FileGetStat (FUN) - SysExt_GetFreeSize (FUN) - eFileType (ENUM) - typFileStat (STRUCT) GVL (GVL) LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoSysFileDir_Internal_PFC.library, last modified 29.05.2024, 19:51:33. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysFileDir_Internal_PFC.library, last modified 29.05.2024, 19:51:33. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

## fbSysFileInternal.EofReached (PROP)


indicates the end of the file for read access.

if the FB was not open, this property is TRUE;

indicates the end of the file for read access. if the FB was not open, this property is TRUE;

## fbSysFileInternal.IsOpen (PROP)


indicates, if a File-FB is open or not.

indicates, if a File-FB is open or not.

## fbSysFileInternal.IsReadable (PROP)


specifies, if the FB allows read-access

specifies, if the FB allows read-access

## fbSysFileInternal.IsWritable (PROP)


specifies if write-access is permitted to the File-FB

specifies if write-access is permitted to the File-FB

## fbSysFileInternal.LastResult (PROP)


represents the result code of the last method

corresponds to “errno”

represents the result code of the last method corresponds to “errno”

## fbSysFileInternal.Pos (PROP)


returns the actual position of the file pointer

corresponds to “fgetpos(3)”

if the file is not open or does not allow positioning, the position is -1.

returns the actual position of the file pointer corresponds to “fgetpos(3)” if the file is not open or does not allow positioning, the position is -1.

## fbSysFileInternal.actualSize (PROP)


Size of the file.

### Global Variable Lists


## GVL (GVL)


| Name | Type |
| --- | --- |
| gFileSystem | FbSysFsInternal |

## LibraryResult (GVL)


| Name | Type |
| --- | --- |
| Factory | WagoSysErrorBase.FbResultFactory |

```
VAR
  eMyResult : eResultCode;  // result code whic is to be investigated
  oError    : FbResult;     // result object for use in highe levels.
END_VAR;

eMyResult := myFunction(...);
Namespace.LibraryResult.Factory.SetResult(eMyResult, oError);
```

Factory for standard result objects

Use this to translate result codes from this library into standard result objects.

where ‘Namespace’ denotes the namespace which is used for including the specific library and ‘myFunction()’ is an example for a general function from this library.

Factory for standard result objects Use this to translate result codes from this library into standard result objects. Usage: where ‘Namespace’ denotes the namespace which is used for including the specific library and ‘myFunction()’ is an example for a general function from this library.

## ResultItems (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | ERROR | ARRAY [0..26] OF typResultItem | [STRUCT(ID := WagoTypes.eResultCode.OK, Severity := WagoTypes.eSeverity.none, Text := ‘OK’), STRUCT(ID := WagoTypes.eResultCode.ENODATA, Severity := WagoTypes.eSeverity.info, Text := ‘No (more) data to transfer.’), STRUCT(ID := WagoTypes.eResultCode.ENOSYS, Severity := WagoTypes.eSeverity.error, Text := ‘Function not implemented.’), STRUCT(ID := WagoTypes.eResultCode.EACCES, Severity := WagoTypes.eSeverity.error, Text := ‘No Access granted or other problems while executing this function.’), STRUCT(ID := WagoTypes.eResultCode.EBADF, Severity := WagoTypes.eSeverity.error, Text := ‘File not open for the desired mode.’), STRUCT(ID := WagoTypes.eResultCode.ENOTDIR, Severity := WagoTypes.eSeverity.error, Text := ‘The referenced resource should be a proper directory name but is not.’), STRUCT(ID := WagoTypes.eResultCode.EIO, Severity := WagoTypes.eSeverity.error, Text := ‘Flush operation reported an internal failure.’), STRUCT(ID := WagoTypes.eResultCode.EINVAL, Severity := WagoTypes.eSeverity.error, Text := ‘Invalid argument, parameter, filename, or access mode.’), STRUCT(ID := WagoTypes.eResultCode.EPERM, Severity := WagoTypes.eSeverity.error, Text := ‘Operation not permitted under these circumstances.’), STRUCT(ID := WagoTypes.eResultCode.ENOENT, Severity := WagoTypes.eSeverity.error, Text := ‘No such file or directory.’), STRUCT(ID := WagoTypes.eResultCode.EBUSY, Severity := WagoTypes.eSeverity.error, Text := ‘Device or resource is busy or exclusivity restricions apply.’), STRUCT(ID := WagoTypes.eResultCode.EISDIR, Severity := WagoTypes.eSeverity.error, Text := ‘Is a directory - a regular file was expected instead of a directory.’), STRUCT(ID := WagoTypes.eResultCode.EINTR, Severity := WagoTypes.eSeverity.error, Text := ‘Interrupted - not all data cold be processed.’), STRUCT(ID := WagoTypes.eResultCode.ENOSPC, Severity := WagoTypes.eSeverity.error, Text := ‘No space left on device - we are running out of resources.’), STRUCT(ID := WagoTypes.eResultCode.ECONNRESET, Severity := WagoTypes.eSeverity.error, Text := ‘SyncedWrite failed.’), STRUCT(ID := WagoTypes.eResultCode.ENOTRECOVERABLE, Severity := WagoTypes.eSeverity.error, Text := ‘Seek failed when executing SyncedWrite.’), STRUCT(ID := WagoTypes.eResultCode.EDQUOT, Severity := WagoTypes.eSeverity.error, Text := ‘The quota of disk blocks or inodes has been exhausted.’), STRUCT(ID := WagoTypes.eResultCode.EEXIST, Severity := WagoTypes.eSeverity.error, Text := ‘File or directory exists but is expected to be non-existent.’), STRUCT(ID := WagoTypes.eResultCode.EFAULT, Severity := WagoTypes.eSeverity.error, Text := ‘Bad address or prefi or bad reference to parameters or values.’), STRUCT(ID := WagoTypes.eResultCode.ENAMETOOLONG, Severity := WagoTypes.eSeverity.error, Text := ‘File name too long.’), STRUCT(ID := WagoTypes.eResultCode.EROFS, Severity := WagoTypes.eSeverity.error, Text := ‘Read-only file system - attempt to modify a RO-file system.’), STRUCT(ID := WagoTypes.eResultCode.ETIME, Severity := WagoTypes.eSeverity.error, Text := ‘Timeout.’), STRUCT(ID := WagoTypes.eResultCode.ENOTEMPTY, Severity := WagoTypes.eSeverity.error, Text := ‘Directory not empty - we assume it should be empty.’), STRUCT(ID := WagoTypes.eResultCode.EXDEV, Severity := WagoTypes.eSeverity.error, Text := ‘Cross-device link - an invalid combination of resources.’), STRUCT(ID := WagoTypes.eResultCode.EAGAIN, Severity := WagoTypes.eSeverity.info, Text := ‘Try again: re-execution of this functionality is necessary.’), STRUCT(ID := WagoTypes.eResultCode.EFBIG, Severity := WagoTypes.eSeverity.error, Text := ‘File too large - the file size would exceed certain logical limits.’), STRUCT(ID := WagoTypes.eResultCode.EBADSTATE, Severity := WagoTypes.eSeverity.error, Text := ‘The Fb is not in the proper state for this operation.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 06.05.2024 | 1.1.1.2 | u010663 | Bugfix FbSysFsInternal MoveFile |
| 25.04.2024 | 1.1.1.1 | u010663 | Changes to avoid compiler warning C0394 |
| 19.02.2024 | 1.1.1.0 | u015614 | Remove additional check of /proc/mounts for SD-Card accesss due to security restrictions |
| 23.10.2023 | 1.1.0.4 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 15.09.2023 | 1.1.0.3 | WAGO / u013972 | fix problem with access rights |
| 31.07.2023 | 1.1.0.2 | WAGO / u013972 | WAT35751: fix problem with pseudo data types |
| 12.04.2023 | 1.1.0.1 | u0103719 | WAT35628: add pseudo data types |
| 13.09.2022 | 1.1.0.0 | u0103719 | rename object identifier of “eFileType.CHAR” to “eFileType._CHAR” ->Key “CHAR” is reserved from 61131-3 |
| 05.04.2022 | 1.0.5.3 | u0103719 | rename object type “char” to “eChar” |
| 08.01.2019 | 1.0.5.2 | u015842 | Properties: copyright added |
| 19.04.2016 | 1.0.5.0 | WAGO / u013972 | WAT18871 If the SD-Card is not inserted the directory will automaticly created |
| 04.03.2016 | 1.0.3.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoSysErrorBase and WagoTypesErrorBase |
| 23.10.2015 | 1.0.2.0 | WAGO / u013972 | Change Input-Parameter of Tsc-Functions |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Change Homepath to ‘/home/codesys/’, Resolve libraries with placeholders |
| 06.03.2015 | 1.0.0.0 | RE | Release Version |

WagoSysFileDir_Internal_PFC

WagoSysFileDir_Internal_PFC

### Other Components


## 91 TSC


- SysExt_FileGetStat (FUN) - SysExt_GetFreeSize (FUN) - eFileType (ENUM) - typFileStat (STRUCT)

## eFileType (ENUM)


| Name | Initial |
| --- | --- |
| UNKNOWN | 0 |
| REGULAR | 1 |
| DIR | 2 |
| FIFO | 3 |
| _CHAR | 4 |
| BLOCK | 5 |

## typFileStat (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| change | DT | time stamp of last change |
| filetype | eFileType | type of file |
| size | ULINT | size of file in case of dir the value is always zero |