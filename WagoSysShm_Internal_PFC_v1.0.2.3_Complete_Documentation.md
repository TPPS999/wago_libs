# WagoSysShm_Internal_PFC v1.0.2.3 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysShm_Internal_PFC
- **Version:** 1.0.2.3
- **Categories:** WAGO Internal|Target|PFC
- **Namespace:** WagoSysShm_Internal
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated.

target specific SHM library for PFC200

This document is automatically generated. target specific SHM library for PFC200

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks - Functions Internal_ShmCreate (FUN) - Internal_ShmDelete (FUN) - Internal_ShmDoesExist (FUN) - Internal_ShmGetSize (FUN) - Internal_ShmIsAttached (FUN) - private_ShmClose (FUN) - private_ShmGetPointer (FUN) - private_ShmOpen (FUN) Methods - FbSharedMemory_Internal.Close (METH) - FbSharedMemory_Internal.GetDataPointer (METH) - FbSharedMemory_Internal.OpenByAddress (METH) - FbSharedMemory_Internal.OpenByName (METH) Program Organization Internal Components - 90 Internal - FbSharedMemory_Internal.ActualSize (PROP) - FbSharedMemory_Internal.IsOpen (PROP) - WagoSysShm_Internal_PFC Library Documentation Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components

### Indices and tables ¶


Based on WagoSysShm_Internal_PFC.library, last modified 20.09.2024, 21:03:24. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysShm_Internal_PFC.library, last modified 20.09.2024, 21:03:24. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysShm_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.09.2024, 21:03:24 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.09.2024, 21:03:24 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysShm_Internal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysShm_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.0.2.3 |
| Title | string | WagoSysShm_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpErrors2 Interfaces Library Identification : Name: CmpErrors2 Interfaces Version: newest Company: System Namespace: CmpErrors Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysShm Library Identification : Placeholder: SysShm Default Resolution: SysShm, * (System) Namespace: SysShm Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Function Blocks


## FbSharedMemory_Internal (FB)


```
///////////////////////////////////////////////////////////////////////////
// this is the structure of the data , which is shared by our applictations
///////////////////////////////////////////////////////////////////////////

TYPE typMySharedStructure :  STRUCT   // just an example without use in reality
     bMyByte  : BYTE;
     MyData   : ARRAY [0 .. 19] OF typOtherStructures;
   END_STRUCT
END_TYPE

///////////////////////////////////////////////////////////////////////////
// For accessing typified data, we extend the shared memory base FB
///////////////////////////////////////////////////////////////////////////

FUNCTION_BLOCK FbMySharedMemory : EXTENDS WagoSysMem.FbSharedMemory_Base;
  PROPERTY pData : POINTER TO typMySharedStructure
    pData := GetDataPointer();   // pData is **typified**, while DataPointer is not.

///////////////////////////////////////////////////////////////////////////
// We make an instance of our shared memory object and initialize it
///////////////////////////////////////////////////////////////////////////

VAR
  MySHM : FbMySharedMemory
END_VAR

IF MySHM.OpenByname('Name_Of_Shm',SIZE(typMySharedStructure), FALSE, FALSE) THEN
  DoErrorHandling();
  EXIT
END_IF;

///////////////////////////////////////////////////////////////////////////
// Finaly we use the data anywhere in the application
///////////////////////////////////////////////////////////////////////////

MyShm^.bMyByte    := 42;
InterestingNumber := MyShm^.Mydata[i].ImportantComponent;
```

This function block provides access to named shared memory objects.

Those serve for inter process communication (IPC) and can be treated like non-persinstent files with non-sequential access.

Please note: This function block serves only as base class and shound not be instatiated directly, as it provides only private means for data access. Instead, other FBs should be derived from this, which implement a proper specific user interface for data access. (see below)

Typically, shared memory is mapped to existing data structures:

This function block provides access to named shared memory objects. Those serve for inter process communication (IPC) and can be treated like non-persinstent files with non-sequential access. Please note: This function block serves only as base class and shound not be instatiated directly, as it provides only private means for data access. Instead, other FBs should be derived from this, which implement a proper specific user interface for data access. (see below) Typically, shared memory is mapped to existing data structures: - FbSharedMemory_Internal.ActualSize (PROP) - FbSharedMemory_Internal.Close (METH) - FbSharedMemory_Internal.GetDataPointer (METH) - FbSharedMemory_Internal.IsOpen (PROP) - FbSharedMemory_Internal.OpenByAddress (METH) - FbSharedMemory_Internal.OpenByName (METH)

### Functions


## Internal_ShmCreate (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_ShmCreate | eResultCode |  |
| Input | sName | Filename | Name of the object |
| udiSize | UDINT | Size of the new Object |
| pData | POINTER TO BYTE | Address to map the shared memory to (0 = ignore) |
| xWipe | BOOL | if TRUE, fill the area with zeroes |
| pHandle | POINTER TO SysTypes.RTS_IEC_HANDLE | where to stor the handle on success. If 0 is given, the object will be autoclosed. |

| Internal_ShmCreate (FUN) - Interface |
| Name | Access | Type | Semantics |
| sName | IN | Filename | Name of the object |
| udiSize | IN | UDINT | Size of the new Object |
| pData | IN | POINTER TO BYTE | Address to map the shared memory to (0 = ignore) |
| xWipe | IN | BOOL | If TRUE, fill the area with zeroes |
| pHandle | IN | POINTER TO RTS_IEC_HANDLE | where to store the handle on success. |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EEXIST | The shared memory object exists, but has incompatible parameters |
| EALREADY | The shared memory object existed with the same size and name (and location). |
| EACCES | The shared memory object could not be created |
| EINVAL | Zero size or size >2G given for the size parameter |
| ENOMEM | Shared memory could not be created due to lack of memory |

creates a new shared memory object.

In contrast to the similar named function from the SysShm, this function is intended mainly for creating a SHM without keeping it open.

For internal usage, the handle MAY be kept open by passing a pHandle argument, but this usage is strongly discouraged for external usage outside of this library.

This function creates a new shared memory object.

In general it is expected that no shared memory object exists with the same name before creation. If it does, there are two options:

If the flag xWipe is set, the newly created shared memory will be wiped with zeroes.

When pData is set to an other value than 0 (“NULL”), the shared memory will be mapped to that address. Otherwise an arbitrary address will be provided by the lower layers of the system, if supported.

If pHandle is <>0, a handle to the created or existing SHM will be strored to that location. In that case the calling application/libary MUST invoke an Internal_ShmClose() call later. ATTN: Be careful to exactly match openings and closings, as otherwise the system will be messed up.

If pHandle is = 0, the SHM will be closed immediatelly after beeing created, but it will not be deleted.

Interface variables creates a new shared memory object. In contrast to the similar named function from the SysShm, this function is intended mainly for creating a SHM without keeping it open. For internal usage, the handle MAY be kept open by passing a pHandle argument, but this usage is strongly discouraged for external usage outside of this library. This function creates a new shared memory object. In general it is expected that no shared memory object exists with the same name before creation. If it does, there are two options: - if the object exists with the same parameters, the function does nothing and returns with EALREADY - else, if the object exists with incompatible parameters, the function does nothing and returns with EEXIST If the flag xWipe is set, the newly created shared memory will be wiped with zeroes. When pData is set to an other value than 0 (“NULL”), the shared memory will be mapped to that address. Otherwise an arbitrary address will be provided by the lower layers of the system, if supported. If pHandle is <>0, a handle to the created or existing SHM will be strored to that location. In that case the calling application/libary MUST invoke an Internal_ShmClose() call later. ATTN: Be careful to exactly match openings and closings, as otherwise the system will be messed up. If pHandle is = 0, the SHM will be closed immediatelly after beeing created, but it will not be deleted.

## Internal_ShmDelete (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_ShmDelete | eResultCode |  |
| Input | sName | FileName | The global Name of the shared memory to delete; |
| xForce | BOOL | delete the object even if it is kept open. |

| ShmDelete (FUN) - Interface |
| Name | Access | Type | Semantics |
| sName | IN | Filename | Name of the object |
| xForce | IN | BOOL | Delete it even if it is still in use |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| ENOENT | The shared memory object did not exist previously |
| EACCES | The shared memory object cannot be deleted |
| ELOOP | Too many tries to delete the object |
| EEXIST | The object still exists after deletion process without specific error cause |
| EBUSY | The object is kept open by another instance |

Deletes a shared memory object

used by: WagoAppMem

Interface variables Deletes a shared memory object used by: WagoAppMem

## Internal_ShmDoesExist (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_ShmDoesExist | BOOL |  |
| Input | sName | Filename | Global name of the shared memory |

| Internal_ShmDoesExist (FUN) - Interface |
| Name | Access | Type | Semantics |
| sName | IN | Filename | Name of the object |
| (none) | Return | BOOL | TRUE = it does exist, FALSE it does not exist |

Checks, if a SHM-Object with the given name does exist, regardless of the size of the SHM

Interface variables Checks, if a SHM-Object with the given name does exist, regardless of the size of the SHM used by: Internal_ShmDelete()

## Internal_ShmGetSize (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_ShmGetSize | UDINT |  |
| Input | sName | Filename | Global name of the shared memory |

| ShmGetSize (FUN) - Interface |
| Name | Access | Type | Semantics |
| sName | IN | Filename | Name of the object |
| (none) | Return | UDINT | size of the shared memory (0 if it does not exist) |

Returns the size of an existing shared memory (0 if it does not exist)

If the SHM exists but has size 0 then it is treated as non-existent, because no data space can be accessed.

Interface variables Returns the size of an existing shared memory (0 if it does not exist) If the SHM exists but has size 0 then it is treated as non-existent, because no data space can be accessed.

## Internal_ShmIsAttached (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_ShmIsAttached | BOOL |  |
| Input | sName | Filename | Global name of the shared memory |

| Internal_ShmIsAttached (FUN) - Interface |
| Name | Access | Type | Semantics |
| sName | IN | Filename | Name of the object |
| (none) | Return | BOOL | TRUE = it is attached, FALSE = not attached. |

Checks, if a SHM-Object with the given name does exist, regardless of the size of the SHM

used by: WagoAppMem

Interface variables Checks, if a SHM-Object with the given name does exist, regardless of the size of the SHM used by: WagoAppMem

## private_ShmClose (FUN)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Return | private_ShmClose | eResultCode |  |
| Input | Handle | SysTypes.RTS_IEC_HANDLE |  |
| xDelete | BOOL | FALSE |

| private_ShmClose (FUN) - Interface |
| Name | Access | Type | Semantics |
| Handle | IN | RTS_IEC_HANDLE | The handle to this object. -1 on failure. |
| xDelete | IN | BOOL | Try to delete the object with the close. |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EBADF | Malformed File Descriptor (0 or -1) |
| ENOLINK | Problems with closing |

Closes a shared memory object.

This function is mainly intended for private usage only with the internal libary. It SHOULD NOT be called from outside. The only need for external call is when a handle is kept open by Internal_ShmCreate() - which is also strongly discouraged for external usage.

In case of urgent need, hovever, this combination of create() and close() is provided also to external code.

When xDelete is set, this function tries to delete the SHM with the close. The success of that depends on if other instances have kept the SHM still open. In that case the SHM will silently not be deleted, but no error message is returned.

Interface variables Closes a shared memory object. This function is mainly intended for private usage only with the internal libary. It SHOULD NOT be called from outside. The only need for external call is when a handle is kept open by Internal_ShmCreate() - which is also strongly discouraged for external usage. In case of urgent need, hovever, this combination of create() and close() is provided also to external code. When xDelete is set, this function tries to delete the SHM with the close. The success of that depends on if other instances have kept the SHM still open. In that case the SHM will silently not be deleted, but no error message is returned.

## private_ShmGetPointer (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | private_ShmGetPointer | POINTER TO BYTE |
| Input | Handle | SysTypes.RTS_IEC_HANDLE |

| private_ShmGetPointer (FUN) - Interface |
| Name | Access | Type | Semantics |
| Handle | IN | RTS_IEC_HANDLE | The handle to this object. -1 on failure. |
| (none) | Return | POINTER TO BYTE | Pointer to the data of handle is valid, else NULL. |

| result codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EBADF | TBad File Descriptor |

Gets the data pointer of an open shm object

used by: testcode

Interface variables Gets the data pointer of an open shm object used by: testcode

## private_ShmOpen (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | private_ShmOpen | eResultCode |  |
| Input | sName | Filename | Name of the object |
| udiSize | UDINT | Size of the new Object |
| pData | POINTER TO BYTE | Address to map the shared memory to (0 = ignore) |
| xCheckAttachment | BOOL | Check if the memory is already attached, else failure |
| Output | Handle | SysTypes.RTS_IEC_HANDLE |  |
| udiResultSize | UDINT |  |

| private_ShmOpen (FUN) - Interface |
| Name | Access | Type | Semantics |
| sName | IN | Filename | Name of the object |
| udiSize | IN | UDINT | Size of the new Object |
| pData | IN | POINTER TO BYTE | Address to map the shared memory to (0 = ignore) |
| xCheckAttachment | IN | BOOL | Check proper attachment (fail EUNATCH on no attachment) |
| Handle | OUT | RTS_IEC_HANDLE | The handle to this object. -1 on failure. |
| udiResultSize | OUT | UDINT | Size of the object. |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EEXIST | The shared memory object exists, but has incompatible size |
| EBADR | The shared memory object exists, but has incompatible address pointer |
| ENOENT | The shared memory Object does not exist |
| EUNATCH | The shared memory object is not attached, but expected to be attached |
| EINVAL | Zero size or size >2G given for the size parameter |
| EACCES | Problems on open other than ‘No-Object’. |

Opens an existing shared memory object and delivers the handle and the size.

This function is intended for private usage only with the internal libary. Do not use it from other libraries or application code.

Note: every call of private_ShmOpen() MUST have a corresponding private_ShmClose() anywhere.

Interface variables Opens an existing shared memory object and delivers the handle and the size. This function is intended for private usage only with the internal libary. Do not use it from other libraries or application code. Note: every call of private_ShmOpen() MUST have a corresponding private_ShmClose() anywhere. Used by: FbShardeMemory_Interface.Open() Internal_ShmCreate()

### Methods


## FbSharedMemory_Internal.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | eResultCode |

| result codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| ENOLINK | Closing fails due to internal errors (e.g. becatse the object has gone inbetween) |
| EBADF | The object is not open |

closes the shared memory object

Interface variables closes the shared memory object

## FbSharedMemory_Internal.GetDataPointer (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetDataPointer | POINTER TO BYTE |

Returns the pointer to the shared memory resssource.

The pointer points into in the current IEC address space. If the SHM is not open, a null pointer will be returned.

This method is protected, because the user is regularly not supposed to access the SHM directly. Instead, for user access a derived FB is supposed to be defined, which provides a proper user interface for data access and uses the pointer only internally.

Interface variables Returns the pointer to the shared memory resssource. The pointer points into in the current IEC address space. If the SHM is not open, a null pointer will be returned. This method is protected, because the user is regularly not supposed to access the SHM directly. Instead, for user access a derived FB is supposed to be defined, which provides a proper user interface for data access and uses the pointer only internally.

## FbSharedMemory_Internal.OpenByAddress (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | OpenByAddress | eResultCode |  |
| Input | sName | FileName | The global name the ressource is known |
| udiSize | UDINT | The real size of the Object |
| pData | POINTER TO BYTE | The physical address of the shared memory |
| xWipe | BOOL | If TRUE, fill the area with zeroes |

| result codes |
| 0 | success |
| ENOSYS | This functionality is not supported by the target hardware |
| EEXIST | The shared memory did exist previously at different physical address |
| EACCES | The shared memory object cannot be created |

```
ShmCreate('Name', udiSize, TRUE, xWipe);
OpenByName('Name', udiSize, FALSE, TRUE);
```

Creates a shared memory object at a definite place.

The SharedMemory FB is opened for reading and writing.

In contrast to OpenByName() , this method assumes that the shared memory object does not yet exist. Otherwise it would not make any sense to assign it to a fixed physical address, because:

Thus, the only purpose of this call is to create a new shared memory object at a fixed address, in order to publish this information to other applications, and simultaneously use it in the own application.

It is equivalent to

Interface variables Creates a shared memory object at a definite place. The SharedMemory FB is opened for reading and writing. In contrast to OpenByName() , this method assumes that the shared memory object does not yet exist. Otherwise it would not make any sense to assign it to a fixed physical address, because: - if it exists at another address, we have a conflict to the previously created object - if it exists at the same address, it is obviously known by name to the system (e.g. because it is ShmCreate()d before), so giving the physical address is redundant. (Although this does not cause an error) So if the name is unknown, but the address is well known (e.g. because it is hardware), this object my be simply addressed by the address and SHM is pointless. Thus, the only purpose of this call is to create a new shared memory object at a fixed address, in order to publish this information to other applications, and simultaneously use it in the own application. It is equivalent to

## FbSharedMemory_Internal.OpenByName (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | OpenByName | eResultCode |  |
| Input | sName | FileName | The global name of the ressource |
| udiSize | UDINT | Minimum size of the Object |
| xRequiresSystemMemory | BOOL | TRUE = visibility is mandatory |
| xAssumeExisting | BOOL | Assume that the shm is created by another process. |

| result codes |
| 0 | success |
| EALREADY | FB is already open with compatible parameters (regular operation may carry on) |
| EBUSY | FB is already open with incompatible parameters. (usage with old parameters may carry on) |
| EBADSLT | Problems with opening existing SHM object |
| EACCES | Problems with creating the SHM object. |
| ENOSYS | This functionality is not supported by the target hardware |
| ENOENT | The shared memory object does not exist and cannot be created |
| EUNATCH | The shared memory is expected to be attached and initialized but it was not attached. |
| ENOMEM | The requested amount of memory cannot be granted |
| EINVAL | Invalid Parameter (e.g. name= is empty or size=0) |

Opens the shared memory FB for reading and writing

Input Parameters

Indicates that the memory is to be shared not only with other IEC-Applications, but also with other independent non-IEC-processes on the controler. If that cannot be granted, the open()-call returns ENOSYS when called with this flag set.

Note (1): When this flag is not set, the firmware may chose freely which method for providing shared memory is actually used. I.e. the shared memory is not explicitely protected from other processes, so other processes might or might not have access to this shared memory which was intended for IEC-only sharing. When ported to other hardware or firmware, however, the behaviour might silently switch to strict IEC-only shared memory without any explicite notice.

Note (2): When this flag is set, the call may fail with ENOSYS when the actual target does not support sharing memory between IEC and other different processes.

Interface variables Opens the shared memory FB for reading and writing Input Parameters sName: Systemwide unique name of the Memory ressource. If a ressource with this name does not exist, it will be created unless the flag xAssumeExisting does not forbid that. If the undelaying OS requires numerical identifiers, that detail will be hidden by firmware layers, so the user of this library will uniformly have to deal with string identifiers. Any strings which are valid as filenames would also be valid as memory identifiers. An empty string will result in EINVAL. udiSize: Required size of the ressource. If the requested size cannot be granted, ENOMEM is returned. That may happen either if the ressource has to be newly allocated and too less memory is available, or if the ressource exists with a smaller size and it cannot be upsized. If an amount of 0 or an amount >2G is requested, EINVAL is returned. xRequireSystemMemory: Indicates that the memory is to be shared not only with other IEC-Applications, but also with other independent non-IEC-processes on the controler. If that cannot be granted, the open()-call returns ENOSYS when called with this flag set. Note (1): When this flag is not set, the firmware may chose freely which method for providing shared memory is actually used. I.e. the shared memory is not explicitely protected from other processes, so other processes might or might not have access to this shared memory which was intended for IEC-only sharing. When ported to other hardware or firmware, however, the behaviour might silently switch to strict IEC-only shared memory without any explicite notice. Note (2): When this flag is set, the call may fail with ENOSYS when the actual target does not support sharing memory between IEC and other different processes. xAssumeExisting: Forbids implicite creation of the SHM object. If the ressource does not exist, it will not be created, if this flag is set. Instead ENOENT is returned. This is used if a SHM-structure has to be initialized uniquely by one explicitely given creating application and before that is done no other application is supposed to use the SHM.

### Program Organization


## 20 Program Organization Units


- FbSharedMemory_Internal (FB) FbSharedMemory_Internal.ActualSize (PROP) - FbSharedMemory_Internal.Close (METH) - FbSharedMemory_Internal.GetDataPointer (METH) - FbSharedMemory_Internal.IsOpen (PROP) - FbSharedMemory_Internal.OpenByAddress (METH) - FbSharedMemory_Internal.OpenByName (METH)

### Internal Components


## 90 Internal


- 01 auxiliary Internal_ShmCreate (FUN) - Internal_ShmDelete (FUN) - Internal_ShmDoesExist (FUN) - Internal_ShmGetSize (FUN) - Internal_ShmIsAttached (FUN) private_ShmClose (FUN) private_ShmGetPointer (FUN) private_ShmOpen (FUN)

## FbSharedMemory_Internal.ActualSize (PROP)


the actual size of shared memory (0 if not open)

the actual size of shared memory (0 if not open)

## FbSharedMemory_Internal.IsOpen (PROP)


Tells if the shared memory FB is ready for usage.

TRUE = ready, FALSE = not ready.

Tells if the shared memory FB is ready for usage. TRUE = ready, FALSE = not ready.

## WagoSysShm_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysShm_Internal_PFC |
| Version: | 1.0.2.3 |
| Categories: | WAGO Internal\|Target\|PFC |
| Namespace: | WagoSysShm_Internal |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated.

target specific SHM library for PFC200

This document is automatically generated. target specific SHM library for PFC200

### Contents:


- 20 Program Organization Units FbSharedMemory_Internal (FB) 90 Internal - 01 auxiliary - private_ShmClose (FUN) - private_ShmGetPointer (FUN) - private_ShmOpen (FUN) LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoSysShm_Internal_PFC.library, last modified 20.09.2024, 21:03:24. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysShm_Internal_PFC.library, last modified 20.09.2024, 21:03:24. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## LibraryResult (GVL)


| Name | Type |
| --- | --- |
| Factory | FbResultFactory |

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
| Constant | ERROR | ARRAY [0..14] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := EALREADY, Severity := eSeverity.info, Text := ‘FB is already open with compatible parameters.’), STRUCT(ID := ENOSYS, Severity := eSeverity.error, Text := ‘This functionality is not supported by the target hardware.’), STRUCT(ID := ENOLINK, Severity := eSeverity.error, Text := ‘Closing fails (e.g. because the object has gone inbetween).’), STRUCT(ID := EBADF, Severity := eSeverity.error, Text := ‘The object is not open or not initialzed.’), STRUCT(ID := EEXIST, Severity := eSeverity.error, Text := ‘Resource exists but is expected to be non-existent.’), STRUCT(ID := EACCES, Severity := eSeverity.error, Text := ‘Permission denied for this resource or other errors.’), STRUCT(ID := ENOENT, Severity := eSeverity.error, Text := ‘The shared memory object does not exist and cannot be created.’), STRUCT(ID := EUNATCH, Severity := eSeverity.error, Text := ‘No memory is attached to the SHM device - but was expected so.’), STRUCT(ID := ENOMEM, Severity := eSeverity.error, Text := ‘The requested amount of memory cannot be granted.’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘Invalid parameter (e.g. name=”” or size=0 or others).’), STRUCT(ID := EBUSY, Severity := eSeverity.error, Text := ‘FB is already open with incompatible parameters.’), STRUCT(ID := EBADSLT, Severity := eSeverity.error, Text := ‘Problems with opening existing SHM object.’), STRUCT(ID := EFAULT, Severity := eSeverity.error, Text := ‘Adressed memory is not in the valid address range.’), STRUCT(ID := EPERM, Severity := eSeverity.error, Text := ‘This operation is not permitted in this situation.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 11.07.2024 | 1.0.2.3 | u0103719 | update library version (context: build server,compile file) |
| 24.10.2023 | 1.0.2.2 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 08.01.2019 | 1.0.2.1 | u015842 | Properties: copyright added |
| 04.03.2016 | 1.0.2.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoSysErrorBase and WagoTypesErrorBase |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Workaround for C0351-Bug, Resolve libraries with placeholders |

WagoSysShm_Internal_PFC.library

WagoSysShm_Internal_PFC.library

### Other Components


## 01 auxiliary


- Internal_ShmCreate (FUN) - Internal_ShmDelete (FUN) - Internal_ShmDoesExist (FUN) - Internal_ShmGetSize (FUN) - Internal_ShmIsAttached (FUN)