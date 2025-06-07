# WagoSysFileDir_Internal_Common v1.0.2.3 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysFileDir_Internal_Common
- **Version:** 1.0.2.3
- **Categories:** WAGO Internal|Common
- **Namespace:** WagoSysFileDirInternalCommon
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysFileDir_Internal_Common

### Description ¶


This document is automatically generated.

Commons for internal FileDir

This document is automatically generated. Commons for internal FileDir

### Contents: ¶


Contents: - Project Information - Library Information - Functions CleanupPathComponents (FUN) - CleanupPathComponentsStrict (FUN) - FuGetVersionHistory (FUN) - denotesAdirectory (FUN) - getFilename (FUN) - getParentDirectory (FUN) - getPrefix (FUN) - hasDirectoryComponents (FUN) Internal Components Other Components

### Indices and tables ¶


Based on WagoSysFileDir_Internal_Common.library, last modified 29.05.2024, 19:51:30. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysFileDir_Internal_Common.library, last modified 29.05.2024, 19:51:30. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysFileDir_Internal_Common.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:51:30 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:51:30 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysFileDirInternalCommon |
| Placeholder | WagoSysFileDir_Internal_Common |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysFileDir_Internal_Common |
| Version | version | 1.0.2.3 |
| Title | string | WagoSysFileDir_Internal_Common |
| LibraryCategories | library-category-list | WAGO Internal\|Common |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Functions


## CleanupPathComponents (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | CleanupPathComponents | FileName |  |
| Input | sName | FileName | the |

ensures that the given Filename contains only valid chars.

attn: no prefix (‘card://’) allowed.

Interface variables ensures that the given Filename contains only valid chars. attn: no prefix (‘card://’) allowed.

## CleanupPathComponentsStrict (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | CleanupPathComponentsStrict | FileName |  |
| Input | sName | FileName | the |

ensures that the given Filename contains only valid chars.

attn: no prefix (‘card://’) allowed.

attn: this function resides here for legacy purposes only. In productive code, it may be removed.

Interface variables ensures that the given Filename contains only valid chars. attn: no prefix (‘card://’) allowed. attn: this function resides here for legacy purposes only. In productive code, it may be removed.

## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 23.10.2023 | 1.0.2.3 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 08.01.2019 | 1.0.2.2 | u015842 | Properties: copyright added |
| 13.04.2018 | 1.0.2.1 | WAGO / u013972 | Resolve documentation error |
| 22.10.2015 | 1.0.2.0 | WAGO / u013972 | Bugfix for WAT17262 - Path is limited to 80 chars |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Resolve libraries with placeholders |
| 06.03.2015 | 1.0.0.0 | RE | Release Version |

## denotesAdirectory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | denotesAdirectory | BOOL |
| Input | sName | FileName |

checks, if the given name denotes a directoy or not.

Interface variables checks, if the given name denotes a directoy or not.

## getFilename (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getFilename | Filename |
| Input | sName | Filename |

## getParentDirectory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getParentDirectory | Filename |
| Input | sName | Filename |

## getPrefix (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getPrefix | STRING |
| Input | sName | Filename |

## hasDirectoryComponents (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | hasDirectoryComponents | BOOL |
| Input | sName | Filename |

### Internal Components


## WagoSysFileDir_Internal_Common Library Documentation


| Company: | WAGO |
| Title: | WagoSysFileDir_Internal_Common |
| Version: | 1.0.2.3 |
| Categories: | WAGO Internal\|Common |
| Namespace: | WagoSysFileDirInternalCommon |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysFileDir_Internal_Common |

### Description


This document is automatically generated.

Commons for internal FileDir

This document is automatically generated. Commons for internal FileDir

### Contents:


- FuGetVersionHistory (FUN) - Program Organisation Units CleanupPathComponents (FUN) - CleanupPathComponentsStrict (FUN) - denotesAdirectory (FUN) - getFilename (FUN) - getParentDirectory (FUN) - getPrefix (FUN) - hasDirectoryComponents (FUN)

### Indices and tables


Based on WagoSysFileDir_Internal_Common.library, last modified 29.05.2024, 19:51:30. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysFileDir_Internal_Common.library, last modified 29.05.2024, 19:51:30. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Other Components


## Program Organisation Units


- CleanupPathComponents (FUN) - CleanupPathComponentsStrict (FUN) - denotesAdirectory (FUN) - getFilename (FUN) - getParentDirectory (FUN) - getPrefix (FUN) - hasDirectoryComponents (FUN)