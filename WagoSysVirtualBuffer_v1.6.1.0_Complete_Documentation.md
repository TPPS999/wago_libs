# WagoSysVirtualBuffer v1.6.1.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysVirtualBuffer
- **Version:** 1.6.1.0
- **Categories:** WAGO Internal|Common
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysVirtualBuffer

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

General Helpers [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. General Helpers [1]

### Contents: ¶


Contents: - Documentation Index 10 Documentation - Example - WagoSysVirtualBuffer Library Documentation Project Information Library Information Function Blocks - FbVirtualReadBuffer_base (FB) - FbVirtualWriteBuffer_base (FB) - MyVirtualWriteBuffer_Example (FB) Methods - FbVirtualReadBuffer_base.AttachBuffer (METH) - FbVirtualReadBuffer_base.Clear (METH) - FbVirtualReadBuffer_base.CyclicService (METH) - FbVirtualReadBuffer_base.Initialize_base (METH) - FbVirtualReadBuffer_base.LookAtFirstByte (METH) - FbVirtualReadBuffer_base.ReAttachBuffer (METH) - FbVirtualReadBuffer_base.ReadOut (METH) - FbVirtualReadBuffer_base.privAcquireDataWrapper (METH) - FbVirtualReadBuffer_base.protAcquireData (METH) - FbVirtualReadBuffer_base.protRead (METH) - ... and 11 more Program Organization Base Components - FbVirtualReadBuffer_base.AvailableSpace (PROP) - FbVirtualReadBuffer_base.IsDataAvailable (PROP) - FbVirtualReadBuffer_base.IsEmpty (PROP) - FbVirtualReadBuffer_base.IsRealBufferAttached (PROP) - FbVirtualReadBuffer_base.LastProcessingProgress (PROP) - FbVirtualReadBuffer_base.LastProcessingResult (PROP) - FbVirtualReadBuffer_base.UnprocessedData (PROP) - FbVirtualWriteBuffer_base.AvailableSpace (PROP) - FbVirtualWriteBuffer_base.IsEmpty (PROP) - FbVirtualWriteBuffer_base.IsLocked (PROP) - ... and 4 more Main Interfaces - 01 main interface - 01 main interface Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components - 02 protected - 02 protected - 03 service - 03 service - 04 properties - 04 properties - 05 private - 05 private

### Indices and tables ¶


| [1] | Based on WagoSysVirtualBuffer.library, last modified 14.01.2019, 16:34:38. The content of this file was automatically generated with None on 14.01.2019, 16:34:42 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation - Example


- MyVirtualWriteBuffer_Example (FB) MyVirtualWriteBuffer_Example.Initialize (METH) - MyVirtualWriteBuffer_Example.protProcessData (METH)

## WagoSysVirtualBuffer Library Documentation


| Company: | WAGO |
| Title: | WagoSysVirtualBuffer |
| Version: | 1.6.1.0 |
| Categories: | WAGO Internal\|Common |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysVirtualBuffer |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

General Helpers [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. General Helpers [1]

### Contents:


- 10 Documentation - Example MyVirtualWriteBuffer_Example (FB) 20 Program Organization Units - FbVirtualReadBuffer_base (FB) - FbVirtualWriteBuffer_base (FB) - eWritebufferStorageType (ENUM) LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysVirtualBuffer.library, last modified 14.01.2019, 16:34:38. The content of this file was automatically generated with None on 14.01.2019, 16:34:42 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysVirtualBuffer.library |
| contentFile | WagoSysVirtualBuffer_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 16:34:42 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 16:34:38 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysVirtualBuffer |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysVirtualBuffer |
| DefaultNamespace |  |
| Version | version | 1.6.1.0 |
| Title | string | WagoSysVirtualBuffer |
| LibraryCategories | library-category-list | WAGO Internal\|Common |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysMem Library Identification : Placeholder: SysMem Default Resolution: SysMem, * (System) Namespace: SysMem Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysFifo Library Identification : Placeholder: WagoSysFifo Default Resolution: WagoSysFifo, * (WAGO) Namespace: WagoSysFifo Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Function Blocks


## FbVirtualReadBuffer_base (FB)


Function block for providing abstract read bufferinga virtually unlimted buffer space.

Data is filled in upon request with protAquireData().

Data is removed from the virtual buffer by ‘protProcessDataOut()’, which is called by the internal framework of the FB from ‘ReadOut()’.

For implementations it is mandatory to re-implement ‘protAquireData()’ properly.

Function block for providing abstract read bufferinga virtually unlimted buffer space. Data is filled in upon request with protAquireData(). Data is removed from the virtual buffer by ‘protProcessDataOut()’, which is called by the internal framework of the FB from ‘ReadOut()’. For implementations it is mandatory to re-implement ‘protAquireData()’ properly. - 01 main interface FbVirtualReadBuffer_base.CyclicService (METH) - FbVirtualReadBuffer_base.LookAtFirstByte (METH) - FbVirtualReadBuffer_base.ReadOut (METH) 02 protected - FbVirtualReadBuffer_base.protAcquireData (METH) - FbVirtualReadBuffer_base.protRead (METH) 03 service - FbVirtualReadBuffer_base.AttachBuffer (METH) - FbVirtualReadBuffer_base.Clear (METH) - FbVirtualReadBuffer_base.Initialize_base (METH) - FbVirtualReadBuffer_base.ReAttachBuffer (METH) 04 properties - FbVirtualReadBuffer_base.AvailableSpace (PROP) - FbVirtualReadBuffer_base.IsDataAvailable (PROP) - FbVirtualReadBuffer_base.IsEmpty (PROP) - FbVirtualReadBuffer_base.IsRealBufferAttached (PROP) - FbVirtualReadBuffer_base.LastProcessingProgress (PROP) - FbVirtualReadBuffer_base.LastProcessingResult (PROP) - FbVirtualReadBuffer_base.UnprocessedData (PROP) 05 private - FbVirtualReadBuffer_base.privAcquireDataWrapper (METH)

## FbVirtualWriteBuffer_base (FB)


Function block for providing a virtually unlimted buffer space.

Data is filled in by FillIn(). Either the complete chunk of data is passed to the FB or the complete chunk is rejected.

Data is removed from the virtual buffer by ‘protProcessDataOut()’, which is called by the internal framework of the FB from ‘FillIn()’ and from ‘CyclicService()’

From the surrounding environment it is expected to cyclically call ‘CyclicService()’ as long as there is data in this FB to be processed.

For implementations it is mandatory to re-implement ‘protProcessDataOut()’ properly, while ‘protNotifyProcessing()’ may be left untouched.

Function block for providing a virtually unlimted buffer space. Data is filled in by FillIn(). Either the complete chunk of data is passed to the FB or the complete chunk is rejected. Data is removed from the virtual buffer by ‘protProcessDataOut()’, which is called by the internal framework of the FB from ‘FillIn()’ and from ‘CyclicService()’ From the surrounding environment it is expected to cyclically call ‘CyclicService()’ as long as there is data in this FB to be processed. For implementations it is mandatory to re-implement ‘protProcessDataOut()’ properly, while ‘protNotifyProcessing()’ may be left untouched. - 01 main interface FbVirtualWriteBuffer_base.CyclicService (METH) - FbVirtualWriteBuffer_base.FillIn (METH) 02 protected - FbVirtualWriteBuffer_base.protProcessData (METH) 03 service - FbVirtualWriteBuffer_base.AttachBuffer (METH) - FbVirtualWriteBuffer_base.Clear (METH) - FbVirtualWriteBuffer_base.Initialize_base (METH) - FbVirtualWriteBuffer_base.ReAttachBuffer (METH) 04 properties - FbVirtualWriteBuffer_base.AvailableSpace (PROP) - FbVirtualWriteBuffer_base.IsEmpty (PROP) - FbVirtualWriteBuffer_base.IsLocked (PROP) - FbVirtualWriteBuffer_base.IsRealBufferAttached (PROP) - FbVirtualWriteBuffer_base.LastProcessingProgress (PROP) - FbVirtualWriteBuffer_base.LastProcessingResult (PROP) - FbVirtualWriteBuffer_base.UnprocessedData (PROP) 05 private - FbVirtualWriteBuffer_base.privProcessDataWrapper (METH)

## MyVirtualWriteBuffer_Example (FB)


this is a template for deriving own classes from the virtual write buffer

this is a template for deriving own classes from the virtual write buffer - MyVirtualWriteBuffer_Example.Initialize (METH) - MyVirtualWriteBuffer_Example.protProcessData (METH)

### Methods


## FbVirtualReadBuffer_base.AttachBuffer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AttachBuffer | eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | where is the buffer range |
| udiRxBufferSize | UDINT | what size has the buffer range |

| result codes |
| 0 | success |
| EINVAL | Null-pointer or size <2 or size >2G |

attaches Buffer Space to the object.

Note: is is legal to call AttachBuffer(0,0). In that case, the buffer is detached.

Interface variables attaches Buffer Space to the object. Note: is is legal to call AttachBuffer(0,0). In that case, the buffer is detached.

## FbVirtualReadBuffer_base.Clear (METH)


whipes out all contained data but leaves the buffer space attached.

whipes out all contained data but leaves the buffer space attached.

## FbVirtualReadBuffer_base.CyclicService (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | CyclicService | eResultCode |

| result codes |
| 0 | success, data transferred |
| ENODATA | there is no data in the FB |
| others | specific error messages |

Cyclic operations

Interface variables Cyclic operations

## FbVirtualReadBuffer_base.Initialize_base (METH)


Cold start of the FB. All buffers are detached after this call.

Cold start of the FB. All buffers are detached after this call.

## FbVirtualReadBuffer_base.LookAtFirstByte (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | LookAtFirstByte | eResultCode |
| Output | bData | BYTE |

## FbVirtualReadBuffer_base.ReAttachBuffer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReAttachBuffer | eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | Location of external buffer space |
| udiRxBufferSize | UDINT | Size of the external buffer |

| result codes |
| 0 | success, ready for communication. |
| EINVAL | Invalid parameters (size beyond plausibility). |
| EFBIG | New buffer is too small for data which is already contained in the previous buffer. |

Attaches external Buffers to the FB

This method can be applied any time, even when the FB is not attached to a communication interface.

By default, each serial FB has a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115k2) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard.

This is provided by this method.

If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost.

If NULL-pointers are appilied or the buffer sizes are smaller than the internal buffers, then the internal buffer of the FB is used and the external buffer is silently ignored.

Interface variables Attaches external Buffers to the FB This method can be applied any time, even when the FB is not attached to a communication interface. By default, each serial FB has a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115k2) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard. This is provided by this method. If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost. If NULL-pointers are appilied or the buffer sizes are smaller than the internal buffers, then the internal buffer of the FB is used and the external buffer is silently ignored.

## FbVirtualReadBuffer_base.ReadOut (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReadOut | eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | where to store the data |
| udiRxBufferSize | UDINT | how much data can be accepted |
| Output | udiRxNBytes | UDINT | how much data could be read |
| eStorageType | eWritebufferStorageType | from where did they come? |

| result codes |
| 0 | complete success |
| EINVAL | invalid call parameters (null-pointer or size>2G) |
| EBUSY | new data cannot be accepted. |
| EACCES | processing returned with EINVAL or EBUSY or FIFO is not operational |
| ENOSYS | There is no method ‘protProcessDataOut’ specified. |
| others: | specific error messages |

Tries to process an amount of data.

If the complete amount of data could not be processed at once because the process would block, then the data is marked up internally for later procesing via CyclicService().

If an error occurs at the first processing attempt, the data is not fed into the buffer.

Note: It is mandatory to have protProcessDataOut re-implemented when using this function. Otherwise FillIn returns with ENOSYS.

Interface variables Tries to process an amount of data. If the complete amount of data could not be processed at once because the process would block, then the data is marked up internally for later procesing via CyclicService(). If an error occurs at the first processing attempt, the data is not fed into the buffer. Note: It is mandatory to have protProcessDataOut re-implemented when using this function. Otherwise FillIn returns with ENOSYS.

## FbVirtualReadBuffer_base.privAcquireDataWrapper (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | privAcquireDataWrapper | eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | where the data-has to be strored |
| udiRxBufferSize | UDINT | how much data to process |
| Output | udiRxNBytes | UDINT | this much data was actually processed |

| result codes |
| 0 | all data successfully processed |
| EWOULDBLOCK | not all data could be processed, but no further errors |
| ERANGE | process returned more processed bytes than fed in |
| others: | specific error messages |

Wrapper for the protected method ‘protAcquireData()’.

It is ensured, that the return values are consistent and that the number of transferred bytes are counted up properly

Interface variables Wrapper for the protected method ‘protAcquireData()’. It is ensured, that the return values are consistent and that the number of transferred bytes are counted up properly

## FbVirtualReadBuffer_base.protAcquireData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protAcquireData | eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | where the data is to be stored |
| udiRxBufferSize | UDINT | how much data to process |
| Output | udiRxNBytes | UDINT | this much data was actually processed |

| result codes |
| 0 | received data |
| ENODATA | no data available |
| others: | specific error messages |

This method is to be overwritten by a real processing routine.

Interface variables This method is to be overwritten by a real processing routine.

## FbVirtualReadBuffer_base.protRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protRead | eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | where to write the read data |
| udiRxBufferSize | UDINT | how many bytes to read maximum |
| Output | udiRxNBytes | UDINT | how many bytes are actually read. |

| result codes |
| 0 | success |
| ENODATA | no data in buffer |
| EINVAL | null-pointer or size <2 or size >2G |

Reads data directly from the fifo and maps that method interface directly. ATTN: This method is intended only for protected use in cases, where ReadOut() is to be overwritten.

Interface variables Reads data directly from the fifo and maps that method interface directly. ATTN: This method is intended only for protected use in cases, where ReadOut() is to be overwritten.

## FbVirtualWriteBuffer_base.AttachBuffer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AttachBuffer | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | where is the buffer range |
| udiTxBufferSize | UDINT | what size has the buffer range |

| result codes |
| 0 | success |
| EINVAL | Null-pointer or size <2 or size >2G |

attaches Buffer Space to the object.

Note: is is legal to call AttachBuffer(0,0). In that case, the buffer is detached.

Interface variables attaches Buffer Space to the object. Note: is is legal to call AttachBuffer(0,0). In that case, the buffer is detached.

## FbVirtualWriteBuffer_base.Clear (METH)


whipes out all contained data but leaves the buffer space attached.

whipes out all contained data but leaves the buffer space attached.

## FbVirtualWriteBuffer_base.CyclicService (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | CyclicService | eResultCode |

| result codes |
| 0 | complete success |
| EWOULDBLOCK | there is still data in the FB |
| others | specific error messages |

Cyclic operations

Interface variables Cyclic operations

## FbVirtualWriteBuffer_base.FillIn (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FillIn | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | where the data is |
| udiTxNBytes | UDINT | how much data |
| Output | eStorageType | eWritebufferStorageType | in which way is the data stored? |

| result codes |
| 0 | complete success |
| EINVAL | invalid call parameters (null-pointer or size>2G) |
| EBUSY | new data cannot be accepted. |
| EACCES | processing returned with EINVAL or EBUSY or FIFO is not operational |
| ENOSYS | There is no method ‘protProcessDataOut’ specified. |
| others: | specific error messages |

Tries to process an amount of data.

If the complete amount of data could not be processed at once because the process would block, then the data is marked up internally for later procesing via CyclicService().

If an error occurs at the first processing attempt, the data is not fed into the buffer.

Note: It is mandatory to have protProcessDataOut re-implemented when using this function. Otherwise FillIn returns with ENOSYS.

Interface variables Tries to process an amount of data. If the complete amount of data could not be processed at once because the process would block, then the data is marked up internally for later procesing via CyclicService(). If an error occurs at the first processing attempt, the data is not fed into the buffer. Note: It is mandatory to have protProcessDataOut re-implemented when using this function. Otherwise FillIn returns with ENOSYS.

## FbVirtualWriteBuffer_base.Initialize_base (METH)


Cold start of the FB. All buffers are detached after this call.

Cold start of the FB. All buffers are detached after this call.

## FbVirtualWriteBuffer_base.ReAttachBuffer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReAttachBuffer | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | Location of external buffer space |
| udiTxBufferSize | UDINT | Size of the external buffer |

| result codes |
| 0 | success, ready for communication. |
| EINVAL | Invalid parameters (size beyond plausibility). |
| EFBIG | New buffer is too small for data which is already contained in the previous buffer. |

This method can be applied any time, even when the FB is not attached to a serial interface.

By default, each serial FB has a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115k2) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard.

This is provided by this method.

If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost.

If NULL-pointers are appilied or the buffer sizes are smaller than the internal buffers, then the internal buffer of the FB is used and the external buffer is silently ignored.

Interface variables - Attaches external Buffers to the SI-FB This method can be applied any time, even when the FB is not attached to a serial interface. By default, each serial FB has a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115k2) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard. This is provided by this method. If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost. If NULL-pointers are appilied or the buffer sizes are smaller than the internal buffers, then the internal buffer of the FB is used and the external buffer is silently ignored.

## FbVirtualWriteBuffer_base.privProcessDataWrapper (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | privProcessDataWrapper | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | where the data-to-process is located |
| udiTxNBytes | UDINT | how much data to process |
| Output | udiTxNBytesTransferred | UDINT | this much data was actually processed |

| result codes |
| 0 | all data successfully processed |
| EWOULDBLOCK | not all data could be processed, but no further errors |
| ERANGE | process returned more processed bytes than fed in |
| others: | specific error messages |

Wrapper for the protected method ‘protProcessdata()’.

It is ensured, that the return values are consistent and that the number of transferred bytes are counted up properly

Interface variables Wrapper for the protected method ‘protProcessdata()’. It is ensured, that the return values are consistent and that the number of transferred bytes are counted up properly

## FbVirtualWriteBuffer_base.protProcessData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protProcessData | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | where the data-to-process is located |
| udiTxNBytes | UDINT | how much data to process |
| Output | udiTxNBytesTransferred | UDINT | this much data was actually processed |

| result codes |
| 0 | all data successfully processed |
| EWOULDBLOCK | not all data could be processed, but no further errors |
| others: | specific error messages |

This method is to be overwritten by a real processing routine.

When service delivers a result code other than OK or EWOULDBLOCK, that would be notified to the user via ‘LastProcesingResult’. The data, however, is not automatiocally removed in these cases, because the application might find a way to recover and continue processing.

Interface variables This method is to be overwritten by a real processing routine. When service delivers a result code other than OK or EWOULDBLOCK, that would be notified to the user via ‘LastProcesingResult’. The data, however, is not automatiocally removed in these cases, because the application might find a way to recover and continue processing.

## MyVirtualWriteBuffer_Example.Initialize (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | handle | UDINT | example the handle of an open connection |

Example: sets up the variable of the derived FB

Interface variables Example: sets up the variable of the derived FB

## MyVirtualWriteBuffer_Example.protProcessData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protProcessData | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | where the data-to-process is located |
| udiTxNBytes | UDINT | how much data to process |
| Output | udiTxNBytesTransferred | UDINT | this much data was actually processed |

| result codes |
| 0 | all data successfully processed |
| EWOULDBLOCK | not all data could be processed, but no further errors |
| others: | specific error messages |

This method is to be overwritten by a real processing routine.

When service delivers a result code other than OK or EWOULDBLOCK, that would be notified to the user via ‘LastProcesingResult’. The data, however, is not automatiocally removed in these cases, because the application might find a way to recover and continue processing.

Interface variables This method is to be overwritten by a real processing routine. When service delivers a result code other than OK or EWOULDBLOCK, that would be notified to the user via ‘LastProcesingResult’. The data, however, is not automatiocally removed in these cases, because the application might find a way to recover and continue processing.

## eWritebufferStorageType (ENUM)


| Name | Initial |
| --- | --- |
| NONE | 0 |
| PROCESSED_DIRECTLY |  |
| BUFFER_STORAGE |  |
| POINTER_LOCKING |  |
| OVERFLOW |  |

### Program Organization


## 20 Program Organization Units


- FbVirtualReadBuffer_base (FB) 01 main interface FbVirtualReadBuffer_base.CyclicService (METH) - FbVirtualReadBuffer_base.LookAtFirstByte (METH) - FbVirtualReadBuffer_base.ReadOut (METH) 02 protected - FbVirtualReadBuffer_base.protAcquireData (METH) - FbVirtualReadBuffer_base.protRead (METH) 03 service - FbVirtualReadBuffer_base.AttachBuffer (METH) - FbVirtualReadBuffer_base.Clear (METH) - FbVirtualReadBuffer_base.Initialize_base (METH) - FbVirtualReadBuffer_base.ReAttachBuffer (METH) 04 properties - FbVirtualReadBuffer_base.AvailableSpace (PROP) - FbVirtualReadBuffer_base.IsDataAvailable (PROP) - FbVirtualReadBuffer_base.IsEmpty (PROP) - FbVirtualReadBuffer_base.IsRealBufferAttached (PROP) - FbVirtualReadBuffer_base.LastProcessingProgress (PROP) - FbVirtualReadBuffer_base.LastProcessingResult (PROP) - FbVirtualReadBuffer_base.UnprocessedData (PROP) 05 private - FbVirtualReadBuffer_base.privAcquireDataWrapper (METH) FbVirtualWriteBuffer_base (FB) - 01 main interface FbVirtualWriteBuffer_base.CyclicService (METH) - FbVirtualWriteBuffer_base.FillIn (METH) 02 protected - FbVirtualWriteBuffer_base.protProcessData (METH) 03 service - FbVirtualWriteBuffer_base.AttachBuffer (METH) - FbVirtualWriteBuffer_base.Clear (METH) - FbVirtualWriteBuffer_base.Initialize_base (METH) - FbVirtualWriteBuffer_base.ReAttachBuffer (METH) 04 properties - FbVirtualWriteBuffer_base.AvailableSpace (PROP) - FbVirtualWriteBuffer_base.IsEmpty (PROP) - FbVirtualWriteBuffer_base.IsLocked (PROP) - FbVirtualWriteBuffer_base.IsRealBufferAttached (PROP) - FbVirtualWriteBuffer_base.LastProcessingProgress (PROP) - FbVirtualWriteBuffer_base.LastProcessingResult (PROP) - FbVirtualWriteBuffer_base.UnprocessedData (PROP) 05 private - FbVirtualWriteBuffer_base.privProcessDataWrapper (METH) eWritebufferStorageType (ENUM)

### Base Components


## FbVirtualReadBuffer_base.AvailableSpace (PROP)


Returns the amount of physically available buffer space of the object. A value of ‘0’ means that either the buffer is completely full or there is no buffer attached at all. A negative value signals, that the data area which is passed last time to the FB is still in use by the FB and it is strictly forbidden to

Note: Unless ‘AvailableSpace’ ist non-negative, it is legal to pass a chunk of data into this FB which is larger than ‘AvalilableSpace’. In that case the memory space which is pointed to is used as buffer itself.

Returns the amount of physically available buffer space of the object. A value of ‘0’ means that either the buffer is completely full or there is no buffer attached at all. A negative value signals, that the data area which is passed last time to the FB is still in use by the FB and it is strictly forbidden to 1. pass more data to the FB or 2. alter the memory space of the most recently passed data chunk. Note: Unless ‘AvailableSpace’ ist non-negative, it is legal to pass a chunk of data into this FB which is larger than ‘AvalilableSpace’. In that case the memory space which is pointed to is used as buffer itself.

## FbVirtualReadBuffer_base.IsDataAvailable (PROP)


tells if any data is written into the Fifo

tells if any data is written into the Fifo

## FbVirtualReadBuffer_base.IsEmpty (PROP) ¶


## FbVirtualReadBuffer_base.IsRealBufferAttached (PROP)


## FbVirtualReadBuffer_base.LastProcessingProgress (PROP)


The amount of data which is physically transferred at the last call of FillIn() or CyclicService().

This is normally used for Watchdogs or progress bars.

The amount of data which is physically transferred at the last call of FillIn() or CyclicService(). This is normally used for Watchdogs or progress bars.

## FbVirtualReadBuffer_base.LastProcessingResult (PROP)


Yields the result code of the last call of protProcessDataOut().

Regularly, protProcessDataOut() returns with OK or EWOULDBLOCK, while other result codes indicate serious errors in the data transfer process, e.g. a broken pipe or a disconnected socket.

Yields the result code of the last call of protProcessDataOut(). Regularly, protProcessDataOut() returns with OK or EWOULDBLOCK, while other result codes indicate serious errors in the data transfer process, e.g. a broken pipe or a disconnected socket.

## FbVirtualReadBuffer_base.UnprocessedData (PROP)


The total amount on data which is still to be processed.

The total amount on data which is still to be processed.

## FbVirtualWriteBuffer_base.AvailableSpace (PROP)


Returns the amount of physically available buffer space of the object. A value of ‘0’ means that either the buffer is completely full or there is no buffer attached at all. A negative value signals, that the data area which is passed last time to the FB is still in use by the FB and it is strictly forbidden to

Note: Unless ‘AvailableSpace’ ist non-negative, it is legal to pass a chunk of data into this FB which is larger than ‘AvalilableSpace’. In that case the memory space which is pointed to is used as buffer itself.

Returns the amount of physically available buffer space of the object. A value of ‘0’ means that either the buffer is completely full or there is no buffer attached at all. A negative value signals, that the data area which is passed last time to the FB is still in use by the FB and it is strictly forbidden to 1. pass more data to the FB or 2. alter the memory space of the most recently passed data chunk. Note: Unless ‘AvailableSpace’ ist non-negative, it is legal to pass a chunk of data into this FB which is larger than ‘AvalilableSpace’. In that case the memory space which is pointed to is used as buffer itself.

## FbVirtualWriteBuffer_base.IsEmpty (PROP) ¶


## FbVirtualWriteBuffer_base.IsLocked (PROP)


Notifies that the memory space which is passed to the FB is still in use by the FB and MUST NOT be altered until IsLocked returns to FALSE:

Note: This situation can be avoided by passing no more data to the FB than ‘AvalableSpace’ indicates.

Notifies that the memory space which is passed to the FB is still in use by the FB and MUST NOT be altered until IsLocked returns to FALSE: Note: This situation can be avoided by passing no more data to the FB than ‘AvalableSpace’ indicates.

## FbVirtualWriteBuffer_base.IsRealBufferAttached (PROP)


## FbVirtualWriteBuffer_base.LastProcessingProgress (PROP)


The amount of data which is physically transferred at the last call of FillIn() or CyclicService().

This is normally used for Watchdogs or progress bars.

The amount of data which is physically transferred at the last call of FillIn() or CyclicService(). This is normally used for Watchdogs or progress bars.

## FbVirtualWriteBuffer_base.LastProcessingResult (PROP)


Yields the result code of the last call of protProcessDataOut().

Regularly, protProcessDataOut() returns with OK or EWOULDBLOCK, while other result codes indicate serious errors in the data transfer process, e.g. a broken pipe or a disconnected socket.

Yields the result code of the last call of protProcessDataOut(). Regularly, protProcessDataOut() returns with OK or EWOULDBLOCK, while other result codes indicate serious errors in the data transfer process, e.g. a broken pipe or a disconnected socket.

## FbVirtualWriteBuffer_base.UnprocessedData (PROP)


The total amount on data which is still to be processed.

The total amount on data which is still to be processed.

### Main Interfaces


## 01 main interface


- FbVirtualReadBuffer_base.CyclicService (METH) - FbVirtualReadBuffer_base.LookAtFirstByte (METH) - FbVirtualReadBuffer_base.ReadOut (METH)

## 01 main interface


- FbVirtualWriteBuffer_base.CyclicService (METH) - FbVirtualWriteBuffer_base.FillIn (METH)

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
| Constant | ERROR | ARRAY [0..8] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := EWOULDBLOCK, Severity := eSeverity.info, Text := ‘not all data could be processed, but no further errors’), STRUCT(ID := ENODATA, Severity := eSeverity.info, Text := ‘there is no data in the FB’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘invalid parameters ‘), STRUCT(ID := EBUSY, Severity := eSeverity.error, Text := ‘new data cannot be accepted.’), STRUCT(ID := EACCES, Severity := eSeverity.error, Text := ‘processing returned with EINVAL or EBUSY or FIFO is not operational’), STRUCT(ID := ENOSYS, Severity := eSeverity.error, Text := ‘There is no method “protProcessDataOut” or similar specified.’), STRUCT(ID := EFBIG, Severity := eSeverity.error, Text := ‘New buffer is too small for data from the previous buffer.’), STRUCT(ID := ERANGE, Severity := eSeverity.error, Text := ‘Process returned more processed bytes than fed in.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.6.1.0 | u015842 | Properties: free placeholder added |
| 02.02.2016 | 1.6.0.0 | Wago / u010545 | WagoAppErrorBase changed to WagoSysErrorBase / WagoTypesErrorBase |
| 28.10.2015 | 1.5.2.0 | Wago / u013972 | Resolve Libraries with Placeholders |
| 23.09.2015 | 1.5.1.0 | WAGO / u013972 | Add Placeholder Property |
| 03.07.2015 | 1.5.0.0 | WAGO / u013972 | Release Version |

WagoAuxVirtualBuffer

### Other Components


## 02 protected


- FbVirtualReadBuffer_base.protAcquireData (METH) - FbVirtualReadBuffer_base.protRead (METH)

## 02 protected


- FbVirtualWriteBuffer_base.protProcessData (METH)

## 03 service


- FbVirtualReadBuffer_base.AttachBuffer (METH) - FbVirtualReadBuffer_base.Clear (METH) - FbVirtualReadBuffer_base.Initialize_base (METH) - FbVirtualReadBuffer_base.ReAttachBuffer (METH)

## 03 service


- FbVirtualWriteBuffer_base.AttachBuffer (METH) - FbVirtualWriteBuffer_base.Clear (METH) - FbVirtualWriteBuffer_base.Initialize_base (METH) - FbVirtualWriteBuffer_base.ReAttachBuffer (METH)

## 04 properties


- FbVirtualReadBuffer_base.AvailableSpace (PROP) - FbVirtualReadBuffer_base.IsDataAvailable (PROP) - FbVirtualReadBuffer_base.IsEmpty (PROP) - FbVirtualReadBuffer_base.IsRealBufferAttached (PROP) - FbVirtualReadBuffer_base.LastProcessingProgress (PROP) - FbVirtualReadBuffer_base.LastProcessingResult (PROP) - FbVirtualReadBuffer_base.UnprocessedData (PROP)

## 04 properties


- FbVirtualWriteBuffer_base.AvailableSpace (PROP) - FbVirtualWriteBuffer_base.IsEmpty (PROP) - FbVirtualWriteBuffer_base.IsLocked (PROP) - FbVirtualWriteBuffer_base.IsRealBufferAttached (PROP) - FbVirtualWriteBuffer_base.LastProcessingProgress (PROP) - FbVirtualWriteBuffer_base.LastProcessingResult (PROP) - FbVirtualWriteBuffer_base.UnprocessedData (PROP)

## 05 private


- FbVirtualReadBuffer_base.privAcquireDataWrapper (METH)

## 05 private


- FbVirtualWriteBuffer_base.privProcessDataWrapper (METH)