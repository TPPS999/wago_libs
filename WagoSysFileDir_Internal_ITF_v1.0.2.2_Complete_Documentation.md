# WagoSysFileDir_Internal_ITF v1.0.2.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysFileDir_Internal_ITF
- **Version:** 1.0.2.2
- **Categories:** WAGO Internal|Common|Types and Interfaces
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysFileDir_Internal_ITF

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Interface to FileSystem Interface for internal usage as well as for application programming [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Interface to FileSystem Interface for internal usage as well as for application programming [1]

### Contents: ¶


Contents: - Project Information - Library Information - Functions - Methods IWagoSysDirInternal.Close (METH) - IWagoSysDirInternal.Open (METH) - IWagoSysDirInternal.Read (METH) - IWagoSysFileInternal.Close (METH) - IWagoSysFileInternal.Open (METH) - IWagoSysFileInternal.Read (METH) - IWagoSysFileInternal.Seek (METH) - IWagoSysFileInternal.Write (METH) - IWagoSysFsInternal.ChangeWorkingDirectory (METH) - IWagoSysFsInternal.CopyFile (METH) - ... and 10 more Interfaces - IWagoSysDirInternal (ITF) - IWagoSysFileInternal (ITF) - IWagoSysFsInternal (ITF) Internal Components - IWagoSysDirInternal.EofReached (PROP) - IWagoSysDirInternal.IsOpen (PROP) - IWagoSysDirInternal.LastResult (PROP) - IWagoSysFileInternal.EofReached (PROP) - IWagoSysFileInternal.IsOpen (PROP) - IWagoSysFileInternal.IsReadable (PROP) - IWagoSysFileInternal.IsWritable (PROP) - IWagoSysFileInternal.LastResult (PROP) - IWagoSysFileInternal.Pos (PROP) - IWagoSysFsInternal.LastResult (PROP) - ... and 2 more Global Variable Lists

### Indices and tables ¶


| [1] | Based on WagoSysFileDir_Internal_itf.library, last modified 14.01.2019, 16:45:03. The content of this file was automatically generated with None on 14.01.2019, 16:45:06 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysFileDir_Internal_itf.library |
| contentFile | WagoSysFileDir_Internal_ITF_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 16:45:06 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 16:45:03 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO / u013972 |
| Placeholder | WagoSysFileDir_Internal_ITF |
| Company | WAGO |
| Title | WagoSysFileDir_Internal_ITF |
| Project | WagoSysFileDir_Internal_itf |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Version | version | 1.0.2.2 |
| LibraryCategories | library-category-list | WAGO Internal\|Common\|Types and Interfaces |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 08.01.2019 | 1.0.2.2 | u015842 | Properties: copyright added |
| 18.04.2018 | 1.0.2.1 | WAGO / u013972 | Resolve documentation error |
| 26.02.2016 | 1.0.2.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoTypesErrorBase |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Resolve libraries with placeholders |
| 06.03.2015 | 1.0.0.0 | RE | Release Version |

WagoSysFileDir_Internal_itf.library

Attn: Documentation is not yet revised! Workaround: get proper Doc from WagoSysFileDir_Internal_PCF. Sorry for the inconvenience.

Interface variables WagoSysFileDir_Internal_itf.library Attn: Documentation is not yet revised! Workaround: get proper Doc from WagoSysFileDir_Internal_PCF. Sorry for the inconvenience.

### Methods


## IWagoSysDirInternal.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | eResultCode |

| return codes |
| 0 | success |
| EBADF | Directory-FB was not open |

Closes the Directory scan.

corresponds to “closedir(3)”

This Method takes no arguments.

If a directory-FB is not open, an additional close() does no harm, but it ensures that the FB is closed in every case.

Interface variables Closes the Directory scan. corresponds to “closedir(3)” This Method takes no arguments. If a directory-FB is not open, an additional close() does no harm, but it ensures that the FB is closed in every case.

## IWagoSysDirInternal.Open (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Open | eResultCode |  |
| Input | sDirName | FileName | Name of the Directory to be scanned |

| return codes |
| 0 | success |
| ENOTDIR | name is not a directory. |

Starts the scanning of a directory

Interface variables Starts the scanning of a directory corresponds to “opendir(3)”

## IWagoSysDirInternal.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | eResultCode |  |
| Inout | FileStatus | typFileProperties | Output Buffer for file Status. |

| return codes |
| 0 | success |
| EBADFD | Directory not Open |
| ENODATA | No data available (end of directory reached) |
| other | specific reasons |

Reads the next entry of a directory

corresponds to “readdir(3)”

The user must provide a data structure “FileStatus : typFileProperties” which is filled on success. On Failure or no more data, the structure is cleared, esp. the Name holds an empty string;

Special system entries, such as ”.” and ”..” are generally skipped.

On success, the method returns 0, on Failure an appropriate error code is returned. When the last entry has been read or the directory is empty, the following Read() returns ENODATA := 61 : No data available

On other faults, the specific fault code is returned.

Interface variables Reads the next entry of a directory corresponds to “readdir(3)” The user must provide a data structure “FileStatus : typFileProperties” which is filled on success. On Failure or no more data, the structure is cleared, esp. the Name holds an empty string; Special system entries, such as ”.” and ”..” are generally skipped. On success, the method returns 0, on Failure an appropriate error code is returned. When the last entry has been read or the directory is empty, the following Read() returns ENODATA := 61 : No data available On other faults, the specific fault code is returned.

## IWagoSysFileInternal.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | eResultCode |

| return codes |
| 0 | success |
| EBADF | Directory-FB was not open |

Closes the File

corresponds to “close(2)”

This Method takes no arguments.

If a file FB is not open, an additional close() does no harm, but it ensures that the FB is closed in every case.

Interface variables Closes the File corresponds to “close(2)” This Method takes no arguments. If a file FB is not open, an additional close() does no harm, but it ensures that the FB is closed in every case.

## IWagoSysFileInternal.Open (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Open | eResultCode |  |
| Input | sName | FileName | the name of the File |
| eAccMode | eFileAccessMode | Access-Mode of the file |
| eSyncMode | eFileSyncMode | Controls the synchronization between FS and physical modia |
| xExclusive | BOOL | TRUE = Exclusive access, FALSE = multiple access |

| return codes |
| 0 | success |
| ENAMETOOLONG | The length of the path argument exceeds its limits |
| ENOENT | the File was opened for reading but does not exist |
| ENOSPC | The directory or file system that would contain the new file cannot be expanded |
| ENOTDIR | A component of the path prefix is not a directory. |
| EROFS | The named file resides on a read-only file system is opened for writze-access |
| EBUSY | The exclusivity-restrictions would be violated. |
| EPERM | The File cold not be opened in desired access-mode |
| other | system specific errors |

Opens a file for reading.

corresponds to “open(2)”

Un success, the FILE-fb transits to the state ‘xIsOpen’ and further operations (such as write, read, close, flush) may be performed on this instance.

Besides the String, the user has to specify the access mode and the exclusivity mode. If the xExclusive-Flag is set, the file is granted to have - no other write-acces if opened for reading and - no other access at all if opened for writing. If that cannot be granted on opening, then open() fails with EBUSY. When a file is opened exclusively , subsequent opens() from other instances would fail, if that would collide with the previous restrictions.

If an open File-FB will encounter a second Open(), it will be cosed first before the new Open() will be performed.

Interface variables Opens a file for reading. corresponds to “open(2)” Un success, the FILE-fb transits to the state ‘xIsOpen’ and further operations (such as write, read, close, flush) may be performed on this instance. Besides the String, the user has to specify the access mode and the exclusivity mode. If the xExclusive-Flag is set, the file is granted to have - no other write-acces if opened for reading and - no other access at all if opened for writing. If that cannot be granted on opening, then open() fails with EBUSY. When a file is opened exclusively , subsequent opens() from other instances would fail, if that would collide with the previous restrictions. If an open File-FB will encounter a second Open(), it will be cosed first before the new Open() will be performed.

## IWagoSysFileInternal.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | points to a buffer for read data |
| udiRxBufferSize | UDINT | Size of the Buffer |
| Inout | udiRxNBytes | UDINT | number of actually read bytes |

| return codes |
| 0 | success |
| EBADF | The file is not open for read access |
| EINVAL | Null-Pointer applied for buffer or zero buffer size was applied |
| ENODATA | No further data available |

reads data from an open file

corresponds to “read(2)”

if the end of the file is reached, subsequent read() will return ENODATA

Interface variables reads data from an open file corresponds to “read(2)” if the end of the file is reached, subsequent read() will return ENODATA

## IWagoSysFileInternal.Seek (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Seek | eResultCode |  |
| Input | liPos | LINT | desired relative position |
| whence | eSeekMode | relative to what? |

| return codes |
| 0 | success |
| EBADF | The file is not open or not seekable |
| EINVAL | Invalid argument for new position or seek mode “whence” |
| ENOSYS | The Function is not implemented |

| Parameter “whence” (seek Mode) |
| fromStart | 0 | (SEEK_SET) positiopn the file pointer relative to start of file |
| fromEnd | 1 | (SEEK_END) position the file ponter relative to file end (negative values!) |
| fromActualPosition | 2 | (SEEK_CUR) positioning reletive to actual position |

sets the filepointer to the desired position

Interface variables sets the filepointer to the desired position corresponds to “fseek(3)”

## IWagoSysFileInternal.Write (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Write | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | points to the write data |
| udiTxBufferSize | UDINT | Size of the write data |

| return codes |
| 0 | success |
| EBADF | The file is not open for write access |
| ENOSPC | There was no free space remaining on the device containing the file. |
| EINVAL | Null-Pointer applied for data |
| ETIME | Timeout occurred before all data were written. |
| EAGAIN | Write was incomplete for other reasons |

writes to an opened file

Interface variables writes to an opened file corresponds to “write(2)”

## IWagoSysFsInternal.ChangeWorkingDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ChangeWorkingDirectory | eResultCode |  |
| Input | sName | FileName | absolute Path of the working Directory |
| xForce | BOOL | if set, the path will be created, if it does not exist. |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EDQUOT | The user’s quota of disk blocks or inodes on the file system has been exhausted. |
| EEXIST | STRING already exists (not necessarily as a directory). This includes the case where STRING is a symbolic link, dangling or not. |
| EFAULT | STRING points outside your accessible address space. (e.g. wrong prefix) |
| ENAMETOOLONG | STRING was too long. |
| ENOENT | A directory component in STRING does not exist or is a dangling symbolic link. |
| ENOSPC | The device containing STRING has no room for the new directory. |
| ENOTDIR | A component used as a directory in STRING is not, in fact, a directory. |
| EPERM | The file system containing STRING does not support the creation of directories. |
| EROFS | STRING refers to a file on a read-only file system. |
| others | specific to hardware |

Sets the current Working Directory

Interface variables Sets the current Working Directory corresponds to “cd (1)”

## IWagoSysFsInternal.CopyFile (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | CopyFile | eResultCode |  |
| Input | sSourceName | FileName | the name of the source file |
| sDestinationName | FileName | the name of the destination name or ~file |
| xOverwrite | BOOL | TRUE= overwrite of existing file is ok. |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| ENOENT | the source file does not exist |
| EBUSY | the destination file cannot be overwritten, because it is open. |
| EACCES | Destination Path cannot be created |
| ETIME | Timeout reached, before the copy was completed. |
| EEXIST | The destination file exists and must not be overwritten. |
| ENOSPC | The device containing the file has no room for the new directory entry. |

copies a file

Copies one file to a second loaction.

corresponds to “cp(1)” and “link(2)”

The destination file my denote a String or also a directory name, in which case the name of the file remains the same but only the path changes.

If the new file name needs creation of parent directories, those will be crated.

Note: whenever possible hardlinks were placed instead of a real binary copy, depending on the target hardware. This detail may result in substantial increase of performance. However, it is hidden from the application.

Interface variables copies a file Copies one file to a second loaction. corresponds to “cp(1)” and “link(2)” The destination file my denote a String or also a directory name, in which case the name of the file remains the same but only the path changes. If the new file name needs creation of parent directories, those will be crated. Note: whenever possible hardlinks were placed instead of a real binary copy, depending on the target hardware. This detail may result in substantial increase of performance. However, it is hidden from the application.

## IWagoSysFsInternal.MakeDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MakeDirectory | eResultCode |  |
| Input | sDirname | FileName | the Name of the new directory |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EEXIST | STRING already exists (not necessarily as a directory). This includes the case where STRING is a symbolic link, dangling or not. |
| EFAULT | STRING points outside your accessible address space. (e.g. wrong prefix) |
| ENAMETOOLONG | STRING was too long. |
| ENOENT | A directory component in STRING does not exist or is a dangling symbolic link. |
| ENOSPC | The device containing STRING has no room for the new directory. |
| ENOTDIR | A component used as a directory in STRING is not, in fact, a directory. |
| EPERM | The file system containing STRING does not support the creation of directories. |
| EROFS | STRING refers to a file on a read-only file system. |
| others | other reasons, see hardware manual for details. |

creates a new directory

Interface variables creates a new directory corresponds to “mkdir (2)”

## IWagoSysFsInternal.MoveDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MoveDirectory | eResultCode |  |
| Input | sOldName | FileName | The Directory which is to be moved |
| sNewLocation | FileName | the new name or path of that file |

| return codes |
| 0 | success |
| ENOSYS | This Functionality is not supported by the target hardware |
| EBUSY | The rename fails because oldpath or newpath is a directory that is in use by some process |
| ENAMETOOLONG | oldpath or newpath were too long. |
| ENOENT | The old name does not exist; or, a directory component in newpath does not exist; or, oldpath or newpath is an empty string. |
| ENOSPC | The device containing the file has no room for the new directory entry. |
| ENOTDIR | A component used as a directory in oldpath or newpath is not, in fact, a directory. |
| EROFS | The file is on a read-only file system. |
| EXDEV | oldpath and newpath are not on the same mounted file system. (Linux permits a file system to be mounted at multiple points, but rename() does not work across different mount points, even if the same file system is mounted on both.) |

Moves (i.e. “renames”) a file from one location to another.

corresponds to “mv(1)” for files

The new name may be a String, in wich case the file is simply renamed, or int may be a directory name, in whioch case the file is moved, but keeps its String.

If the new path needs the creation of new subdirectories, these directories will be created. In addition to regular Linux-Beahaviour, this function may move files also between different media if the system supports that.

Interface variables Moves (i.e. “renames”) a file from one location to another. corresponds to “mv(1)” for files The new name may be a String, in wich case the file is simply renamed, or int may be a directory name, in whioch case the file is moved, but keeps its String. If the new path needs the creation of new subdirectories, these directories will be created. In addition to regular Linux-Beahaviour, this function may move files also between different media if the system supports that.

## IWagoSysFsInternal.MoveFile (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | MoveFile | eResultCode |  |
| Input | sOldName | FileName | The File which is to be moved |
| sNewLocation | FileName | the new name or path of that file |

| return codes |
| 0 | success |
| ENOSYS | This Functionality is not supported by the target hardware |
| EBUSY | The rename fails because oldpath or newpath is a directory that is in use by some process |
| ENAMETOOLONG | oldpath or newpath were too long. |
| ENOENT | The old name does not exist; or, a directory component in newpath does not exist; or, oldpath or newpath is an empty string. |
| ENOSPC | The device containing the file has no room for the new directory entry. |
| ENOTDIR | A component used as a directory in oldpath or newpath is not, in fact, a directory. |
| EROFS | The file is on a read-only file system. |
| EXDEV | oldpath and newpath are not on the same mounted file system. (Linux permits a file system to be mounted at multiple points, but rename() does not work across different mount points, even if the same file system is mounted on both.) |

Moves (i.e. “renames”) a file from one location to another.

corresponds to “mv(1)” for files

The new name may be a String, in wich case the file is simply renamed, or int may be a directory name, in whioch case the file is moved, but keeps its String.

If the new path needs the creation of new subdirectories, these directories will be created. In addition to regular Linux-Beahaviour, this function may move files also between different media if the system supports that.

Interface variables Moves (i.e. “renames”) a file from one location to another. corresponds to “mv(1)” for files The new name may be a String, in wich case the file is simply renamed, or int may be a directory name, in whioch case the file is moved, but keeps its String. If the new path needs the creation of new subdirectories, these directories will be created. In addition to regular Linux-Beahaviour, this function may move files also between different media if the system supports that.

## IWagoSysFsInternal.RemoveDirectoryWithContents (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RemoveDirectoryWithContents | eResultCode |  |
| Input | sDirName | FileName | The name of the Directory to be deleted |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EBUSY | The directory to be removed is currently in use by the system or some process and the implementation considers this to be an error. |
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

## IWagoSysFsInternal.RemoveEmptyDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RemoveEmptyDirectory | eResultCode |  |
| Input | sDirName | FileName | The name of the Directory to be deleted |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EBUSY | The directory to be removed is currently in use by the system or some process and the implementation considers this to be an error. |
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

## IWagoSysFsInternal.RemoveFile (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RemoveFile | eResultCode |  |
| Input | sFileName | FileName | the name of the file to be removed |

| return codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EBUSY | The file cannot be removed because it is being used by the system or another process |
| EISDIR | String refers to a directory. |
| ENAMETOOLONG | String was too long. |
| ENOENT | the requeste dfile does not exist |
| EPERM | the file cannot be removed due to wrong attributes |
| EROFS | String refers to a file on a read-only file system. |

removes a file

Interface variables removes a file corresponds to “rm(1)” and “unlink/ulink(2)”

## IWagoSysFsInternal.Rename (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Rename | eResultCode |  |
| Input | sOldPath | FileName | The Directory which is to be moved |
| sNewName | FileName | the new name of that directory |
| xAllowOverwrite | BOOL | allows overwriting of existing Entities. |

| return codes |
| 0 | success |
| ENOSYS | This Functionality is not supported by the target hardware |
| EBUSY | The rename fails because oldpath or newpath is a directory that is in use by some process (perhaps as current working directory, or as root directory, or because it was open for reading) or is in use by the system (for example as mount point), while the system considers this an error. (Note that there is no requirement to return EBUSY in such cases–there is nothing wrong with doing the rename anyway–but it is allowed to return EBUSY if the system cannot otherwise handle such situations.) |
| EINVAL | The new STRING contained a path prefix of the old, or, more generally, an attempt was made to make a directory a subdirectory of itself. |
| ENAMETOOLONG | oldpath or newpath were too long. |
| ENOENT | Oldpath does not exist; or, a directory component in newpath does not exist; or, oldpath or newpath is an empty string. |
| ENOSPC | The device containing the file has no room for the new directory entry. |
| ENOTDIR | A component used as a directory in oldpath or newpath is not, in fact, a directory. Or, oldpath is a directory, and newpath exists but is not a directory. |
| ENOTEMPTY | newpath is a nonempty directory, that is, contains entries other than ”.” and ”..”. |
| EROFS | The file is on a read-only file system. |
| EXDEV | oldpath and newpath are not on the same mounted file system. (Linux permits a file system to be mounted at multiple points, but rename() does not work across different mount points, even if the same file system is mounted on both.) |

Moves (i.e. “renames”) a directory from one location to another.

corresponds to “mv(1)” for directories

The directory may contain content, but there must not be open references into that directory. If the new path needs the creation of new subdirectories, these directories will be created.

In addition to regular Linux-Beahaviour, this function may move files also between different media. In this case, a timeout may be applied. When resuming a time-outed inter-media-move, xAllowMerge must be applied.

Interface variables Moves (i.e. “renames”) a directory from one location to another. corresponds to “mv(1)” for directories The directory may contain content, but there must not be open references into that directory. If the new path needs the creation of new subdirectories, these directories will be created. In addition to regular Linux-Beahaviour, this function may move files also between different media. In this case, a timeout may be applied. When resuming a time-outed inter-media-move, xAllowMerge must be applied.

## IWagoSysFsInternal.SetAttributes (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetAttributes | eResultCode |  |
| Input | sName | FileName | name of the File or directory |
| Inout | eNewProperties | typFileProperties |  |

| return codes |
| 0 | success |
| ENOSYS | This Functionality is not supported by the target hardware |
| ENOENT | File does not exist |
| EPERM | Attributes cannot be manipulated |

sets or clears the attributes of a file

THIS FUNCTION is fed with the results OF stat():

Please note: NOT all attribute can be changed. e.g.: xDirectory may NOT be changed.

Changeable items are typivally:

Not Changeable are:

Interface variables sets or clears the attributes of a file THIS FUNCTION is fed with the results OF stat(): stat(PropertyBuffer) PropertyBuffer.xExclusive := TRUE; setAttributes(PropertyBuffer) Please note: NOT all attribute can be changed. e.g.: xDirectory may NOT be changed. Changeable items are typivally: - dtLastModification - xArchive - xHidden - xReadonly - xExclusive Not Changeable are: - sFileName - uliSize - xDirectory

## IWagoSysFsInternal.Stat (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Stat | eResultCode |  |
| Input | sName | FileName | name of the stat’ed ressource |
| pFileStatus | POINTER TO typFileProperties | Output Buffer for file Status. |

| return codes |
| 0 | success |
| ENOSYS | This Functionality is not supported by the target hardware |
| ENOENT | The requested file or directory does not exist. |

retrieves the status if a named file or directory

complement to “stat(2)”

This is recommended for determining, if a file exists at all. If a Pointer to a previously allocated filestatus structure is applied, that structure will be filled with the file information. Otherwise it will be simply checked, if the ressource exists or not.

Interface variables retrieves the status if a named file or directory complement to “stat(2)” This is recommended for determining, if a file exists at all. If a Pointer to a previously allocated filestatus structure is applied, that structure will be filled with the file information. Otherwise it will be simply checked, if the ressource exists or not.

## IWagoSysFsInternal.getFreeSpaceInDirectory (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | getFreeSpaceInDirectory | LINT |  |
| Input | sDirectoryName | FileName | the name of the investigated |

### Interfaces


## IWagoSysDirInternal (ITF)


This is the interface to a Directory-FB.

Directory FBs are used to scan directories for their included files. They behave as Read-Only-File-Systems.

This is the interface to a Directory-FB. Directory FBs are used to scan directories for their included files. They behave as Read-Only-File-Systems. - For accessing file entries, the Dir-FB must be opened first. - In further steps information about each item in the directory (file or subdirectory) is provided by the Read() method. - Finally, the directory has to be closed again, in order to free the resources for other usage, e.g. for RemoveFile(), etc, which would be blocked if the directory, in which that file resides is still opened by a directory-FB# - IWagoSysDirInternal.Close (METH) - IWagoSysDirInternal.EofReached (PROP) - IWagoSysDirInternal.IsOpen (PROP) - IWagoSysDirInternal.LastResult (PROP) - IWagoSysDirInternal.Open (METH) - IWagoSysDirInternal.Read (METH)

## IWagoSysFileInternal (ITF)


This Interface provides Access to a generic File Object.

Internal Details, such as File-handles etc. will be hidden from the user, who operates on FBs only. Reason: size and internal structure of such handles may vary between different systems.

This Interface provides Access to a generic File Object. Internal Details, such as File-handles etc. will be hidden from the user, who operates on FBs only. Reason: size and internal structure of such handles may vary between different systems. - IWagoSysFileInternal.Close (METH) - IWagoSysFileInternal.EofReached (PROP) - IWagoSysFileInternal.IsOpen (PROP) - IWagoSysFileInternal.IsReadable (PROP) - IWagoSysFileInternal.IsWritable (PROP) - IWagoSysFileInternal.LastResult (PROP) - IWagoSysFileInternal.Open (METH) - IWagoSysFileInternal.Pos (PROP) - IWagoSysFileInternal.Read (METH) - IWagoSysFileInternal.Seek (METH) - IWagoSysFileInternal.Write (METH)

## IWagoSysFsInternal (ITF)


In this interface, all functions are summarized, which operate on the whole file system.

In most cases they do not have any awareness of sequential operations or internal states / variables, wheareas in others (e.g. “setWorkingDirectory”) they very well have.

note: in most cases these functions have their POSIX-pendants with quite similar behaviour.

In this interface, all functions are summarized, which operate on the whole file system. In most cases they do not have any awareness of sequential operations or internal states / variables, wheareas in others (e.g. “setWorkingDirectory”) they very well have. note: in most cases these functions have their POSIX-pendants with quite similar behaviour. - IWagoSysFsInternal.ChangeWorkingDirectory (METH) - IWagoSysFsInternal.CopyFile (METH) - IWagoSysFsInternal.LastResult (PROP) - IWagoSysFsInternal.MakeDirectory (METH) - IWagoSysFsInternal.MoveDirectory (METH) - IWagoSysFsInternal.MoveFile (METH) - IWagoSysFsInternal.RemoveDirectoryWithContents (METH) - IWagoSysFsInternal.RemoveEmptyDirectory (METH) - IWagoSysFsInternal.RemoveFile (METH) - IWagoSysFsInternal.Rename (METH) - IWagoSysFsInternal.SetAttributes (METH) - IWagoSysFsInternal.Stat (METH) - IWagoSysFsInternal.WorkingDirectory (PROP) - IWagoSysFsInternal.getFreeSpaceInDirectory (METH)

### Internal Components


## IWagoSysDirInternal.EofReached (PROP)


indicates the end of the file for read access.

if the FB was not open, this property is TRUE;

indicates the end of the file for read access. if the FB was not open, this property is TRUE;

## IWagoSysDirInternal.IsOpen (PROP)


indicates whether the directory-FB is open for reading.

indicates whether the directory-FB is open for reading.

## IWagoSysDirInternal.LastResult (PROP)


represents the result code of the last method

corresponds to “errno”

represents the result code of the last method corresponds to “errno”

## IWagoSysFileInternal.EofReached (PROP)


indicates the end of the file for read access.

if the FB was not open, this property is TRUE;

indicates the end of the file for read access. if the FB was not open, this property is TRUE;

## IWagoSysFileInternal.IsOpen (PROP)


indicates, if a File-FB is open or not.

indicates, if a File-FB is open or not.

## IWagoSysFileInternal.IsReadable (PROP)


specifies, if the FB allows read-access

specifies, if the FB allows read-access

## IWagoSysFileInternal.IsWritable (PROP)


specifies if write-access is permitted to the File-FB

specifies if write-access is permitted to the File-FB

## IWagoSysFileInternal.LastResult (PROP)


represents the result code of the last method

corresponds to “errno”

represents the result code of the last method corresponds to “errno”

## IWagoSysFileInternal.Pos (PROP)


returns the actual position of the file pointer

corresponds to “fgetpos(3)”

if the file is not open or does not allow positioning, the position is -1.

returns the actual position of the file pointer corresponds to “fgetpos(3)” if the file is not open or does not allow positioning, the position is -1.

## IWagoSysFsInternal.LastResult (PROP)


represents the result code of the last method

corresponds to “errno”

represents the result code of the last method corresponds to “errno”

## IWagoSysFsInternal.WorkingDirectory (PROP)


retrieves the name of the current working directory if set and an empty string else.

complement to “pwd”

Note: although the workung directory can as well be retrieved and set, the setter-function is designed as method “ChangWorkingDirectory (cd)”, because it could potentially fail. The getter-function instead is designed as property get, because it does not return a status result.

retrieves the name of the current working directory if set and an empty string else. complement to “pwd” Note: although the workung directory can as well be retrieved and set, the setter-function is designed as method “ChangWorkingDirectory (cd)”, because it could potentially fail. The getter-function instead is designed as property get, because it does not return a status result.

## WagoSysFileDir_Internal_ITF Library Documentation


| Company: | WAGO |
| Title: | WagoSysFileDir_Internal_ITF |
| Version: | 1.0.2.2 |
| Categories: | WAGO Internal\|Common\|Types and Interfaces |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysFileDir_Internal_ITF |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Interface to FileSystem Interface for internal usage as well as for application programming [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Interface to FileSystem Interface for internal usage as well as for application programming [1]

### Contents:


- FuGetVersionHistory (FUN) - IWagoSysDirInternal (ITF) IWagoSysDirInternal.Close (METH) - IWagoSysDirInternal.EofReached (PROP) - IWagoSysDirInternal.IsOpen (PROP) - IWagoSysDirInternal.LastResult (PROP) - IWagoSysDirInternal.Open (METH) - IWagoSysDirInternal.Read (METH) IWagoSysFileInternal (ITF) - IWagoSysFileInternal.Close (METH) - IWagoSysFileInternal.EofReached (PROP) - IWagoSysFileInternal.IsOpen (PROP) - IWagoSysFileInternal.IsReadable (PROP) - IWagoSysFileInternal.IsWritable (PROP) - IWagoSysFileInternal.LastResult (PROP) - IWagoSysFileInternal.Open (METH) - IWagoSysFileInternal.Pos (PROP) - IWagoSysFileInternal.Read (METH) - IWagoSysFileInternal.Seek (METH) - IWagoSysFileInternal.Write (METH) IWagoSysFsInternal (ITF) - IWagoSysFsInternal.ChangeWorkingDirectory (METH) - IWagoSysFsInternal.CopyFile (METH) - IWagoSysFsInternal.LastResult (PROP) - IWagoSysFsInternal.MakeDirectory (METH) - IWagoSysFsInternal.MoveDirectory (METH) - IWagoSysFsInternal.MoveFile (METH) - IWagoSysFsInternal.RemoveDirectoryWithContents (METH) - IWagoSysFsInternal.RemoveEmptyDirectory (METH) - IWagoSysFsInternal.RemoveFile (METH) - IWagoSysFsInternal.Rename (METH) - IWagoSysFsInternal.SetAttributes (METH) - IWagoSysFsInternal.Stat (METH) - IWagoSysFsInternal.WorkingDirectory (PROP) - IWagoSysFsInternal.getFreeSpaceInDirectory (METH) ResultItems (GVL)

### Indices and tables


| [1] | Based on WagoSysFileDir_Internal_itf.library, last modified 14.01.2019, 16:45:03. The content of this file was automatically generated with None on 14.01.2019, 16:45:06 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## ResultItems (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | ERROR | ARRAY [0..26] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := ENODATA, Severity := eSeverity.info, Text := ‘No (more) data to transfer.’), STRUCT(ID := ENOSYS, Severity := eSeverity.error, Text := ‘Function not implemented.’), STRUCT(ID := EACCES, Severity := eSeverity.error, Text := ‘No Access granted or other problems while executing this function.’), STRUCT(ID := EBADF, Severity := eSeverity.error, Text := ‘File not open for the desired mode.’), STRUCT(ID := ENOTDIR, Severity := eSeverity.error, Text := ‘The referenced resource should be a proper directory name but is not.’), STRUCT(ID := EIO, Severity := eSeverity.error, Text := ‘Flush operation reported an internal failure.’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘Invalid argument, parameter, filename, or access mode.’), STRUCT(ID := EPERM, Severity := eSeverity.error, Text := ‘Operation not permitted under these circumstances.’), STRUCT(ID := ENOENT, Severity := eSeverity.error, Text := ‘No such file or directory.’), STRUCT(ID := EBUSY, Severity := eSeverity.error, Text := ‘Device or resource is busy or exclusivity restricions apply.’), STRUCT(ID := EISDIR, Severity := eSeverity.error, Text := ‘Is a directory - a regular file was expected instead of a directory.’), STRUCT(ID := EINTR, Severity := eSeverity.error, Text := ‘Interrupted - not all data cold be processed.’), STRUCT(ID := ENOSPC, Severity := eSeverity.error, Text := ‘No space left on device - we are running out of resources.’), STRUCT(ID := ECONNRESET, Severity := eSeverity.error, Text := ‘SyncedWrite failed.’), STRUCT(ID := ENOTRECOVERABLE, Severity := eSeverity.error, Text := ‘Seek failed when executing SyncedWrite.’), STRUCT(ID := EDQUOT, Severity := eSeverity.error, Text := ‘The quota of disk blocks or inodes has been exhausted.’), STRUCT(ID := EEXIST, Severity := eSeverity.error, Text := ‘File or directory exists but is expected to be non-existent.’), STRUCT(ID := EFAULT, Severity := eSeverity.error, Text := ‘Bad address or prefi or bad reference to parameters or values.’), STRUCT(ID := ENAMETOOLONG, Severity := eSeverity.error, Text := ‘File name too long.’), STRUCT(ID := EROFS, Severity := eSeverity.error, Text := ‘Read-only file system - attempt to modify a RO-file system.’), STRUCT(ID := ETIME, Severity := eSeverity.error, Text := ‘Timeout.’), STRUCT(ID := ENOTEMPTY, Severity := eSeverity.error, Text := ‘Directory not empty - we assume it should be empty.’), STRUCT(ID := EXDEV, Severity := eSeverity.error, Text := ‘Cross-device link - an invalid combination of resources.’), STRUCT(ID := EAGAIN, Severity := eSeverity.info, Text := ‘Try again: re-execution of this functionality is necessary.’), STRUCT(ID := EFBIG, Severity := eSeverity.error, Text := ‘File too large - the file size would exceed certain logical limits.’), STRUCT(ID := EBADSTATE, Severity := eSeverity.error, Text := ‘The Fb is not in the proper state for this operation.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.