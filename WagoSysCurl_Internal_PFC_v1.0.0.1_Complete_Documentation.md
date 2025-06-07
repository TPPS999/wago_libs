# WagoSysCurl_Internal_PFC v1.0.0.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysCurl_Internal_PFC
- **Version:** 1.0.0.1
- **Categories:** WAGO Internal|Common; WAGO Internal|Feature|Common; WAGO Internal|Feature|Network; WAGO Internal|Target|PFC
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

This is an internal library. Please use WagoSysCurl [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. This is an internal library. Please use WagoSysCurl [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks FbCurl_Internal (FB) - doc10_general (FB) Methods - FbCurl_Internal.curl_easy_abort (METH) - FbCurl_Internal.curl_easy_cleanup (METH) - FbCurl_Internal.curl_easy_getResponseCode (METH) - FbCurl_Internal.curl_easy_init (METH) - FbCurl_Internal.curl_easy_perform (METH) - FbCurl_Internal.curl_easy_reset (METH) - FbCurl_Internal.curl_easy_setopt_BOOL (METH) - FbCurl_Internal.curl_easy_setopt_DINT (METH) - FbCurl_Internal.curl_easy_setopt_STRING (METH) - FbCurl_Internal.curl_easy_setopt_STRING2 (METH) - ... and 7 more Program Organization Internal Components Global Variable Lists

### Indices and tables ¶


| [1] | Based on WagoSysCurl_Internal_PFC.library, last modified 14.01.2019, 19:13:58. The content of this file was automatically generated with None on 14.01.2019, 19:14:01 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation


- doc10_general (FB) - General Interface of each FB Method oriented Interface - Scheduling Mode - Abortion Result Codes Not implemented functions Path and file notations - Canonical Filenames and Pathnames Prefix - Path - Filename and path components - Character Set - Portability Other Forms of pathes and filenames

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysCurl_Internal_PFC.library |
| contentFile | WagoSysCurl_Internal_PFC_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 19:14:01 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 19:13:58 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO / u013972 |
| DefaultNamespace |  |
| Released | bool | False |
| Company | string | WAGO |
| Title | WagoSysCurl_Internal_PFC |
| Project | WagoSysCurl_Internal_PFC |
| NoPlaceholder |  |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Version | version | 1.0.0.1 |
| LibraryCategories | library-category-list | WAGO Internal\|Common; WAGO Internal\|Feature\|Common; WAGO Internal\|Feature\|Network; WAGO Internal\|Target\|PFC |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCurl Library Identification : Placeholder: WagoTypesCurl Default Resolution: WagoTypesCurl, * (WAGO) Namespace: WagoTypesCurl Library Properties :

### Function Blocks


## FbCurl_Internal (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Output | xDone | BOOL | Successful completion of the action. |
| xBusy | BOOL | Action is still in progress. |
| xError | BOOL | Indicates an error. |
| eErrorCode | WagoTypesCurl.eCurlCode | Curl specific error code. |
| sErrorSource | STRING(255) | Source of an error. |
| sErrorString | STRING(255) | Error string that describes the error |
| udiProgressNBytes | UDINT | Number of Bytes to transfer |
| udiProgressNBytesTransferred | UDINT | Number of Bytes, that are currently transferred |
| udiNBytesCompleteTranferredToRam | UDINT | Number of Bytes, that are transferred to RAM in the execution. This output is set if the execution is finished. |

Interface variables - FbCurl_Internal.curl_easy_abort (METH) - FbCurl_Internal.curl_easy_cleanup (METH) - FbCurl_Internal.curl_easy_getResponseCode (METH) - FbCurl_Internal.curl_easy_init (METH) - FbCurl_Internal.curl_easy_perform (METH) - FbCurl_Internal.curl_easy_reset (METH) - FbCurl_Internal.curl_easy_setopt_BOOL (METH) - FbCurl_Internal.curl_easy_setopt_DINT (METH) - FbCurl_Internal.curl_easy_setopt_STRING (METH) - FbCurl_Internal.curl_easy_setopt_STRING2 (METH) - FbCurl_Internal.curl_easy_setopt_slist (METH) - FbCurl_Internal.curl_set_FilePath (METH) - FbCurl_Internal.curl_set_LogFile (METH) - FbCurl_Internal.curl_set_RAM (METH) - FbCurl_Internal.curl_slist_append (METH) - FbCurl_Internal.curl_slist_append2 (METH) - FbCurl_Internal.curl_slist_free_all (METH)

## doc10_general (FB)


This library, WagoAppFileDir, provides real time access to the files and the file system of the PLC.

This library, WagoAppFileDir, provides real time access to the files and the file system of the PLC.

## General Interface of each FB


All functionalities of FBs in the Compact (cpt) and Modular (mod) section are wrapped in FBs which uniformly implement standard WAGO behaviour models, mostly WagoExecute for simple functionalities and the method oriented ones for more complex issues.

All functionalities of FBs in the Compact (cpt) and Modular (mod) section are wrapped in FBs which uniformly implement standard WAGO behaviour models, mostly WagoExecute for simple functionalities and the method oriented ones for more complex issues.

### Method oriented Interface


In the FBGeneralFile , for example, the xExecute-Input is replaced by a couple of specific trigger methods ‘Open(filename,accesmode,...)’, ‘Close()’, Write(content), Seek(where, whence), ..., which combine specific initializing and triggering in one method.

In the FBGeneralFile , for example, the xExecute-Input is replaced by a couple of specific trigger methods ‘Open(filename,accesmode,...)’, ‘Close()’, Write(content), Seek(where, whence), ..., which combine specific initializing and triggering in one method.

### Scheduling Mode


The parameter eSchedMode controls the scheduling priority of the FB, as described in WagoSysAsync.

Beside the main intention of this library to decouple long running work from the application task, all FBs can also be run synchronously if wanted, i.e. no other task is spawned and reaction time is minimum. Details of scheduling depend on the target hardware.

For a detailed description of the scheduling modes, please refer to ‘eSchedulingMode’ in WagoTypesCommon.

The parameter eSchedMode controls the scheduling priority of the FB, as described in WagoSysAsync. Beside the main intention of this library to decouple long running work from the application task, all FBs can also be run synchronously if wanted, i.e. no other task is spawned and reaction time is minimum. Details of scheduling depend on the target hardware. For a detailed description of the scheduling modes, please refer to ‘eSchedulingMode’ in WagoTypesCommon.

### Abortion


The functionalities Abort and Timeout provide an interface for cancelling the process prematurely. Please note that the effect of abortion is delayed internally until the aborted process has finished all non-interruptible activites.

The functionalities Abort and Timeout provide an interface for cancelling the process prematurely. Please note that the effect of abortion is delayed internally until the aborted process has finished all non-interruptible activites. 1. Direct abortion: When the applications calls the abort method, the FB will terminate with the errorcode ECANCELLED after it has reached the next point where abortion is possible. 1. Time-out: When applying xExecute , a time-out value is passed to the FB. When the applied amount of time is exceeded, an internal abortion is performed automatically. If ‘0’ is passed to this input, no time-out will take place.

## Result Codes


| eResultCode |
| Posix Name | No. | Semantic |
| OK | 0 | Operation successfully completed, no error (Not Posix but useful). |
| EPERM | 1 | Operation not permitted in this situation. |
| ENOENT | 2 | No such file or directory |
| EBADF | 9 | Bad file number / File not open |
| EAGAIN | 11 | Try again (a subsequent retry of the call might be successful) |
| EACCES | 13 | Permission denied for this resource. |
| EFAULT | 14 | Bad address or bad reference to parameters or values |
| EBUSY | 16 | Device or resource busy and cannot not respond to the desired function. |
| EEXIST | 17 | File or directory exists but is expected to be non-existent. |
| EXDEV | 18 | Cross-device link - an invalid combination of resources |
| ENOTDIR | 20 | Not a directory - the referenced resource should be a proper directory name. |
| EISDIR | 21 | Is a directory - but a regular file was expected. |
| EINVAL | 22 | Invalid argument |
| EFBIG | 27 | File too large - the file size would exceed certain logical limits. |
| ENOSPC | 28 | No space left on device - we are running out of resources. |
| EROFS | 30 | Read-only file system - attempt to modify a RO-file system. |
| ENAMETOOLONG | 36 | File name too long. |
| ENOSYS | 38 | Function not implemented. |
| ENOTEMPTY | 39 | Directory not empty - we assume it should be empty. |
| ENODATA | 61 | No data available - attempt to read beyond end of file or directory. |
| EBADSTATE | 77 | Internal malfunction. |
| ETIMEDOUT | 110 | Execution terminated prematurely due to tTimeout . |
| EINPROGRESS | 115 | The asynchronous process has been started, but has not yet terminated. |
| ECANCELED | 125 | Execution was terminated prematurely by applying xAbort . |

Nearly every method returns a status code eResultCode . On success it is always a ‘0’.

Other functionalities, which 1.) return a single value and 2.) could not potentially fail are coincidentally quite simple and thus are designed as property-getters whenever possible.

There are also a methods which meet both of the above conditions but need additional input parameters or are not assigned to any instance of a function block (e.g. getWorkingDirectory()). These deliver their function result directly.

The list below directly reflects the result codes from POSIX. (operation return status, according to POSIX.1, 1996 edition, corresponding to ‘errno.h’).

Only a small subset (typically lower numbers) is actually used by the functions in this library.

Which subset of these codes is produced, and under which conditions, is defined in the context of each function or method (and stated in the header). Even when the underlying (hidden) hardware layers change their error behaviour, it is guaranteed that the published behaviour and the error codes at application level remain as stated.

The codes which are likely to appear within this library are:

The documentation of each function contains detailed informations about which codes appear under which circumstances.

Nearly every method returns a status code eResultCode . On success it is always a ‘0’. Other functionalities, which 1.) return a single value and 2.) could not potentially fail are coincidentally quite simple and thus are designed as property-getters whenever possible. There are also a methods which meet both of the above conditions but need additional input parameters or are not assigned to any instance of a function block (e.g. getWorkingDirectory()). These deliver their function result directly. The list below directly reflects the result codes from POSIX. (operation return status, according to POSIX.1, 1996 edition, corresponding to ‘errno.h’). Only a small subset (typically lower numbers) is actually used by the functions in this library. Which subset of these codes is produced, and under which conditions, is defined in the context of each function or method (and stated in the header). Even when the underlying (hidden) hardware layers change their error behaviour, it is guaranteed that the published behaviour and the error codes at application level remain as stated. The codes which are likely to appear within this library are: The documentation of each function contains detailed informations about which codes appear under which circumstances.

## Not implemented functions


If the deployed hardware does not support certain functions, the errorcode ENOSYS (38, ‘Function not implemented’) is returned, so applications can retrieve knowledge about whether a function is implemented.

If the deployed hardware does not support certain functions, the errorcode ENOSYS (38, ‘Function not implemented’) is returned, so applications can retrieve knowledge about whether a function is implemented.

## Path and file notations


### Canonical Filenames and Pathnames


The canonical form of a filename is:

prefix could be e.g: - TEMP : A temporary file system which does not survive powercycles - HOME : Data which will survive power cycles - CARD : Files on removable media, such as sd-cards

The canonical form of a filename is: prefix://path/name prefix could be e.g: - TEMP : A temporary file system which does not survive powercycles - HOME : Data which will survive power cycles - CARD : Files on removable media, such as sd-cards

#### Prefix


The prefix will be translated internally into the appropriate hardware specific mount point, e.g. ‘/media/card/’ or ‘F:’ or other names. However, these interal names are hidden from the user in order to help implementing portable applications.

The prefix can be entered in lower case letters as well as in upper case letters (but not mixed). When the system returns a prefix (e.g. as a result of GetWorkingDirectory()), it will always return the nominal form, which is upper case for local media in order to resemble windows ‘drive letters’, while it is lower case for remote drives in order to meet worldwide conventions.

The prefix will be translated internally into the appropriate hardware specific mount point, e.g. ‘/media/card/’ or ‘F:’ or other names. However, these interal names are hidden from the user in order to help implementing portable applications. The prefix can be entered in lower case letters as well as in upper case letters (but not mixed). When the system returns a prefix (e.g. as a result of GetWorkingDirectory()), it will always return the nominal form, which is upper case for local media in order to resemble windows ‘drive letters’, while it is lower case for remote drives in order to meet worldwide conventions.

#### Path


The ‘//path/’ denotes the access path to the desired resource. Canonically it starts with a double slash ‘//’ and ends with the last slash ‘/’. If a path is expected and the last character is not a slash, then that last slash will be appended. If the entered path contains backslashes (‘\’), these will be translated into canonical slashes (‘/’). When the system returns paths, the path components are always separated by slashes (‘/’).

The ‘//path/’ denotes the access path to the desired resource. Canonically it starts with a double slash ‘//’ and ends with the last slash ‘/’. If a path is expected and the last character is not a slash, then that last slash will be appended. If the entered path contains backslashes (‘\’), these will be translated into canonical slashes (‘/’). When the system returns paths, the path components are always separated by slashes (‘/’).

#### Filename and path components


The filenames and pathes may or may not include dots (‘.’) for indicating intended file usage (e.g. ‘report.csv’). Components of filenames may contain zero, one, or more dots. For file usage indication (‘extension’) the substring behind the last dot (if any) is relevant. (‘logfile_1.3.4.43.txt’)

Path components and filenames may not contain slashes or backslashes as part of their names, as these characters are reserved for separation of path components. Filenames or path components must not be empty. This ensures that the combination of two consecutive slashes (‘//’) will never appear at places other then between prefix and path.

The filenames and pathes may or may not include dots (‘.’) for indicating intended file usage (e.g. ‘report.csv’). Components of filenames may contain zero, one, or more dots. For file usage indication (‘extension’) the substring behind the last dot (if any) is relevant. (‘logfile_1.3.4.43.txt’) Path components and filenames may not contain slashes or backslashes as part of their names, as these characters are reserved for separation of path components. Filenames or path components must not be empty. This ensures that the combination of two consecutive slashes (‘//’) will never appear at places other then between prefix and path.

#### Character Set


The usable character set for filename and path components is limited only by the target hardware, which means these components may contain every character except for slashes (‘/’), backslashes (‘\’) and reserved characters 0x00..0x1f.

The library will not check or modify other characters, but these characters might be rejected by the firmware, e.g. when a new file is to be created with characters in the name, which are not supported by the firmware.

This implicit dependency upon the target hardware is known and wanted, because we envisage special situations where filenames with strange characters are required by external IT-components.

The usable character set for filename and path components is limited only by the target hardware, which means these components may contain every character except for slashes (‘/’), backslashes (‘\’) and reserved characters 0x00..0x1f. The library will not check or modify other characters, but these characters might be rejected by the firmware, e.g. when a new file is to be created with characters in the name, which are not supported by the firmware. This implicit dependency upon the target hardware is known and wanted, because we envisage special situations where filenames with strange characters are required by external IT-components.

#### Portability


In order to keep programs portable, however, we strongly recommend restricting the used character set for filenames to the following characters:

When codes in the range [0xa0..0xff] are needed, we highly recommend the use of UTF8-codes, because the use of 8-Bit character planes is a prominent point for portability issues. Codes in the range [0x80..0xbf] may lead to undefined results in other systems if used outside the context of UTF8 codes.

In order to enhance portability, target firmware (or corresponding target specific layers) may convert those characters which would otherwise not be supported into replacement characters (e.g. ‘%20%’ instead of <space>), but this behaviour is not yet specified nor is it guaranteed, so the user cannot rely on it.

In order to keep programs portable, however, we strongly recommend restricting the used character set for filenames to the following characters: [A-Z][a-z][0-9]{‘_’, ‘-‘, ‘.’, ‘+’, ‘~’, ‘=’, ‘(‘, ‘)’ } When codes in the range [0xa0..0xff] are needed, we highly recommend the use of UTF8-codes, because the use of 8-Bit character planes is a prominent point for portability issues. Codes in the range [0x80..0xbf] may lead to undefined results in other systems if used outside the context of UTF8 codes. In order to enhance portability, target firmware (or corresponding target specific layers) may convert those characters which would otherwise not be supported into replacement characters (e.g. ‘%20%’ instead of <space>), but this behaviour is not yet specified nor is it guaranteed, so the user cannot rely on it.

### Other Forms of pathes and filenames


If a filename does not start with a prefix (e.g. ‘CARD:’), then it is assumed that the name denotes either

Please note that the use of system dependant absolute paths leads to portability problems. Thus we strongly recommend using standard prefixes.

If a filename does not start with a prefix (e.g. ‘CARD:’), then it is assumed that the name denotes either - a system dependant absolute path (starting with a slash, e.g. ‘/media/card/log/actual.txt’) which will be passed unconverted to the system or - a relative path (starting with no slash ‘log/actual.txt’) where the working directory will be added for translation. Please note that the use of system dependant absolute paths leads to portability problems. Thus we strongly recommend using standard prefixes.

### Methods


## FbCurl_Internal.curl_easy_abort (METH) ¶


## FbCurl_Internal.curl_easy_cleanup (METH) ¶


## FbCurl_Internal.curl_easy_getResponseCode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | curl_easy_getResponseCode | LINT |

## FbCurl_Internal.curl_easy_init (METH) ¶


## FbCurl_Internal.curl_easy_perform (METH) ¶


## FbCurl_Internal.curl_easy_reset (METH) ¶


## FbCurl_Internal.curl_easy_setopt_BOOL (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | eCurlOption | WagoTypesCurl.eCurlOptions_BOOL |
| xParameter | BOOL |

## FbCurl_Internal.curl_easy_setopt_DINT (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | eCurlOption | WagoTypesCurl.eCurlOptions_DINT |
| diParameter | DINT |

## FbCurl_Internal.curl_easy_setopt_STRING (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | eCurlOption | WagoTypesCurl.eCurlOptions_STRING |
| sParameter | STRING(1023) |

## FbCurl_Internal.curl_easy_setopt_STRING2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | eCurlOption | WagoTypesCurl.eCurlOptions_STRING |
| pString | POINTER TO STRING |
| udiStringLength | UDINT |

## FbCurl_Internal.curl_easy_setopt_slist (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | curl_easy_setopt_slist | BOOL |
| Input | eCurlOption | WagoTypesCurl.eCurlOptions_slist |
| uiSlistIndex | UINT |

## FbCurl_Internal.curl_set_FilePath (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | sFilePath | STRING(255) |

## FbCurl_Internal.curl_set_LogFile (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | sFilePath | STRING(255) |

## FbCurl_Internal.curl_set_RAM (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | pAddress | POINTER TO BYTE |
| udiSize | UDINT |

## FbCurl_Internal.curl_slist_append (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | curl_slist_append | BOOL |
| Input | uiSlistIndex | UINT |
| sString | STRING(255) |

## FbCurl_Internal.curl_slist_append2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | curl_slist_append2 | BOOL |
| Input | uiSlistIndex | UINT |
| pString | POINTER TO STRING |
| udiStringLength | UDINT |

## FbCurl_Internal.curl_slist_free_all (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | curl_slist_free_all | BOOL |
| Input | uiSlistIndex | UINT |

### Program Organization


## 20 Program Organization Units


- FbCurl_Internal (FB) FbCurl_Internal.curl_easy_abort (METH) - FbCurl_Internal.curl_easy_cleanup (METH) - FbCurl_Internal.curl_easy_getResponseCode (METH) - FbCurl_Internal.curl_easy_init (METH) - FbCurl_Internal.curl_easy_perform (METH) - FbCurl_Internal.curl_easy_reset (METH) - FbCurl_Internal.curl_easy_setopt_BOOL (METH) - FbCurl_Internal.curl_easy_setopt_DINT (METH) - FbCurl_Internal.curl_easy_setopt_STRING (METH) - FbCurl_Internal.curl_easy_setopt_STRING2 (METH) - FbCurl_Internal.curl_easy_setopt_slist (METH) - FbCurl_Internal.curl_set_FilePath (METH) - FbCurl_Internal.curl_set_LogFile (METH) - FbCurl_Internal.curl_set_RAM (METH) - FbCurl_Internal.curl_slist_append (METH) - FbCurl_Internal.curl_slist_append2 (METH) - FbCurl_Internal.curl_slist_free_all (METH)

### Internal Components


## WagoSysCurl_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysCurl_Internal_PFC |
| Version: | 1.0.0.1 |
| Categories: | WAGO Internal\|Common; WAGO Internal\|Feature\|Common; WAGO Internal\|Feature\|Network; WAGO Internal\|Target\|PFC |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

This is an internal library. Please use WagoSysCurl [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. This is an internal library. Please use WagoSysCurl [1]

### Contents:


- 10 Documentation doc10_general (FB) - General Interface of each FB - Result Codes - Not implemented functions - Path and file notations 20 Program Organization Units - FbCurl_Internal (FB) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysCurl_Internal_PFC.library, last modified 14.01.2019, 19:13:58. The content of this file was automatically generated with None on 14.01.2019, 19:14:01 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.0.0.1 | u015842 | Properties: copyright added |
| 22.11.2018 | 1.0.0.0 | WAGO / u013972 | Add the methods curl_slist_append2() and curl_easy_setopt_STRING2() for STRINGs with a larger size |
| 13.04.2018 | 0.1.1.3 | WAGO / u013972 | Resolve documentation error |
| 23.03.2017 | 0.1.1.2 | WAGO / u013972/u016827 | Change size of sParameter of curl_easy_setopt_STRING |
| 14.11.2016 | 0.1.1.0 | WAGO / u013972 | Add metod curl_easy_getResponseCode |
| 05.11.2015 | 0.1.0.0 | WAGO / u013972 | Release Version |
| 07.07.2015 | 0.0.0.1 | WAGO / u013972 | First Version |

WagoSysCurl